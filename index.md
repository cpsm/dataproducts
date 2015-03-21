---
title       : Data Products Assignment Project
subtitle    : Design and Performance of automobiles
author      : Simon
job         : Student Developing data products cours
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---
## Introduction

 * Data from 1974 Motor Trend US Magazine to compare 10 aspects of automoile design
   and performance is stored in mtcars data

*  Data consists of design and pertormance of 32 automobile during the year(1973-74)

*  The variables  are as follows
       1  Miles/(US) gallon
       2  Number of cylinder
       3  Displacement (cu.in.)
       4  Gross horsepower
       5  Rear axle ratio
       6  Weight (lb/1000)
       7  1/4 mile time
       8  V/S
       9  Transmission (0 = automatic, 1 = manual)
       10 Number of forward gears
       11 Number of carburetors


--- .class #id 

## Data Summary

#### Summary of the data objects 


```
## [1] 32 11
```

```
##       mpg             cyl             disp             hp       
##  Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0  
##  1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5  
##  Median :19.20   Median :6.000   Median :196.3   Median :123.0  
##  Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7  
##  3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0  
##  Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0  
##       drat             wt             qsec             vs        
##  Min.   :2.760   Min.   :1.513   Min.   :14.50   Min.   :0.0000  
##  1st Qu.:3.080   1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000  
##  Median :3.695   Median :3.325   Median :17.71   Median :0.0000  
##  Mean   :3.597   Mean   :3.217   Mean   :17.85   Mean   :0.4375  
##  3rd Qu.:3.920   3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000  
##  Max.   :4.930   Max.   :5.424   Max.   :22.90   Max.   :1.0000  
##        am              gear            carb      
##  Min.   :0.0000   Min.   :3.000   Min.   :1.000  
##  1st Qu.:0.0000   1st Qu.:3.000   1st Qu.:2.000  
##  Median :0.0000   Median :4.000   Median :2.000  
##  Mean   :0.4062   Mean   :3.688   Mean   :2.812  
##  3rd Qu.:1.0000   3rd Qu.:4.000   3rd Qu.:4.000  
##  Max.   :1.0000   Max.   :5.000   Max.   :8.000
```

--- .class #id 

## Regression model

#### Estimate the relationship the exists between the dependent variable and exploratory variable

```
## 
## Call:
## glm(formula = mpg ~ ., data = mtcars)
## 
## Deviance Residuals: 
##     Min       1Q   Median       3Q      Max  
## -3.4506  -1.6044  -0.1196   1.2193   4.6271  
## 
## Coefficients:
##             Estimate Std. Error t value Pr(>|t|)  
## (Intercept) 12.30337   18.71788   0.657   0.5181  
## cyl         -0.11144    1.04502  -0.107   0.9161  
## disp         0.01334    0.01786   0.747   0.4635  
## hp          -0.02148    0.02177  -0.987   0.3350  
## drat         0.78711    1.63537   0.481   0.6353  
## wt          -3.71530    1.89441  -1.961   0.0633 .
## qsec         0.82104    0.73084   1.123   0.2739  
## vs           0.31776    2.10451   0.151   0.8814  
## am           2.52023    2.05665   1.225   0.2340  
## gear         0.65541    1.49326   0.439   0.6652  
## carb        -0.19942    0.82875  -0.241   0.8122  
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## (Dispersion parameter for gaussian family taken to be 7.023544)
## 
##     Null deviance: 1126.05  on 31  degrees of freedom
## Residual deviance:  147.49  on 21  degrees of freedom
## AIC: 163.71
## 
## Number of Fisher Scoring iterations: 2
```




--- .class #id 


## Residual Summary

![plot of chunk unnamed-chunk-3](assets/fig/unnamed-chunk-3-1.png) 

```
## Error in eval(expr, envir, enclos): object '.class' not found
```
