--- 
title: "STAT764: Applied Spatio-temporal Statistics - Portfolio"
author: "Leonardo L. Bosche"
date: "2024-05-09"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
# url: your book url like https://bookdown.org/yihui/bookdown
# cover-image: path to the social sharing image like images/cover.jpg
description: |
  This is a minimal example of using the bookdown package to write a book.
  The HTML output format for this example is bookdown::bs4_book,
  set in the _output.yml file.
biblio-style: apalike
csl: chicago-fullnote-bibliography.csl
---

# About

This Portfolio provides an archivable record of the three activities and daily journals of STAT 764: Applied Spatio-temporal Statistics, Spring 2024.


<!--chapter:end:index.Rmd-->

# (PART\*) JOURNALS
# 1st class - January 18th {-}

1. Something new I learned in class within the past 24 hours:
In the recent class session and through the assigned readings (pages 1-15 in Wikle et al., 2019), I gained a profound understanding of the significance of spatial-temporal analysis and its relevance in various fields, particularly within the agricultural world where I am located. Basically, all the data we collect has a temporal and spatial component included, which underscores the importance of delving into spatial-temporal analysis to extract key insights. In addition to that, I am excited about the potential applications of spatial-temporal analysis in my work and look forward to incorporating these insights into my future projects as a master's student.

2. Something I am struggling to understand that was covered in class within the past 24 hours:
At this early stage of the semester, following the introductory class session, I find myself without any specific challenges or difficulties in understanding the material. The initial class primarily focused on providing an overview and setting the stage for the upcoming topics we will explore throughout the semester. It involved insightful explanations about the structure and expectations of the course.

<!--chapter:end:0_1_January18th.Rmd-->

# 2nd class - January 25th {-}

1. Something new I learned in class within the past 24 hours:

One insightful aspect from today's class was the marathon example, which served as a valuable tool not only for revisiting polynomial regression concepts, but also to offer a comprehensive perspective on model assumptions, performance, and the examination of the line of best fit to ensure its alignment with real-world observations. 

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Regarding something I am struggling to understand are probability distributions and mathematical models, since I have never taken any mathematical/basic stat classes (my first one was STAT 705). In my opinion this is something I will need to invest some time to get a better understanding and consolidate basic principles that are essential for statistical models. 

in my opinion these are important points for statistical models which I will need to improve for sure.





<!--chapter:end:0_jan25thjournal.Rmd-->

# 3rd class - January 30th {-}

1. Something new I learned in class within the past 24 hours: 

Today’s class and the assigned readings (pages 11-14 in Wikle et al., 2019) helped me to get a better understanding of the concept of Hierarchical Statistical Models, how it is defined, and how it works. It was well covered how flexible they are in terms of assumptions manipulation aiming to improve model performance. In addition to that, its ability to portray uncertainty rather than just estimation was also a key point in my opinion. If we have additional information that might help improve our statistical model, why not use it to make better inferences? Another interesting point was that for dealing with space-time data most of the basic approach won’t work unless you really specify important assumptions (allowed in more sophisticated models) that are able to improve your model performance and consequently make meaningful inferences. 

2. Something I am struggling to understand that was covered in class within the past 24 hours: 

I am struggling to understand at this point is, how can we use those assumptions to change model performance? I mean, how it exactly works, how am I supposed to add additional information as a prior? What is related/should be considered in my selection in terms of probability distribution for a given prior? I understand that these topics have not been fully covered so far, and I am looking forward to attending the next classes and getting to know more about it. 


<!--chapter:end:1_Jan30thjournalRmd.Rmd-->

# 4th class - February 1st {-}

1. Something new I learned in class within the past 24 hours: 

I think the explanation about how to change model assumptions was great, the example using marathon data for fitting a model helped a lot, at least in my mind is clearer now how can we manage it. In addition to that, I would say that the point about removing outliers was kind of new the way it was covered, I mean thinking that we need to take into account that the error aspect might be affecting all data, not only those odd points. Lastly, I could understand better what prediction, forecasts, and hindcasts mean as a model purpose.

2. Something I am struggling to understand that was covered in class within the past 24 hours: 

I am struggling to understand at this point, why adding more complexity to our model might help on predicting but not on forecasting and hindcasting. What makes it miss the ability to extrapolate beyond the range of the data, in other words, what is the explanation for this to be happening. Communicating uncertainty is another key point I need to get a better understanding of.









<!--chapter:end:2_Feb1stjournal.Rmd-->

# 5th class - February 6th {-}

1. Something new I learned in class within the past 24 hours: 

