
# Activity 3 



## Library 


```r
library(sf)
library(sp)
library(raster)
library(mgcv)
library(ggplot2)
library(dplyr)
library(ggpubr)
```

## Import KS map and aphid data


```r
# Download data on English grain aphid

url <- "https://www.dropbox.com/scl/fi/9ymxt900s77uq50ca6dgc/Enders-et-al.-2018-data.csv?rlkey=0rxjwleenhgu0gvzow5p0x9xf&dl=1"
df1 <- read.csv(url)
df1 <- df1[,c(2,8:10)] # Keep only the data on English grain aphid

pts.sample <- data.frame(long = df1$long,lat = df1$lat, 
                         count = df1$EGA)
coordinates(pts.sample) =~ long + lat
proj4string(pts.sample) <- CRS("+proj=longlat +datum=WGS84 +no_defs +ellps=WGS84 +towgs84=0,0,0")
```

## Data visualization


```r
# Download KS shapefile
ks <- raster::getData(name="GADM", country="USA", level=1) %>% 
  st_as_sf() %>% 
  dplyr::filter(NAME_1 == "Kansas")

coordinates <- st_as_sf(df1, coords = c("long", "lat"), crs = st_crs(ks))

# Plot
ggplot() +
  geom_sf(data = ks, fill = "grey90", color = "black") +
  geom_point(data = df1, aes(x = long, y = lat, size = EGA), shape = 21) +
  #scale_fill_viridis_c (option = "viridis", direction = -1) +
  labs(title = "Abundance of English Grain Aphids", x = "Longitude", y = "Latitude")+
  facet_wrap(~year)
```

![](activity3_files/figure-latex/unnamed-chunk-3-1.pdf)<!-- --> 

```r
hist(df1$EGA)
```

![](activity3_files/figure-latex/unnamed-chunk-3-2.pdf)<!-- --> 

```r
# Download National Land Cover Database
url.nlcd <- "https://www.dropbox.com/scl/fi/ew7yzm93aes7l8l37cn65/KS_2011_NLCD.img?rlkey=60ahyvxhq18gt0yr47tuq5fig&dl=1"
rl.nlcd2011 <- raster(url.nlcd)

# Make raster file that contains pixels with value of 1 if grassland and 
# zero if other type of land cover.
plot(rl.nlcd2011)
```

![](activity3_files/figure-latex/unnamed-chunk-3-3.pdf)<!-- --> 

```r
rl.nlcd.grass <- rl.nlcd2011
rl.nlcd.grass[] <- ifelse(rl.nlcd.grass[]==71,1,0)

plot(rl.nlcd.grass)
```

![](activity3_files/figure-latex/unnamed-chunk-3-4.pdf)<!-- --> 

```r
# Calculate percentage of land area that is grassland withing 5 km of sampled location
df1$grass.perc <- unlist(lapply(extract(rl.nlcd.grass,pts.sample,buffer=5000),mean))*100

hist(df1$grass.perc,col="grey",main="",xlab="% grassland within \n5 km at sample location")
```

![](activity3_files/figure-latex/unnamed-chunk-3-5.pdf)<!-- --> 

## 1. For the data on the abundance of English grain aphids, propose three different statistical models (or machine learning approach) that are capable of predicting the number of English grain aphids at any location within the state of Kansas at any time for the years 2014 and 2015. Make sure to write out the three statistical models using formal notation and fully describe each component using words.

### Model 1

Data model
$$Z = y$$
Process model
Using Poisson distribution

$$[y|\lambda] = Poisson(\lambda) $$

$$\eta_s\sim MVN(0, \Sigma)$$
$$\eta_t\sim MVN(0, \Sigma)$$
$$E(y)=e^{\beta_0+\beta_1\cdot X+\eta_s+\eta_t}$$

### Model 2

Data model
$$Z = y$$
Process model
Using Negative binomial distribution

$$[y|r,p] = NB(r, p)$$
$$\eta_s\sim MVN(0, \Sigma)$$
$$\eta_t\sim MVN(0, \Sigma)$$
$$E(y)=e^{\beta_0+\beta_1\cdot X+\eta_s+\eta_t}$$
### Model 3

Data model
$$Z = y$$
Process model
Using zero inflated poisson distribution

$$[y|p, \lambda]=ZIP(p,\lambda)$$
$$\eta_s\sim MVN(0, \Sigma)$$
$$P(y=0) = p\cdot e^{-0} + (1-p) \cdot e^{-{\lambda}}$$
$$P(y = k) = (1-p) \cdot \frac{(e^{-{\lambda}}{\lambda^k})}{k!}, k \in N$$
$${\lambda} > 0, p \in (0,1)$$
$$E(y)=e^{\beta_0+\beta_1\cdot X+\eta_s+\eta_t}$$

## 2. For the three statistical models you proposed in question #1, propose a way to measure the accuracy (and perhaps the calibration) of predictions.

Mean absolute error(MAE), Mean square error (MSE) and Akaike information criteria (AIC)

