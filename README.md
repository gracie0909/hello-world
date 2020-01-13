1.we mainly used ArcMap to do the research.
the birmingham.mxd is the ArcMap file of the final coursework.
other data containing gdb file and the original input data can be downloaded from the following link:
https://drive.google.com/open?id=1GSZ90Zp7NRO8AzdRn7f9EIumSb7leoX1


2.Following R code is used to gererate the histogram of location quotient.

LSOA <- read.csv('finaltable.csv')
library(ggplot2)
summary(LSOA$location_quotient)
histplot <- ggplot(data=LSOA, aes(x=LSOA$location_quotient)) 
                  +geom_histogram(colour = "black", fill = "white",binwidth = 0.2)
histplot + theme(axis.text=element_text(size=12),
                 axis.title=element_text(size=18)) 
                 + xlab('Location quotient') 
                 + ylab('Count')