Today’s class was a nice oportunity to review basic concepts on probability distribution function, mainly normal distribution. In adition to that, how to make my own function for the PDF (using the exponential distribution as an example) was something new for me, I think it helped to get a better understanding on how to move from mathematical equations into function for the PDF of any distribution. The difference between the mean and the expected value using the maximum "likeliehood" approach might be something simpels but I have never heard about it before, which was great to start thinking and understanding more deeply.

2. Something I am struggling to understand that was covered in class within the past 24 hours: 

I'd say that the part of the class about mathematical model rivew, specially regarding difference equations (works on discrete functions) and differential equations (works on continuous) was not clear for me and I need to look for materials to study and get familiar with it. Something I need to explore more is how to write mathematical equations in R, it would be more a programming skill that I need to practice and improve it.





<!--chapter:end:3_Feb6thjournal.Rmd-->

# 6th class - February 8th {-}

1. Something new I learned in class within the past 24 hours: 

Something new I learned in class within the past 24 hours was the Bayesian Hierarchical modeling framework, while it wasn't entirely new to me, I found that my understanding improved significantly. The concepts became clearer, and I feel more confident in my ability to use/apply this framework in my data analysis. In addition to that, what is exactly the idea behind the posterior distribution (uncertainty about parameters) and posterior predictive distribution (making predictions about future observations based on updated knowledge) were well covered in my opinion. 

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Since the last class covered a review of mathematical models and explored the example regarding the whooping crane, I didn't encounter any specific struggles, one area that piqued my curiosity and left me pondering was the process of selecting a distribution for a particular data model. I find myself wondering about the criteria we should consider when making this decision and how we can test different distributions to arrive at the most appropriate one.


<!--chapter:end:4_Feb8thjournal.Rmd-->

# 7th class - February 13th {-}

1. Something new I learned in class within the past 24 hours: 

Today's class was great for better understanding Data model, Process model, and Parameter model on a hierarchical framework. In addition to that, it is now clearer how can we add assumptions to our model, choosing distributions for each layer of the hierarchical model that reflects our real data. What is the support of the expected value and observed value was also something new from today's class, in my opinion, it is a very important step, and we should spend some time at the beginning of our data analysis process to consider unique information regarding our data which will help later when selecting the most appropriate distribution.


2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling to understand is the dynamic mathematical model example covered in class, well I could get the idea behind the dependence on births, deaths, and growth rate in the very beginning, and how it is was written, but from there to get the analytical solution, is something that is not that clear in my head at this point.

<!--chapter:end:5_Feb13journal.Rmd-->

# 8th class - February 15th {-}

1. Something new I learned in class within the past 24 hours: 

Something new for me in today's class was how we can work with the Parameter Model (prior), through Whooping crane examples we set reasonable priors to our model, which was great to better understand how this process works and what should we consider. In addition to that, simulating data from prior predictive distribution and rejection sampling were both new for me.


2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling to understand is the R coding part, I mean adding the mathematical model we selected and distribution into R. I would say that most of the codes seem okay, I can understand, but there are some specific points like more mathematical ones that I am not familiar with.

<!--chapter:end:6_Feb15thjournal.Rmd-->

# 9th class - February 20th {-}

1. Something new I learned in class within the past 24 hours: 

I'd say that something new I learned in class within the past 24 hours was how and from where we can download weather (rainfall) data. In addition to that, some features of the sf package were also new to me. The idea of first setting our goals and what we wanna make inferences on before start analyzing your data was an important point, it has been mentioned in previous classes, but it is always good to keep it in mind and have clear objectives before exploring deeply a dataset. 

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling to understand is about how to deal with NA, and how are the implications indeed to your choice. Mainly because of the extreme rainfall example, this topic came up, and in my point of view, it is not clear what is the best/preferable approach in this scenario.

<!--chapter:end:7_Feb20thjournal.Rmd-->

# 10th class - February 22th {-}

1. Something new I learned in class within the past 24 hours: 

Something new I learned in class was regarding the intro to GIS, I've been using some GIS data like shapefiles and points, however, the review from today's class was great to better interpret them. In addition to that, transformations and coordinate reference system discussion were also important to identify potential units used in this world and how to deal with them.


2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling to understand is the Gaussian process part of the class, in my opinion, it was too fast and we did not have enough time to explore it, since it is an important aspect present when working with the Hierarchical Bayesian Framework.  








<!--chapter:end:8_Feb22ndjournal.Rmd-->

# 11th class - February 27th {-}

1. Something new I learned in class within the past 24 hours: 

Something new I learned in today's class was the multivariate normal distribution and how we can use it in spatial-temporal analysis. In addition to that, the part covering potential correlation matrices to be included in the multivariate normal distribution was great to better understand which correlation is more suitable for each case based on the correlation we have among variables.  


