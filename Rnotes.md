# R week 2
## History of R

- S, john Chambers, Bell Labs
- 1976 was a statistical analysis environment
- 1988 rewritten in C
- 1998 version 4 is current
- M&A statsci>insightfulcorp?alcatel>Lucent

- R, Ross Ihaka/Robert Gentlemen, New Zealand
- 1993, R released
- 2000, 1.00, 2013 3.0.2
- free, lean (modular packages), graphics, community pro
- 40yrold tech, physical memory storage

## R console input and evaluation

> x<-1 ## assigning 1 to x

> msg<-"hello" ## character vector "hello" assigned to msg

> print(x) ## should print 1

> x ## print is explicit in R, should print 1

> x <- 1:20 ## creates a sequence of 20!

## Data types - R objects and attributes

**R has five basic classes of objects**
- character
- numeric (real numbers)
- integer
- complex
- logical (true/false)

The most basic object is a vector
- A vector can only contain objects of the same class (exception "list")
- 1L should give an integer whereas 1 is numeric
- inf and NaN

**Attributes**
Objects can have attributes
- names, dimnames
- dimensions (matrices, arrays)
- class
- length
- other user-defined attributes/metadata
Attributes of an object can be accessed using the "attributes()" function.

## Data types, vectors and lists

> x <- c(0.5, 0.6) ## numeric

> x <- c(TRUE, FALSE) ## logical

> x <- c(T, F)          ## logical

> x <- c("a", "b", "c") ## character

> x <- 9:29 ## integer

> x <- c(1+0i, 2+4i)    ## complex

> x <- vector("numeric", length = 10)

> x 

[1] 0 0 0 0 0 0 0 0 0 0 

> x <- c(1.7, "a")      ## character, coercion

> x <- c(TRUE, 2)       ## numeric, coercion,

> x <- c("a", TRUE)     ## character, coercion

> as.numeric(x) ## converts x to numeric

> as.character(x)

> as.logical(x)

> class(x) ## prints variable class

> x <- c("a", "b", "c")

> as.numeric(x) ## nonsensical coercion results in NAs

> x <- list(1, "a", TRUE, 1+4i) ## lists are a vector that can contain multiple classes

> x
