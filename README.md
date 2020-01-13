1.we mainly use ArcMap to do the research.

2.Following R code is used to gererate the histogram of location quotient.

LSOA <- read.csv('finaltable.csv')
library(ggplot2)
histplot <- ggplot(data=LSOA, aes(x=LSOA$location_quotient)) 
                  +geom_histogram(colour = "black", fill = "white",binwidth = 0.2)
histplot + theme(axis.text=element_text(size=12),
                 axis.title=element_text(size=18)) + xlab('Location quotient') + ylab('Count')
summary(LSOA$location_quotient)