2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling to understand is the Gaussian correlation function, I mean I could get that it is basically a mathematical function that helps us to describe how two variables are correlated, but how to interpret its results based on the output we got is something I will need to read and understand better.





<!--chapter:end:9_Feb27thjournal.Rmd-->

# 12th class - February 29th {-}

1. Something new I learned in class within the past 24 hours: 

I'd say that today's class was great for revising/learning how to apply a hierarchical model in spatial analysis, mainly through the extreme rainfall example covered in class. Starting from the exploratory data analysis (steps and what could we explore) and going to statistical data analysis, testing different models, such as a hierarchical linear model with two error terms, and comparing with a non-hierarchical approach. In addition to that, how to make spatial predictions at each pixel was something new for me. 


2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling to understand is how to properly write my model inside a function, once you have specified it with all parameters and distributions. For example in the extreme rainfall analysis, how to translate the data model and process model into the gls function in R.




<!--chapter:end:10_Feb29thjournal.Rmd-->

# 13th class - March 5th {-}

1. Something new I learned in class within the past 24 hours: 

Today's class was a great opportunity to practice concepts we've seen the last couple of weeks, mainly applying them to activity 2. I learned how to fit a simple kriging model to my elevation dataset, which I am working on to create an elevation map for a field trial, aiming to get better insights on how we should place the blocks and avoid areas with too low elevation. In addition to that, it was cool to see many different models other friends were trying to implement to their elevation data.

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling with is fitting a second order polynomial regression, I guess the model is not converging, which is why I get NA for the second-order term. I'm trying to fix it, otherwise I plan to stop by some office hours this week.

<!--chapter:end:11_March3rdjournal.Rmd-->

# 14th class - March 7th {-}

1. Something new I learned in class within the past 24 hours: 

Today's class was great to explore and learn alternatives for modeling elevation data. We saw many different approaches, such as regression trees, gradient boosting, and support vector machines.

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Since the class was more about practicing and working on activity 2, I do not have anything special to emphasize about something I am struggling with.

<!--chapter:end:12_March7thjournal.Rmd-->

# 15th class - March 19th {-}

1. Something new I learned in class within the past 24 hours: 

In today's class, we could review what was covered so far, distributions, hierarchical modeling, and model building process. I'd say that what I learned in class within the past 24 hours was mostly related to the mgcv package, how to use it, and the applications it presents.

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling with is deciding/choosing appropriate PDFs or PMFs for the data, and parameters models, I think that the following classes, which will cover more examples on this, are going to help me to clarify and get a better understanding.



<!--chapter:end:15_March19thjournal.Rmd-->

# 16th class - March 21st {-}

1. Something new I learned in class within the past 24 hours: 

In today's class, we had the opportunity to work on activity 2. I would say that something new I learned in class within the past 24 hours was mainly related to how to fit a kriging model using the gam function from the mgcv package. 

2. Something I am struggling to understand that was covered in class within the past 24 hours:

I'd say that something I still struggling with is dealing with GIS objects when making predictions.  




<!--chapter:end:16_March21stjournal.Rmd-->

# 17th class - March 26th {-}

1. Something new I learned in class within the past 24 hours: 

I'd say that something new I learned in class within the past 24 hours were techeniques for model checking/comparison, mainly the idea of collecting more data or using part of the data that was not used for model fitting to check predictive accuracy. In addition to that, the scoring rules presented and performed in today's class were great to remember and practice model comparison.

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Something I am struggling with is which scoring rule is more appropiate depending on the model we are fitting, I'd say that this is something I need to invest some time and read about it.

<!--chapter:end:17_March26thjournal.Rmd-->

# 18th class - March 28th {-}

1. Something new I learned in class within the past 24 hours: 

In today's class, I could work on my class project, and something new I learned was how to run a Generalized Additive Model using Bayesian, with brms package in R, it seems simple to implement and give us a powerful output, including uncertainty, which is something harder to get by running GAM in mgcv package. In addition to that, I learned how to add the block effect in my GAM model and check the difference between the model fitting with and without it.

2. Something I am struggling to understand that was covered in class within the past 24 hours:

I'd say that something I am struggling with is understanding the difference between outputs depending on the function we use to get the predictions, such as predict(), and posterior_predict().  






<!--chapter:end:18_March28thjournal.Rmd-->

# 19th class - April 2nd {-}

1. Something new I learned in class within the past 24 hours: 

I'd say that something new I learned in class within the past 24 hours was how to deal with spatial-temporal models for disease data, I mean the example from today's class was a great opportunity to understand the base rules and how we should think to perform our analysis, considering the spatial-temporal component and factors that might impact the result, such as data regarding surrounding areas.

2. Something I am struggling to understand that was covered in class within the past 24 hours:

I am struggling to understand every piece of the three different empirical hierarchical models used for model fitting in the Bird Cherry-oat Aphid example.





<!--chapter:end:19_April2ndjournal.Rmd-->

# 20th class - April 4th {-}

1. Something new I learned in class within the past 24 hours: 

In today's class, I could work on my class project, and something new I learned was how to use a machine learning algorithm (extreme gradient boosting) to assess features importance. Using the xgboost algorithm I could select the 5 most important variables driving corn yield response to nitrogen nutrition index. In addition to that, I used a multinomial logistic model to predict the probabilities of the different possible clusters based on the type of response, flat, plateau response, and non-plateau response.

2. Something I am struggling to understand that was covered in class within the past 24 hours:

I'd say that something I am struggling with is to improve the multinomial logistic model outcome, to be able to show the effect of the most important variables selected through xgboost within each cluster.  

<!--chapter:end:20_April4thjournal.Rmd-->

# 21st class - April 9th {-}

1. Something new I learned in class within the past 24 hours: 

Something new I learned in class within the past 24 hours was mostly related to the spatio-temporal models used for model fitting in the Bird cherry-oat aphid abundance example. The class was a great opportunity to get a better understanding of each piece of the model, especially the first and second one, using Poisson and negative binomial distributions respectively, I could also understand better the reason behind testing those two distributions and why they make sense for this kind of data. 

2. Something I am struggling to understand that was covered in class within the past 24 hours:

I'd say that something I am struggling with is understanding the third model tested in the bird cherry-oat aphid example.




<!--chapter:end:20_April9thjournal.Rmd-->

# 22nd class - April 11th {-}

1. Something new I learned in class within the past 24 hours: 

In today's class, we had the opportunity to work on activity 3. I would say that something new I learned in class within the past 24 hours was mainly related to how to fit the three different spatio-temporal models covered in class to the abundance of English grain aphid data. In addition to that, I could also measure the performance of predictions from each model.


2. Something I am struggling to understand that was covered in class within the past 24 hours:

I'd say that something I am struggling with is regarding the concurvity measurement of each model. This is something I need to double check and read about it to get to know better.

<!--chapter:end:21_April11thjournal.Rmd-->

# 25th class - April 23th {-}

1. Something new I learned in class within the past 24 hours: 

Today's class was a great opportunity to work on a spatio-temporal model fitting, using the Earthquake data and KS oil and gas well data. I'd say that something new I learned was regarding the use of IPPP (Inhomogeneous Poisson Point Process) when modeling spatio-temporal data like Earthquake.


2. Something I am struggling to understand that was covered in class within the past 24 hours:

I'd say that something I am struggling with is understanding the difference between the first and the second model performed in the analyses, in my mind both seem to use the spatio-temporal effect intine model, not only the second model.




<!--chapter:end:22_April23rdjournal.Rmd-->

# 26th class - April 25th {-}

1. Something new I learned in class within the past 24 hours: 

In today's class, we had the opportunity to work on activity 3. Mainly checking the model fitting results and measuring the performance of predictions from each model.


2. Something I am struggling to understand that was covered in class within the past 24 hours:

I'd say that something I am struggling with is writing out the three statistical models using appropriate notation and describing each component of the model using words.






<!--chapter:end:23_April25thjournal.Rmd-->

# 27th class - April 30th {-}

1. Something new I learned in class within the past 24 hours: 

I'd say that something new I learned in class within the past 24 hours was mostly related to the use of Mechanistic models as a tool for long-range forecasting within spatio-temporal analysis. 

2. Something I am struggling to understand that was covered in class within the past 24 hours:

Regarding something I am struggling to understand, I'd say that at this point I do not have any specific topic to highlight here.







<!--chapter:end:24_April30thjournal.Rmd-->

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


<!--chapter:end:activity01.Rmd-->


# Activity 2



## Library


```r
library(sf)
library(sp)
library(raster)
library(ggplot2)
library(nlme)
library(mapview)
library(dplyr)
library(gstat)
library(mgcv)
```

## Chose an area on or close to campus where it is easy for you to understand how the elevation changes. Using a smartphone record the elevation at several locations (points) within the area you chose.

Area: Agronomy North Farm (2201 North Farm - Research Center)

## Obtain a .gpx or .csv file for your elevation data. At minimum the file should contain the location and time of the elevation measurements.

Data was obtained using the app Strava.


```r
# Download shapefile of Kansas from census.gov
download.file("http://www2.census.gov/geo/tiger/GENZ2015/shp/cb_2015_us_state_20m.zip", destfile = "states.zip")
unzip("states.zip")
sf.us <- st_read("cb_2015_us_state_20m.shp")
```