$$MAE = \frac{\sum^n_{i=1} |y_i - x_i|}{n}$$
$$MSE = \frac{1}{n} \sum^n_{i=1}{(Y_i - \hat{Y}_i)^2}$$
$$AIC = 2k - 2ln(\hat{L})$$


## 3. Fit the three statistical models you proposed in question #1 to the English grain aphid abundance data.


```r
# Split df
set.seed(100)
df.sample <- sample(c(TRUE,FALSE), nrow(df1), replace=TRUE, prob=c(0.5,0.5))
df.train <- df1[df.sample,]
df.test <- df1[!df.sample,]
```

### Model 1


```r
m1 <- gam(EGA ~ grass.perc + as.factor(year) + s(long,lat, bs = "gp"), 
          family = poisson(link = "log"), data = df.train)

summary(m1)
```

```
## 
## Family: poisson 
## Link function: log 
## 
## Formula:
## EGA ~ grass.perc + as.factor(year) + s(long, lat, bs = "gp")
## 
## Parametric coefficients:
##                      Estimate Std. Error z value Pr(>|z|)    
## (Intercept)         -4.072721   0.508579  -8.008 1.17e-15 ***
## grass.perc          -0.034166   0.001664 -20.538  < 2e-16 ***
## as.factor(year)2015  6.148542   0.500663  12.281  < 2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Approximate significance of smooth terms:
##               edf Ref.df Chi.sq p-value    
## s(long,lat) 31.45   31.8   5663  <2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## R-sq.(adj) =   0.67   Deviance explained = 81.1%
## UBRE = 17.558  Scale est. = 1         n = 178
```

### Model 2


```r
m2 <- gam(EGA ~ grass.perc + as.factor(year) + s(long,lat, bs = "gp"), 
          family = nb(theta = NULL,link = "log"), data = df.train)

summary(m2)
```

```
## 
## Family: Negative Binomial(0.653) 
## Link function: log 
## 
## Formula:
## EGA ~ grass.perc + as.factor(year) + s(long, lat, bs = "gp")
## 
## Parametric coefficients:
##                     Estimate Std. Error z value Pr(>|z|)    
## (Intercept)         -3.29390    0.61890  -5.322 1.03e-07 ***
## grass.perc          -0.00141    0.00678  -0.208    0.835    
## as.factor(year)2015  5.67995    0.59656   9.521  < 2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Approximate significance of smooth terms:
##               edf Ref.df Chi.sq p-value    
## s(long,lat) 8.356  11.02  224.3  <2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## R-sq.(adj) =  0.263   Deviance explained = 72.7%
## -REML = 493.04  Scale est. = 1         n = 178
```

### Model 3


```r
m3 <- gam(list(EGA ~ grass.perc + as.factor(year) + s(long,lat, bs = "gp"), ~ s(long,lat, bs = "gp")), 
          family = ziplss(), data = df.train)

summary(m3)
```

```
## 
## Family: ziplss 
## Link function: identity identity 
## 
## Formula:
## EGA ~ grass.perc + as.factor(year) + s(long, lat, bs = "gp")
## ~s(long, lat, bs = "gp")
## 
## Parametric coefficients:
##                       Estimate Std. Error z value Pr(>|z|)    
## (Intercept)         -3.5612020  0.9360800  -3.804 0.000142 ***
## grass.perc          -0.0395195  0.0017325 -22.811  < 2e-16 ***
## as.factor(year)2015  5.5461797  0.9273705   5.981 2.22e-09 ***
## (Intercept).1        0.0008942  0.1018556   0.009 0.992995    
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Approximate significance of smooth terms:
##                  edf Ref.df  Chi.sq p-value    
## s(long,lat)   30.937 31.330 4819.22 < 2e-16 ***
## s.1(long,lat)  2.485  2.891   15.84 0.00131 ** 
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Deviance explained = 78.1%
## -REML = 1761.5  Scale est. = 1         n = 178
```

### Create points for prediction


```r
newPoints <- st_sample(ks, size = 1000, type = "regular") %>% 
  as(., 'Spatial') %>% as.data.frame() %>% 
    rename("long" = "coords.x1", 
          "lat" = "coords.x2") %>% 
  cross_join(data.frame(year = as.factor(c('2014', '2015'))))

pts.sample<- newPoints

coordinates(pts.sample) =~ long + lat
proj4string(pts.sample) <- CRS("+proj=longlat +datum=WGS84 +no_defs +ellps=WGS84 +towgs84=0,0,0")

# Calculate percentage of land area that is grassland withing 5 km of new points location

newPoints$grass.perc <- unlist(lapply(extract(rl.nlcd.grass,pts.sample,buffer=5000),mean))*100

# Step 2: Use predict() to obtain predictions
newPoints$predictions.m1 <- predict(m1, newdata = newPoints, type = "response")
newPoints$predictions.m2 <- predict(m2, newdata = newPoints, type = "response")
newPoints$predictions.m3 <- predict(m3, newdata = newPoints, type = "response")
```

### Plot predictions


```r
# model 1
ggplot() +
  geom_tile(data = newPoints, aes(x = long, y = lat, fill = predictions.m1))+
  geom_sf(data = ks, fill = NA, color = 'black')+
  scale_fill_viridis_c(option = "plasma")+ 
  labs(title = "Model 1 - Abundance of English grain aphids", x = "Longitude", y = "Latitude")+
  facet_wrap(~year, ncol = 1)+
  theme_bw()
```

