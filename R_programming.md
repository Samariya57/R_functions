#Library (dplyr)
##select() 
Select some columns with conditions from data.

select(data, column1:column5)

##filter()
Filter rows with conditions
filter(data, column1==5)

##arrange()
Sort data 
arrange(data, column1, desc(column2))

##mutate() 
Add a new column to data

mutate(data, column2=column1+5)

##summarize()
pack_sum <- summarize(by_package,
                      count = n(),
                      unique = n_distinct(ip_id),
                      countries = n_distinct(country),
                      avg_bytes = mean(size))
##tb1_df()

cran <- tbl_df(mydf)

##group_by()

by_package<-group_by(cran, package)
summarize(by_package, mean(size))

##quantile()
quantile(pack_sum$count, probs = 0.99)
top_counts<-filter(pack_sum, count>679)
View(top_counts)

## %>%

result3 <-
  cran %>%
  group_by(package) %>%
  summarize(count = n(),
            unique = n_distinct(ip_id),
            countries = n_distinct(country),
            avg_bytes = mean(size)
  ) %>%
  filter(countries > 60) %>%
  arrange(desc(countries), avg_bytes)

#library(lubridate)
##today()
year(), day(), month()
##wday()
wday(this_day, label=TRUE)
##now()
hour(), minute(), and second()
ymd(), dmy(), hms(), ymd_hms()

#Graphs
##summary()
##boxplot(data$column, col="blue")
abline(h=12)- horisontal line at level 12
abline(v=12, lwd=2) - vertical
boxplot(column1~column2, data=data, col="")
##barplot(table(data$column), col="", main="")
##hist(data$column, col="blue", breaks=100)
##with(polution, plot(latitude, pm25, col=column3))
##rug(data$column)