```
## Reading layer `cb_2015_us_state_20m' from data source 
##   `/Users/bosche/Desktop/stat_764_portfolio/cb_2015_us_state_20m.shp' 
##   using driver `ESRI Shapefile'
## Simple feature collection with 52 features and 9 fields
## Geometry type: MULTIPOLYGON
## Dimension:     XY
## Bounding box:  xmin: -179.1743 ymin: 17.91377 xmax: 179.7739 ymax: 71.35256
## Geodetic CRS:  NAD83
```

```r
sf.kansas <- sf.us[48,6]
sf.kansas <- as(sf.kansas, 'Spatial')
```


```r
# Shapefile of study area at Agronomy North Farm - KSU (Manhattan KS)
url <- "https://www.dropbox.com/scl/fi/umgo5u6ns6jkbbykqcq90/study_area.gpx?rlkey=63gjxiifvb4xq7ll25bfwyb8c&dl=1"
pt.study.area <- st_read(dsn=url,layer="track_points")
```

```
## Reading layer `track_points' from data source 
##   `https://www.dropbox.com/scl/fi/umgo5u6ns6jkbbykqcq90/study_area.gpx?rlkey=63gjxiifvb4xq7ll25bfwyb8c&dl=1' 
##   using driver `GPX'
## Simple feature collection with 122 features and 26 fields
## Geometry type: POINT
## Dimension:     XY
## Bounding box:  xmin: -96.59424 ymin: 39.20581 xmax: -96.5938 ymax: 39.20647
## Geodetic CRS:  WGS 84
```

```r
sf.study.area  <- st_polygon(list(rbind(st_coordinates(pt.study.area),st_coordinates(pt.study.area)[1,])))
sf.study.area <- st_buffer(sf.study.area, .00006)
sf.study.area <- st_sf(st_sfc(sf.study.area), crs = crs(sf.kansas))

plot(sf.study.area)
```

![](activity2_NF_files/figure-latex/unnamed-chunk-3-1.pdf)<!-- --> 


```r
url <- "https://www.dropbox.com/scl/fi/1b5r111l0man0la5wr1vg/NF_mungbean_trial.gpx?rlkey=80dv7ghjwt57299bwip2t4iqz&dl=1"
pt.elev <- st_read(dsn=url,layer="track_points")
```

```
## Reading layer `track_points' from data source 
##   `https://www.dropbox.com/scl/fi/1b5r111l0man0la5wr1vg/NF_mungbean_trial.gpx?rlkey=80dv7ghjwt57299bwip2t4iqz&dl=1' 
##   using driver `GPX'
## Simple feature collection with 492 features and 26 fields
## Geometry type: POINT
## Dimension:     XY
## Bounding box:  xmin: -96.59423 ymin: 39.20584 xmax: -96.59381 ymax: 39.20647
## Geodetic CRS:  WGS 84
```

```r
pt.elev <- pt.elev[,4] 
```

## Plot/map your elevation data. I would recommend using R and/or Google earth.


```r
ggplot()+
  geom_sf(data = pt.elev, aes(fill = ele ), shape = 21)+
  scale_fill_viridis_c(option = "plasma", direction = -1)+
  labs(x = 'Longitude', y = 'Latitude')+
  theme_bw()+
  theme(axis.text.x = element_text(angle = 20))+
  labs(title = "Elevation data:",
       subtitle = "Field trial - Agronomy North Farm - KSU",
       fill = "Elevation (m)")
```

![](activity2_NF_files/figure-latex/unnamed-chunk-5-1.pdf)<!-- --> 

## Create data frame: elevation, longitude, latitude


```r
# Transform data to a planar coordinate reference system

pt.elev.utm <- st_transform(pt.elev,CRS("+proj=utm +zone=14 +datum=WGS84  +units=m"))
sf.study.area.utm <- st_transform(sf.study.area,CRS("+proj=utm +zone=14 +datum=WGS84  +units=m"))


# Create data frame
df.elev <- data.frame (elev = pt.elev$ele,
                          long = st_coordinates(pt.elev)[,1],
                          lat = st_coordinates(pt.elev)[,2],
                          s1 = st_coordinates(pt.elev.utm)[,1],
                          s2 = st_coordinates(pt.elev.utm)[,2])
```

The data seems to be okay, no major problems. I'd say that I wasn't expect to see more than 1 meter in elevation change, however I already knew this field has lower elevation towards east. 


```r
# Summary statistics

summary(pt.elev$ele)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   333.2   333.5   333.8   333.8   334.2   334.7
```

```r
# Box Plot

