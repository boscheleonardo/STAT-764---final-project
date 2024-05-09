# (PART\*) ACTIVITIES
# Activity 1 



## Library


```r
library(sf)
library(lubridate) 
library(mgcv)
library(dplyr)
library(ggmap)
library(geosphere)
library(leaflet)
```

## Read data (.gpx file) collected using app Strava


```r
url <- 'https://www.dropbox.com/scl/fi/mcotiucy8hfne8ad2wclp/Afternoon_Ride.gpx?rlkey=25hlqa7o7ug5zvevg3wmf34jc&dl=1'

data <- st_read(dsn=url,layer="track_points")


data$time <- as.character(data$time)

data <- data[,5]

data$time <- as_datetime(data$time,tz="America/Chicago")

print(data)
```

## Plot movement data


```r
# Create data frame 

df_ride <- data.frame(t = as.numeric(data$time - data$time[1]),
                          s1 = st_coordinates(data)[,1],
                          s2 = st_coordinates(data)[,2])
# Option 01.

ggplot()+
  geom_point(data = df_ride, aes(s1, s2), size = 1, color = "black")+
  labs(x = "Longitude", y = "Latitude")+
  theme_linedraw()
```

![](activity01_files/figure-latex/unnamed-chunk-3-1.pdf)<!-- --> 

## Explore movement data
<br>
The data looks okay, my only point here is that at the very beginning, when I was in the parking lot, it presents a large error in the location, but besides that, looks great. I got surprised on how it captured each side of the road I was driving, I did not expect it.  
<br>

## Fit model to movement data


```r
# Fit model to longitude (s_1)

# a. Polynomial regression

long_m1 <- lm(s1 ~ poly(t,degree=10,raw=TRUE),data=df_ride)

summary(long_m1)


# b. Generalized additive model

long_m2 <- gam(s1 ~ s(t,bs="gp",k=50),data=df_ride)

summary(long_m2)

# Fit model to latitude (s_1) 

# a. Polynomial regression

lat_m1 <- lm(s2 ~ poly(t,degree=10,raw=TRUE),data=df_ride)

summary(lat_m1)

# a. Generalized additive model

lat_m2 <- gam(s2 ~ s(t,bs="gp",k=50),data=df_ride)

summary(lat_m2)

# Obtain prediction of my location (for every 1 sec)

df.pred <- data.frame(t = seq(0,as.integer(max(df_ride$t)),by=1)) 


df.pred$s1_m1.hat <- predict(long_m1,newdata=df.pred) 
df.pred$s1_m2.hat <- predict(long_m2,newdata=df.pred)
df.pred$s2_m1.hat <- predict(lat_m1,newdata=df.pred) 
df.pred$s2_m2.hat <- predict(lat_m2,newdata=df.pred)
```

## Plot estimated movement trajectory from (5)


```r
  ggplot()+
  geom_point(data = df_ride, aes(t/60, s1), size = 3)+
  geom_line(data = df.pred, aes(t/60, s1_m1.hat), color = "orange", size = 1)+
   labs(x = "Time (minutes)", y = "Longitude", title = "1.Ponylomial regression model - Longitude")+
    theme_linedraw()
```

![](activity01_files/figure-latex/unnamed-chunk-5-1.pdf)<!-- --> 

```r
  ggplot()+
  geom_point(data = df_ride, aes(t/60, s1), size = 3)+
  geom_line(data = df.pred, aes(t/60, s1_m2.hat), color = "blue3", size = 1)+
    labs(x = "Time (minutes)", y = "Longitude", title = "2.Generalized additive model - Longitude")+
    theme_linedraw()
```

![](activity01_files/figure-latex/unnamed-chunk-5-2.pdf)<!-- --> 

```r
  ggplot()+
  geom_point(data = df_ride, aes(t/60, s2), size = 3)+
  geom_line(data = df.pred, aes(t/60, s2_m1.hat), color = "orange", size = 1)+
      labs(x = "Time (minutes)", y = "Latitude", title = "3.Polynomial regression model - Latitude")+
    theme_linedraw()
```

