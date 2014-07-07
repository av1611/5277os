# R Data Structures


## Using Simple Data Types
## Integer 


```r
x <- 32
```


```r
x <- 32
32 -> x
```

## Numeric

```r
x <- 4.67
y <- 8.58
```

## Char


```r
myChar <- "a"
myName <- "John"
class(myChar)
```

```
## [1] "character"
```

```r
class(myName)
```

```
## [1] "character"
```



## Logical


```r
x <- 1
y <- 2
x < y
```

```
## [1] TRUE
```

## Complex

```r
x <- 2
y <- 3
z <- complex(real = x, imaginary = y)
z
```

```
## [1] 2+3i
```

## Creating datasets with vectors

## Creating simple vectors

```r
myFirstVector <- c (2, 14, 6, 17, 18, 9, 15, 25, 7, 11)
mean(myFirstVector)
```

```
## [1] 12.4
```

```r
n <- rep(2, 10) 
n <- rep(c(2, 5), 10)
seq(20)
```

```
##  [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
```

```r
seq(0, 20, 2)
```

```
##  [1]  0  2  4  6  8 10 12 14 16 18 20
```

```r
seq(from = 0, to = 20, by = 2)
```

```
##  [1]  0  2  4  6  8 10 12 14 16 18 20
```

```r
?seq
```

```
## starting httpd help server ... done
```

```r
seq(from = 1, to = 1, by = ((to - from)/(length.out - 1)), length.out = NULL, along.with = NULL, ...) 
```

```
## Error: '...' used in an incorrect context
```

```r
myCharacterVector <- c("a", "b", "c", "d", "e")
myStringVector <- c("apple", "grape", "pomegranate", "orange", "banana")
myCharacterVector <- c("a", "b", "c", "d", "e", 1, 2)
myCharacterVector
```

```
## [1] "a" "b" "c" "d" "e" "1" "2"
```

```r
myStringVector[1]
```

```
## [1] "apple"
```

```r
myStringVector[2]
```

```
## [1] "grape"
```

## Performing basic mathematic operations on vectors 

## Manipulating vectors with functions

## Storing characters and strings with vectors

## Matrices

### Creating a simple matrix

```r
myFirstMatrix <- matrix(1:20, 4, 5)
myFirstMatrix
```

```
##      [,1] [,2] [,3] [,4] [,5]
## [1,]    1    5    9   13   17
## [2,]    2    6   10   14   18
## [3,]    3    7   11   15   19
## [4,]    4    8   12   16   20
```

```r
myFirstMatrix <- matrix(1:20, nrow = 4, ncol = 5)
myFirstMatrix
```

```
##      [,1] [,2] [,3] [,4] [,5]
## [1,]    1    5    9   13   17
## [2,]    2    6   10   14   18
## [3,]    3    7   11   15   19
## [4,]    4    8   12   16   20
```

```r
myFirstMatrix <- matrix(1:20, nrow = 5, ncol = 4)
myFirstMatrix
```

```
##      [,1] [,2] [,3] [,4]
## [1,]    1    6   11   16
## [2,]    2    7   12   17
## [3,]    3    8   13   18
## [4,]    4    9   14   19
## [5,]    5   10   15   20
```

```r
myFirstMatrix <- matrix(1:20, 4, 5)
myFirstMatrix <- matrix(1:20, nrow = 4, ncol = 5)
myFirstMatrix <- matrix(1:20, 5, 4)
myFirstMatrix <- matrix(1:20, nrow = 5, ncol = 5)
```

### Combining vectors to create a matrix

```r
vector1 <- c(1:10)
vector2 <- c(101:110)
vector3 <- c(6:15)

matrix1 <- rbind(vector1, vector2, vector3)
matrix1
```

```
##         [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10]
## vector1    1    2    3    4    5    6    7    8    9    10
## vector2  101  102  103  104  105  106  107  108  109   110
## vector3    6    7    8    9   10   11   12   13   14    15
```

```r
matrix2 <- cbind(vector1, vector2, vector3)
matrix2
```

```
##       vector1 vector2 vector3
##  [1,]       1     101       6
##  [2,]       2     102       7
##  [3,]       3     103       8
##  [4,]       4     104       9
##  [5,]       5     105      10
##  [6,]       6     106      11
##  [7,]       7     107      12
##  [8,]       8     108      13
##  [9,]       9     109      14
## [10,]      10     110      15
```