boxplot(pt.elev$ele, main = "Elevation Boxplot", ylab = "Elevation", col = "navy")
```

![](activity2_NF_files/figure-latex/unnamed-chunk-7-1.pdf)<!-- --> 

```r
# Histogram
hist(pt.elev$ele,col="navy", xlim = c(333, 335), breaks = 7, main="Histogram of elevation",xlab="elevation (m)")
```

![](activity2_NF_files/figure-latex/unnamed-chunk-7-2.pdf)<!-- --> 

```r
# Density Plot
ggplot() +
  geom_density(aes(x = pt.elev$ele), fill = "navy", alpha = 0.8) +
  xlim(333, 335)+
  labs(title = "Elevation Density Plot", x = "Elevation", y = "Density")+
  theme_bw()
```

![](activity2_NF_files/figure-latex/unnamed-chunk-7-3.pdf)<!-- --> 

## Write out the goals that you wish to accomplish using your elevation data. For example, my goal was to make a map of the Dicken’s Hall parking lot. This involves using the elevation data I collected to make predictions of the elevation at any possible spatial locations within the parking lot. I would also like to make inference about the location where the elevation is lowest within the parking lot.

My goal is to identify elevation change patterns in a specific field at Agronomy North Farm, where we plan to have an experiment this year. First of all, I wanna create an elevation map of the field, a map showing the elevation variations across the entire field. Then, I want to use the elevation data to pinpoint the lowest elevation points within the field. These areas are more susceptible to flooding and may require special attention in my experiment planning (how to place experimental blocks within the field). In addition to that, make sure the blocks are situated in areas with minimal elevation variation to minimize potential biases.

##  Write out several statistical or machine learning models that you think you can use to answer the questions/goals you wrote in prompt #5. Be as creative and inclusive here. For each statistical or machine learning model, make sure you explain each component (piece) of the model.

Linear model:    
$y_i = \beta_0 + \beta_1\cdot lon + \beta_2\cdot lon^2 + \beta_3\cdot lat + \beta_4\cdot lat^2 + \epsilon_i$  
$\epsilon_i \sim \mathcal{N}(0, \sigma^2)$  

GAM Model: 
$y_i= \beta_0 + f(lon, lat) + \epsilon_i$  
$\epsilon_i \sim \mathcal{N}(0, \sigma^2)$

##  Of the models you developed in prompt #6, find (or develop) software to fit at least two of these models to your elevation data. Note that in a perfect world, you would be able to either find existing software or develop new programs that enable you to fit any statistical or machine learning model you want. In reality, you may may end up having to make some unwanted changes to your models in prompt #6 to be able to find existing software to fit these models to the data. 

### Model 1: Non-hierarchical linear model with iid errors


```r
# Second order polynomial model

m1 <- lm(elev~s1+I(s1^2)+s2+I(s2^2),data=df.elev)

# Make raster of study area to be able to map predictions from m1
rl.E.y <- raster(,nrow=100,ncols=100,ext=extent(sf.study.area.utm),crs=crs(sf.study.area.utm))

# Make data.frame to be able to make predictions at each pixel (cell of raster)
df.pred <- data.frame(elev = NA,
                      s1 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,1],
                      s2 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,2])

# Make spatial predictions at each pixel
df.pred$elev <- predict(m1,newdata=df.pred) 


# View first 6 rows of predictions
head(df.pred) 
```

```
##       elev       s1      s2
## 1 334.2992 707720.0 4342454
## 2 334.2813 707720.5 4342454
## 3 334.2633 707721.0 4342454
## 4 334.2453 707721.5 4342454
## 5 334.2274 707722.0 4342454
## 6 334.2094 707722.5 4342454
```

```r
# Fill raster file with predictions 
rl.E.y[] <- c(df.pred$elev)

rl.E.y <- mask(rl.E.y,sf.study.area.utm)

# Plot map of predictions
plot(rl.E.y, main = "Second order polynomial regression")
plot(sf.study.area.utm,add=TRUE)
```

![](activity2_NF_files/figure-latex/unnamed-chunk-8-1.pdf)<!-- --> 

### Model 2: Hierarchical linear model with two error terms using low-rank approximation


```r
m2 <- m2 <- gam(elev~s(s1,s2,bs="gp",k=50,m=c(-2,10^4,2)),
          family=gaussian(link = "identity"),
          method = "ML",
          data=df.elev)

summary(m2)
```

```
## 
## Family: gaussian 
## Link function: identity 
## 
## Formula:
## elev ~ s(s1, s2, bs = "gp", k = 50, m = c(-2, 10^4, 2))
## 
## Parametric coefficients:
##              Estimate Std. Error t value Pr(>|t|)    
## (Intercept) 3.338e+02  3.098e-03  107775   <2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Approximate significance of smooth terms:
##            edf Ref.df    F p-value    
## s(s1,s2) 4.956      6 2851  <2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Rank: 7/50
## R-sq.(adj) =  0.972   Deviance explained = 97.2%
## -ML = -594.17  Scale est. = 0.0047207  n = 492
```

```r
# Make raster of study area to be able to map predictions from m3
rl.E.y <- raster(,nrow=100,ncols=100,ext=extent(sf.study.area.utm),crs=crs(sf.study.area.utm))