![](activity01_files/figure-latex/unnamed-chunk-5-3.pdf)<!-- --> 

```r
  ggplot()+
  geom_point(data = df_ride, aes(t/60, s2), size = 3)+
  geom_line(data = df.pred, aes(t/60, s2_m2.hat), color = "blue3", size = 1)+
        labs(x = "Time (minutes)", y = "Longitude", title = "4.Generalized additive model - Latitude")+
    theme_linedraw()
```

![](activity01_files/figure-latex/unnamed-chunk-5-4.pdf)<!-- --> 

### Explore estimated trajectory 


```r
ggplot()+
  geom_point(data = df_ride, aes(s1, s2), size = 3)+
  geom_point(data = df.pred, aes(s1_m1.hat, s2_m1.hat), color = "orange", size = 1)+
  labs(x = "Longitude", y = "Latitude", title = "Polynomial regression model")+
  theme_linedraw()
```

![](activity01_files/figure-latex/unnamed-chunk-6-1.pdf)<!-- --> 

```r
ggplot()+
  geom_point(data = df_ride, aes(s1, s2), size = 3)+
  geom_point(data = df.pred, aes(s1_m2.hat, s2_m2.hat), color = "blue3", size = 1)+
  labs(x = "Longitude", y = "Latitude", title = "Generalized additive model")+
  theme_linedraw()
```

![](activity01_files/figure-latex/unnamed-chunk-6-2.pdf)<!-- --> 

## Estimate velocity


```r
# 1.1 Calculate speed - observed data

df_obs <- st_as_sf(df_ride, coords = c("s1", "s2"), 
                           crs = st_crs(data))

dist_obs<- st_distance(df_obs$geometry[1:441], df_obs$geometry[2:442], by_element = T)
(sum(dist_obs)/1000)*.62
```

```
## 2.881934 [m]
```

```r
speed_obs <- (dist_obs/as.numeric(diff(df_obs$t)))*2.24
plot(df_obs$t[-1]/60, speed_obs,xlab="Time (minutes)",ylab="Velocity (miles per hour)", main = 'Observed data')
```

![](activity01_files/figure-latex/unnamed-chunk-7-1.pdf)<!-- --> 

```r
# 1. Convert model coordinates to sf object

data.hat.m1 <- st_as_sf(df.pred, coords = c("s1_m1.hat", "s2_m1.hat"), 
                           crs = st_crs(data))

data.hat.m2 <- st_as_sf(df.pred, coords = c("s1_m2.hat", "s2_m2.hat"), 
                           crs = st_crs(data))


# 1.1 Calculate speed m1
dist.hat.m1 <- st_distance(data.hat.m1$geometry[1:465], data.hat.m1$geometry[2:466], by_element = T)
(sum(dist.hat.m1)/1000)*.62
```

```
## 2.890516 [m]
```

```r
speed.hat.m1 <- (dist.hat.m1/as.numeric(diff(data.hat.m1$t)))*2.24
plot(data.hat.m1$t[-1]/60, speed.hat.m1,xlab="Time (minutes)",ylab="Velocity (miles per hour)", main = 'Polynomial regression model')
```

![](activity01_files/figure-latex/unnamed-chunk-7-2.pdf)<!-- --> 

```r
# 1.2 Calculate speed m2
dist.hat.m2 <- st_distance(data.hat.m2$geometry[1:465], data.hat.m2$geometry[2:466], by_element = T)
(sum(dist.hat.m2)/1000)*.62
```

```
## 2.802154 [m]
```

```r
speed.hat.m2 <- (dist.hat.m2/as.numeric(diff(data.hat.m2$t)))*2.24
plot(data.hat.m2$t[-1]/60, speed.hat.m2,xlab="Time (minutes)",ylab="Velocity (miles per hour)", main = 'Generalized additive model')
```

![](activity01_files/figure-latex/unnamed-chunk-7-3.pdf)<!-- --> 

