ymd("character")
mdy("March 12, 1975")
dmy(25081985)
depart<-nyc+days(2)
arrive <- with_tz(arrive, tzone ="Asia/Hong_Kong")
last_time <- mdy("June 17, 2008", tz = "Singapore")
how_long<-interval(last_time, arrive)
as.period(how_long)


ymd_hms(dt1)
hms("03:22:14")
update(this_moment, hours = 8, minutes = 34, seconds = 55) changes some components
now("America/New_York")

stopwatch()