# Make data.frame to be able to make predictions at each pixel (cell of raster)
df.pred <- data.frame(elev = NA,
                      s1 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,1],
                      s2 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,2])

# Make spatial predictions at each pixel
df.pred$elev <- c(predict(m2,newdata=df.pred,type="response"))

# View first 6 rows of predictions
head(df.pred) 
```

```
##       elev       s1      s2
## 1 334.2379 707720.0 4342454
## 2 334.2175 707720.5 4342454
## 3 334.1974 707721.0 4342454
## 4 334.1774 707721.5 4342454
## 5 334.1576 707722.0 4342454
## 6 334.1380 707722.5 4342454
```

```r
# Fill raster file with predictions 
rl.E.y[] <- df.pred$elev

rl.E.y <- mask(rl.E.y,sf.study.area.utm)

# Plot map of predictions
plot(rl.E.y, main = "Kriging")
plot(sf.study.area.utm,add=TRUE)
```

![](activity2_NF_files/figure-latex/unnamed-chunk-9-1.pdf)<!-- --> 

## Related to prompt #5, use both models you fit to your elevation data in prompt #7 to answer the questions/goals. 

Based on the results, since the field shows a clear lower elevation trend towards to east, we can assign blocks from west to east, in this way we would minimize bias due to elevation changes. 

Using the second model, which seems to predict better the elevation pattern:


```r
# Make spatial predictions at each pixel
df.pred$elev <- c(predict(m1,newdata=df.pred,type="response"))

# Fill raster file with predictions 
rl.E.y[] <- df.pred$elev

# Estimate coordinates and point of minimum elevation
xyFromCell(rl.E.y,cell=which.min(rl.E.y[]))
```

```
##             x       y
## [1,] 707769.2 4342454
```

```r
rl.E.y[which.min(rl.E.y[])]
```

```
## [1] 332.5205
```

```r
# Plot estimate coordinates of maximum elevation

rl.E.y <- mask(rl.E.y,sf.study.area.utm)
plot(rl.E.y)
plot(sf.study.area.utm,add=TRUE)
points(xyFromCell(rl.E.y,cell=which.min(rl.E.y[])),col="tomato",pch="x",cex=2)
```

![](activity2_NF_files/figure-latex/unnamed-chunk-10-1.pdf)<!-- --> 

## Based on the material in Chapter 6 of Spatio-Temporal Statistics with R and our discussion in class on March 26, compare, check and evaluate the two models from #8


```r
# Create train and test data
set.seed(123)
trainIndices <- sample(1:nrow(df.elev), size = floor(0.7 * nrow(df.elev)))

# Subset the data into train and test sets
train_df <- df.elev[trainIndices, ]
test_df <- df.elev[-trainIndices, ]
```

## Fit m1 using train df


```r
# Second order polynomial model

m1 <- lm(elev~s1+I(s1^2)+s2+I(s2^2),data=train_df)

# Make raster of study area to be able to map predictions from m1
rl.E.y <- raster(,nrow=100,ncols=100,ext=extent(sf.study.area.utm),crs=crs(sf.study.area.utm))

# Make data.frame to be able to make predictions at each pixel (cell of raster)
df.pred <- data.frame(elev = NA,
                      s1 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,1],
                      s2 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,2])

# Make spatial predictions at each pixel
df.pred$elev <- predict(m1,newdata=df.pred) 


# View first 6 rows of predictions
head(df.pred) 
```

```
##       elev       s1      s2
## 1 334.3000 707720.0 4342454
## 2 334.2822 707720.5 4342454
## 3 334.2645 707721.0 4342454
## 4 334.2467 707721.5 4342454
## 5 334.2289 707722.0 4342454
## 6 334.2112 707722.5 4342454
```

```r
# Fill raster file with predictions 
rl.E.y[] <- c(df.pred$elev)

rl.E.y <- mask(rl.E.y,sf.study.area.utm)

# Plot map of predictions
plot(rl.E.y, main = "Second order polynomial regression")
plot(sf.study.area.utm,add=TRUE)
```

![](activity2_NF_files/figure-latex/unnamed-chunk-12-1.pdf)<!-- --> 

## Fit m2 using train df


```r
m2 <- m2 <- gam(elev~s(s1,s2,bs="gp",k=50,m=c(-2,10^4,2)),
          family=gaussian(link = "identity"),
          method = "ML",
          data=train_df)

