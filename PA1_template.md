---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---

## Loading required libraries


```r
library(dplyr)
library(lubridate)
library(ggplot2)

# disable messages
knitr::opts_chunk$set(message = FALSE)
```

## Loading and preprocessing the data


```r
unzip("activity.zip", exdir = "data")
activity <- read.csv("data/activity.csv") %>% as_tibble()
activity <- activity %>% mutate(date = ymd(date))
head(activity)
```

```
## # A tibble: 6 x 3
##   steps date       interval
##   <int> <date>        <int>
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
```
The dates are parsed according to YYYY-MM-DD format.

## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
