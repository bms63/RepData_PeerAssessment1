# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
setwd("C:/Users/Owner/Desktop/Repro Research")
list.files()
```

```
## [1] "activity.csv"            "Knitr Demo.Rmd"         
## [3] "Knitr_Demo.html"         "Project1.R"             
## [5] "R Markdown Demo.Rmd"     "R_Markdown_Demo.html"   
## [7] "RepData_PeerAssessment1" "Spam.R"
```

```r
library("dplyr")
```

```
## 
## Attaching package: 'dplyr'
## 
## The following object is masked from 'package:stats':
## 
##     filter
## 
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

```r
library(ggplot2)

activity = read.csv("activity.csv")

new_activity = na.omit(activity)

new_activity <- new_activity[which(new_activity$steps > 0),]

new_activity <- tbl_df(new_activity)

by_date <- group_by(new_activity, date)
```


## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