```r
colnames(matrix2) <- c("column1", "column2", "column3")
rownames(matrix2) <- c(1:10)
matrix2
```

```
##    column1 column2 column3
## 1        1     101       6
## 2        2     102       7
## 3        3     103       8
## 4        4     104       9
## 5        5     105      10
## 6        6     106      11
## 7        7     107      12
## 8        8     108      13
## 9        9     109      14
## 10      10     110      15
```

```r
matrix5
```

```
## Error: object 'matrix5' not found
```

```r
matrix6 <- matrix(rep(11:25), 3, 5)
matrix6
```

```
##      [,1] [,2] [,3] [,4] [,5]
## [1,]   11   14   17   20   23
## [2,]   12   15   18   21   24
## [3,]   13   16   19   22   25
```

```r
matrix7 <- rbind(matrix5, matrix6)
```

```
## Error: object 'matrix5' not found
```

```r
matrix7
```

```
## Error: object 'matrix7' not found
```

### Combining matrices

```r
install.packages("gdata", dependencies=TRUE)
```

```
## Error: trying to use CRAN without setting a mirror
```

```r
library(gdata)
```

```
## gdata: Unable to locate valid perl interpreter
## gdata: 
## gdata: read.xls() will be unable to read Excel XLS and XLSX files
## gdata: unless the 'perl=' argument is used to specify the location
## gdata: of a valid perl intrpreter.
## gdata: 
## gdata: (To avoid display of this message in the future, please
## gdata: ensure perl is installed and available on the executable
## gdata: search path.)
## gdata: Unable to load perl libaries needed by read.xls()
## gdata: to support 'XLX' (Excel 97-2004) files.
## 
## gdata: Unable to load perl libaries needed by read.xls()
## gdata: to support 'XLSX' (Excel 2007+) files.
## 
## gdata: Run the function 'installXLSXsupport()'
## gdata: to automatically download and install the perl
## gdata: libaries needed to support Excel XLS and XLSX formats.
## 
## Attaching package: 'gdata'
## 
## The following object is masked from 'package:stats':
## 
##     nobs
## 
## The following object is masked from 'package:utils':
## 
##     object.size
```

```r
matrix2
```

```
##    column1 column2 column3
## 1        1     101       6
## 2        2     102       7
## 3        3     103       8
## 4        4     104       9
## 5        5     105      10
## 6        6     106      11
## 7        7     107      12
## 8        8     108      13
## 9        9     109      14
## 10      10     110      15
```

```r
dim(matrix2)
```

```
## [1] 10  3
```

```r
matrix2
```

```
##    column1 column2 column3
## 1        1     101       6
## 2        2     102       7
## 3        3     103       8
## 4        4     104       9
## 5        5     105      10
## 6        6     106      11
## 7        7     107      12
## 8        8     108      13
## 9        9     109      14
## 10      10     110      15
```

```r
dim(matrix3)
```

```
## Error: object 'matrix3' not found
```

```r
cbindX(matrix2, matrix3)
```

```
## Error: object 'matrix3' not found
```

### Selecting and extracting elements 

## Data frames

```r
dataFrame3 <- as.data.frame(matrix3)
```

```
## Error: object 'matrix3' not found
```

```r
View(dataFrame3)
```

```
## Error: object 'dataFrame3' not found
```

```r
setwd("C:/Dropbox/book")
```

```
## Error: cannot change working directory
```

```r
worms <- read.table("./worms.txt", header=T)
```

```
## Warning: cannot open file './worms.txt': No such file or directory
```

```
## Error: cannot open the connection
```

```r
names(worms)
```

```
## Error: object 'worms' not found
```

```r
worms[2, 2]
```

```
## Error: object 'worms' not found
```

```r
worms[2, ]
```

```
## Error: object 'worms' not found
```

```r
worms[order(worms$Soil.pH), ]
```

```
## Error: object 'worms' not found
```

```r
detach (worms)
```

```
## Error: invalid 'name' argument
```

```r
worms[Damp==T,]
```

```
## Error: object 'worms' not found
```

```r
worms[-(2:10),]
```

```
## Error: object 'worms' not found
```

```r
na.exclude(worms)
```

```
## Error: object 'worms' not found
```

```r
rbind.fill(mtcars[c("mpg", "wt")], mtcars[c("wt", "cyl")])
```