![](activity3_files/figure-latex/unnamed-chunk-9-1.pdf)<!-- --> 


```r
# model 2
ggplot() +
  geom_tile(data = newPoints, aes(x = long, y = lat, fill = predictions.m2))+
  geom_sf(data = ks, fill = NA, color = 'black')+
  scale_fill_viridis_c(option = "plasma")+ 
  labs(title = "Model 2 - Abundance of English grain aphids", x = "Longitude", y = "Latitude")+
  facet_wrap(~year, ncol = 1)+
  theme_bw()
```

![](activity3_files/figure-latex/unnamed-chunk-10-1.pdf)<!-- --> 


```r
#model 3
ggplot() +
  geom_tile(data = newPoints, aes(x = long, y = lat, fill = predictions.m3))+
  geom_sf(data = ks, fill = NA, color = 'black')+
  scale_fill_viridis_c(option = "plasma")+ 
  labs(title = "Model 3 - Abundance of English grain aphids", x = "Longitude", y = "Latitude")+
  facet_wrap(~year, ncol = 1)+
  theme_bw()
```

![](activity3_files/figure-latex/unnamed-chunk-11-1.pdf)<!-- --> 

## 4. For the three models you fit in question #3, which model makes the most accurate predictions? How good is the best model in real world terms? Remember we are trying to predict the number of English grain aphids, which is a count!

Model 2 makes the most accurate predictions.


```r
pred.m1 <- predict(m1, newdata = df.test, type = "response")
pred.m2 <- predict(m2, newdata = df.test, type = "response")
pred.m3 <- predict(m3, newdata = df.test, type = "response")

# Calculate AIC
AIC(m1, m2, m3)
```

```
##          df      AIC
## m1 34.44604 3764.439
## m2 14.12373  980.207
## m3 38.22045 3311.273
```

```r
# Calculate MAE
mae.m1 <- mean(abs(df.test$EGA - pred.m1))
mae.m2 <- mean(abs(df.test$EGA - pred.m2))
mae.m3 <- mean(abs(df.test$EGA - pred.m3))

# Calculate RMSE
rmse.m1 <- sqrt(mean((df.test$EGA - pred.m1)^2))
rmse.m2 <- sqrt(mean((df.test$EGA - pred.m2)^2))
rmse.m3 <- sqrt(mean((df.test$EGA - pred.m3)^2))

# MAE:
mae.m1
```

```
## [1] 37.94015
```

```r
mae.m2
```

```
## [1] 24.29216
```

```r
mae.m3
```

```
## [1] 35.37633
```

```r
# RMSE
rmse.m1
```

```
## [1] 99.04343
```

```r
rmse.m2
```

```
## [1] 77.86172
```

```r
rmse.m3
```

```
## [1] 95.28032
```

### Plot observed vs. predicted


```r
m1_metric <- ggplot(df.test, aes(x = EGA)) +
  geom_point(aes(y = pred.m1), fill = "navy", shape = 21) +
  geom_line(aes(y = EGA), linetype = "dotted", color = "black") +
  labs(title = "Model 1",
       x = "Observed EGA",
       y = "Predicted EGA")+
  theme_bw()+
  theme(panel.grid = element_blank(),
        aspect.ratio = 1,
        text = element_text(size = 12))

m2_metric <- ggplot(df.test, aes(x = EGA)) +
  geom_point(aes(y = pred.m2), fill = "darkgreen", shape = 21) +
  geom_line(aes(y = EGA), linetype = "dotted", color = "black") +
  labs(title = "Model 2",
       x = "Observed EGA",
       y = "Predicted EGA")+
  theme_bw()+
  theme(panel.grid = element_blank(),
        aspect.ratio = 1,
        text = element_text(size = 12))

m3_metric <- ggplot(df.test, aes(x = EGA)) +
  geom_point(aes(y = pred.m3), fill = "tomato", shape = 21) +
  geom_line(aes(y = EGA), linetype = "dotted", color = "black") +
  labs(title = "Model 3",
       x = "Observed EGA",
       y = "Predicted EGA")+
  theme_bw()+
  theme(panel.grid = element_blank(),
        aspect.ratio = 1,
        text = element_text(size = 12))

ggarrange(m1_metric, m2_metric, m3_metric, nrow = 1)
```

![](activity3_files/figure-latex/unnamed-chunk-13-1.pdf)<!-- --> 

## 5. Summarize your results using words, numerical values and figures/maps.

I've decided to split the data into training and testing subsets (50/50), aiming to evaluate predictive performance. In summary, the subsequent model, built upon the assumption of a negative binomial distribution for the process model (m2), exhibited the best predictive accuracy. This superiority was evident in the forecasted visual representations and was further corroborated by the reduced values of AIC, MAE, and RMSE in comparison to m1 and m3. Notably, 2014 exhibited a minimal abundance of EGA, whereas 2015 witnessed a notable concentration of EGA in the East region.


