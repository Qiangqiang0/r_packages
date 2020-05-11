# r_Packages

## 1. ggplot2

* color and fill
	* color: plot with color of curve

	* fill: plot filled with some color

	* try it inside the aes()

* geom_***
	* aes(): we could have data, color, and fill

* facet_wrap: separate graphs.

* facet_grid: one graph: one variable spread in one line or one row

```r
# histogram
ggplot(data=diamonds) + geom_histogram(aes(x=carat),fill="grey50")
ggplot(data=diamonds) + geom_histogram(aes(x=carat,fill=cut),fill="grey50")

# density
ggplot(data=diamonds) + geom_density(aes(x=carat),fill="grey50")

# point
g <- ggplot(data=diamonds,aes(x=carat,y=price))
g + geom_point(aes(color=color))

# 分面图
g + geom_point(aes(color=color)) + facet_wrap(~color)
g + geom_point(aes(color=color)) + facet_grid(cut~clarity)

# boxplot
ggplot(data=diamonds,aes(y=carat,x= 1)) + geom_boxplot()
ggplot(data=diamonds,aes(y=carat,x= cut)) + geom_boxplot()
       
# violine plot
ggplot(data=diamonds,aes(y=carat,x= cut)) + geom_violin(aes(color=cut,fill=cut))
ggplot(data=diamonds,aes(y=carat,x= cut)) + geom_violin(aes(color=cut,fill=cut)) + geom_point()
ggplot(data=diamonds,aes(y=carat,x= cut)) + geom_point() + geom_violin(aes(color=cut,fill=cut)) 

```

## 2. lubridate
