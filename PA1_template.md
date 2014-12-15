# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

```r
#unzip and read csv
unzip("activity.zip")
activity_data<-read.csv("activity.csv")

#Format date column into a date
activity_data$date<-as.Date(activity_data$date)
```

## What is mean total number of steps taken per day?

```r
#aggregate teh steps by date
mean_steps<-aggregate(steps~date, data=activity_data, sum, na.rm=TRUE)

hist(mean_steps$steps, main="Total Number of Steps taken per Day")
```

![](PA1_template_files/figure-html/meanofsteps-1.png) 

```r
#calculate the mean and media of the total steps
mean(mean_steps$steps)
```

```
## [1] 10766.19
```

```r
median(mean_steps$steps)
```

```
## [1] 10765
```

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
