#library(datasets)
data(table)
with(table, plot(column1, column2))
with(subset(table, column1==5), points(column1, column2, col="blue"))
data1<-transform(data1, column=factor(column))
boxplot(column2!column, data1, xlab="" ,ylab="")
keys:
pch-plotting symbol
Ity-line type
lwd-line width
col-color
title - title
##par()-function for global graph parametrs
las-orientation of axis
bg-background color
mar-margin size
oma-outer margin
mfrow(mfcol)-number of plots per row


#library(lattice)
##state<- data.frame(state.x77,region=state.region)
xyplot(Life.exp~income|region, data=state, layout=c(4,1))

#library(ggplot2)
data(mgp)
qplot(displ, hwy, data=mpg)

##example(points)

##plot into file
pdf(file="file1.pdf")
plot()
dev.off() - close your device

dev.cur() - current devices
dev.copy (png, file="myfile.png")
