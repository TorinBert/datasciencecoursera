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

## Matrices

> m <- matrix(nrow = 2, ncol = 3) ## matrice, vector with dimension

> dim(m)
[1] 2 3

> attributes(m)
$dim
[1] 2 3

> m <- matrix(1:6, nrow = 2, ncol = 3) ## fills down columns from left to right

> m <- 1:10

> m 
[1] 1 2 3 4 5 6 7 8 9 10

> dim(m) <- c(2,5) ## m converts from a vector to a matrix

> x <- 1:3

> y <- 10:12

> cbind(x, y) ## fills 2x3 matrix by column top down (1 2 3, 10 11 12)
 
> rbind(x, y) ## fills 3x2 matrix by row left to right (1 2 3, 10 11 12)

## Data Types - Factors

- Factors used to represent categorical data
- Factors can be unordered or ordered
- Like an integer vector where each integer has a label
- Factors are treated specifically by modeling functions like lm() and glm()
Using factors with labels is *better* than using integers because factors are self-describing; having a variable that has values "male" and "female" is better than a variable that has values 1 and 2.

> x<- factor(c("yes", "yes", "yes", "yes", "no"))

> x
[1] yes yes yes yes no
Levels: no yes

> table(x) ## prints a table of no:1 yes:4

> unclass(x)
[1] 2 2 2 2 1
attr(,"levels")
[1] "no" "yes"

> x <- factor(c("yes, "no", "yes"), Levels = c("yes, "no"))

> x
[1] yes no yes
Levels: yes no