summary(m2)
```

```
## 
## Family: gaussian 
## Link function: identity 
## 
## Formula:
## elev ~ s(s1, s2, bs = "gp", k = 50, m = c(-2, 10^4, 2))
## 
## Parametric coefficients:
##              Estimate Std. Error t value Pr(>|t|)    
## (Intercept) 3.338e+02  3.776e-03   88396   <2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Approximate significance of smooth terms:
##           edf Ref.df    F p-value    
## s(s1,s2) 4.94      6 1903  <2e-16 ***
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Rank: 7/50
## R-sq.(adj) =  0.971   Deviance explained = 97.1%
## -ML = -402.09  Scale est. = 0.0049059  n = 344
```

```r
# Make raster of study area to be able to map predictions from m3
rl.E.y <- raster(,nrow=100,ncols=100,ext=extent(sf.study.area.utm),crs=crs(sf.study.area.utm))


# Make data.frame to be able to make predictions at each pixel (cell of raster)
df.pred <- data.frame(elev = NA,
                      s1 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,1],
                      s2 = xyFromCell(rl.E.y,cell=1:length(rl.E.y[]))[,2])

# Make spatial predictions at each pixel
df.pred$elev <- c(predict(m2,newdata=df.pred,type="response"))

# View first 6 rows of predictions
head(df.pred) 
```

```
##       elev       s1      s2
## 1 334.2387 707720.0 4342454
## 2 334.2183 707720.5 4342454
## 3 334.1981 707721.0 4342454
## 4 334.1781 707721.5 4342454
## 5 334.1582 707722.0 4342454
## 6 334.1386 707722.5 4342454
```

```r
# Fill raster file with predictions 
rl.E.y[] <- df.pred$elev

rl.E.y <- mask(rl.E.y,sf.study.area.utm)

# Plot map of predictions
plot(rl.E.y, main = "Kriging")
plot(sf.study.area.utm,add=TRUE)
```

![](activity2_NF_files/figure-latex/unnamed-chunk-13-1.pdf)<!-- --> 

## Compare point prediction of the the expected value of elevation (E(y)) to observed records from test data set.

### m1


```r
E.y.m1 <- predict(m1,newdata=test_df)
plot(E.y.m1,test_df$elev,xlab="Predicted expected value",ylab="New observed elevation")
```

![](activity2_NF_files/figure-latex/unnamed-chunk-14-1.pdf)<!-- --> 

```r
# Quantify predictive accuracy using scoring rule 

sum(dnorm(test_df$elev,E.y.m1,log=TRUE)) # logarithmic scoring rule (proper scoring rule for linear model)
```

```
## [1] -136.5505
```

```r
mean((test_df$elev - E.y.m1)^2) # Mean square error. Commonly used scoring rule, but not proper scoring rule for ALL situations
```

```
## [1] 0.00739952
```

```r
mean(abs(test_df$elev - E.y.m1)) # Mean absolute error. Commonly used scoring rule, but not proper scoring rule for ALL situations
```

```
## [1] 0.06668116
```

```r
# Quantify calibration of predictive intervals. 

PI.m1 <- predict(m1,newdata=test_df,
               interval = c("prediction"),
               level = 0.95)

# Determine what % of the new observations fall within the prediction intervals.

mean(ifelse(test_df$elev>PI.m1[,2],1,0)*ifelse(test_df$elev<PI.m1[,3],1,0))
```

```
## [1] 0.9662162
```

### m2


```r
E.y.m2 <- predict(m2,newdata=test_df)
plot(E.y.m2,test_df$elev,xlab="Predicted expected value",ylab="New observed elevation")
```

![](activity2_NF_files/figure-latex/unnamed-chunk-15-1.pdf)<!-- --> 

```r
# Quantify predictive accuracy using scoring rule 

sum(dnorm(test_df$elev,E.y.m2,log=TRUE)) # logarithmic scoring rule (proper scoring rule for linear model)
```

```
## [1] -136.3232
```

```r
mean((test_df$elev - E.y.m2)^2) # Mean square error. Commonly used scoring rule, but not proper scoring rule for ALL situations
```

```
## [1] 0.004328524
```

```r
mean(abs(test_df$elev - E.y.m2)) # Mean absolute error. Commonly used scoring rule, but not proper scoring rule for ALL situations
```

```
## [1] 0.05134698
```

```r
# Quantify calibration of predictive intervals. 

PI.m2 <- predict(m2,newdata=test_df,
               interval = c("prediction"),
               level = 0.95)
```

In summary, comparing both models, the m2 (GAM) was the best model, presenting lower logarithmic scoring rule, MSE and MAE.


<!--chapter:end:activity2_NF.Rmd-->


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



<!--chapter:end:activity3.Rmd-->