```
## Error: could not find function "rbind.fill"
```


## Apply functions family
### Apply

```r
matrix8 <- matrix(c(1:20, 41:60), nrow = 10, ncol = 2)
View(matrix8)
apply(matrix8, 1, mean)
```

```
##  [1]  6  7  8  9 10 11 12 13 14 15
```

```r
apply(matrix8, 2, mean)
```

```
## [1]  5.5 15.5
```

```r
apply(matrix8, 1:2, function(x) {sqrt(x) } )
```

```
##        [,1]  [,2]
##  [1,] 1.000 3.317
##  [2,] 1.414 3.464
##  [3,] 1.732 3.606
##  [4,] 2.000 3.742
##  [5,] 2.236 3.873
##  [6,] 2.449 4.000
##  [7,] 2.646 4.123
##  [8,] 2.828 4.243
##  [9,] 3.000 4.359
## [10,] 3.162 4.472
```

### Lapply

```r
myList <- list(a = 21:40, b = 31:50)
lapply(myList, sqrt)
```

```
## $a
##  [1] 4.583 4.690 4.796 4.899 5.000 5.099 5.196 5.292 5.385 5.477 5.568
## [12] 5.657 5.745 5.831 5.916 6.000 6.083 6.164 6.245 6.325
## 
## $b
##  [1] 5.568 5.657 5.745 5.831 5.916 6.000 6.083 6.164 6.245 6.325 6.403
## [12] 6.481 6.557 6.633 6.708 6.782 6.856 6.928 7.000 7.071
```


### Sapply

```r
sapply(myList, sqrt)
```

```
##           a     b
##  [1,] 4.583 5.568
##  [2,] 4.690 5.657
##  [3,] 4.796 5.745
##  [4,] 4.899 5.831
##  [5,] 5.000 5.916
##  [6,] 5.099 6.000
##  [7,] 5.196 6.083
##  [8,] 5.292 6.164
##  [9,] 5.385 6.245
## [10,] 5.477 6.325
## [11,] 5.568 6.403
## [12,] 5.657 6.481
## [13,] 5.745 6.557
## [14,] 5.831 6.633
## [15,] 5.916 6.708
## [16,] 6.000 6.782
## [17,] 6.083 6.856
## [18,] 6.164 6.928
## [19,] 6.245 7.000
## [20,] 6.325 7.071
```
## Plyr package

```r
set.seed(12)
d <- data.frame(year = rep(2000:2002, each = 3), count = round(runif(9, 0, 20)))
d <- data.frame(year = rep(2000:2002, each = 3), count = round(runif(9, 0, 20)))
print(d)
```

```
##   year count
## 1 2000     0
## 2 2000     8
## 3 2000    16
## 4 2001     8
## 5 2001     8
## 6 2001     5
## 7 2002     9
## 8 2002     9
## 9 2002    11
```

```r
library(plyr)
ddply(d, "year", function(x) {
      mean.count <- mean(x$count)
      sd.count <- sd(x$count)
      cv <- sd.count/mean.count
      data.frame(cv.count = cv)
     }
  )
```

```
##   year cv.count
## 1 2000   1.0000
## 2 2001   0.2474
## 3 2002   0.1195
```

```r
ddply(d, "year", summarise, mean.count = mean(count))
```

```
##   year mean.count
## 1 2000      8.000
## 2 2001      7.000
## 3 2002      9.667
```

```r
ddply(d, "year", transform, total.count = sum(count))
```

```
##   year count total.count
## 1 2000     0          24
## 2 2000     8          24
## 3 2000    16          24
## 4 2001     8          21
## 5 2001     8          21
## 6 2001     5          21
## 7 2002     9          29
## 8 2002     9          29
## 9 2002    11          29
```

```r
ddply(d, "year", mutate, mu = mean(count), sigma = sd(count), cv = sigma/mu)
```

```
##   year count    mu sigma     cv
## 1 2000     0 8.000 8.000 1.0000
## 2 2000     8 8.000 8.000 1.0000
## 3 2000    16 8.000 8.000 1.0000
## 4 2001     8 7.000 1.732 0.2474
## 5 2001     8 7.000 1.732 0.2474
## 6 2001     5 7.000 1.732 0.2474
## 7 2002     9 9.667 1.155 0.1195
## 8 2002     9 9.667 1.155 0.1195
## 9 2002    11 9.667 1.155 0.1195
```
