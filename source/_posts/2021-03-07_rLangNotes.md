---
title: R Language Notes
tags:
  - R
  - Statistics
mathjax: true
abbrlink: 72aeab1e
date: 2021-03-07 21:03:25
---

**Abstract:** R is a common-used language especially for statistical analysis. I am a skilled user of python, NCL(Ncar Command Language), C Shell, and Fortran, but rarely use R. It is necessary to maintain such a post to note basic knowledge and tips for R.

<!-- more -->

# 1. Basics of R
## 1.1. Packages Management
There are two main mathods to install packages for R that using R function `install.packages('packages')` and using `conda install r-packages`.

When loading packages, both `require('package')` and `library('package')` are available. However, there is a essential difference between the two commands that `library()` will raise an error when the package is not available while `require()` merely returns `FALSE`. In other words, `library()` loads a package, and `require()` **tries** to load a package. Detailed discussion could be found in [What is the difference between require() and library()?](https://stackoverflow.com/questions/5595512/what-is-the-difference-between-require-and-library) and [library() vs require() in R](https://yihui.org/en/2014/07/library-vs-require/).

Some R packages are hard to install, I tried many times and finally succeeded. Here are instuctions:

```bash
# rgdal
$ conda install -c conda-forge r-rgdal 
```

## 1.2. Run R Scripts in Command Line
```bash
$ Rscript your_r_script.R
```

## 1.3. Arrays and Matrices 
```R
# Get dims of matrix
Dims <- dim(your_matrix)

# Get length of Array
Len <- length(your_array)
```

## 1.4. Loops
```R
for ()
```

## 1.5. String
```R
# combine strings
paste()
```

**References:**           
1. [R语言中字符串的拼接操作](https://blog.csdn.net/waple_0820/article/details/53171784)

# 2. Some Tips for R
## 2.1. Data IO
```R
# Read *.dbf data
library(foreign)

data <- read.dbf('your_dbf_data.dbf')

# Read *.nc data
data <- nc_open('your_nc_data.nc)
names(data$var)

PM25 <- ncvar_get( nc = data, varid = 'PM25')
PM10 <- ncvar_get( nc = data, varid = 'PM10')
```

**References:**          
1. [【R】R语言NC文件读写](https://www.jianshu.com/p/690f3e1f3ee0)

## 2.2. Date and Time
```R
# Create date seq
start_date = '2017-01-01'
ndays = 31
calendar = seq.Date(from=as.Date(start_date, format='%Y-%m-%d'), by='day', length.out=ndays)
calendar <- format(calendar, format="%Y%m%d")
calendarJ = seq.Date(from=as.Date(start_date, format='%Y-%m-%d'), by='day', length.out=ndays)
calendarJ <- format(calendarJ, format="%Y%j")
```

**References:**           
1. [R语言中生成日期序列](http://blog.sciencenet.cn/blog-247792-837263.html)