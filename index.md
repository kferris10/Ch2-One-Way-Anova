---
title       : Ch 1 - T tests and CIs
subtitle    : Stat 217
framework   : bootstrap3        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [quiz, mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
layout      : deck3
assets      : 
  css       : 
    - "libraries/frameworks/bootstrap3/css/custom.css"
    - "libraries/frameworks/bootstrap3/css/moving_sidebar.css"
    - "http://fonts.googleapis.com/css?family=Vollkorn"
    - "http://fonts.googleapis.com/css?family=Droid%20Sans%20Mono"
---



## Introduction

In this activity ...

---
## The Insect Sprays Data

In an agricultural experiment, 72 plots of land were randomly assigned to be treated with one of six different insecticides.  The next day, the number of insects in each plot were counted.  We will test to see if there is a difference in the number of insects for at least one of the sprays.


```r
data(InsectSprays)  # load the data
boxplot(count ~ spray, data = InsectSprays)
```

<img src="assets/fig/insect-data-1.png" title="plot of chunk insect-data" alt="plot of chunk insect-data" style="display: block; margin: auto;" />


---
## The ACT Data
A school is interested in comparing ACT scores for students with baseball scholarships, football scholarships, and non-athletes.  Let Group 1 be the Baseball athletes, Group 2 be the non-athletes, and Group 3 be the Football athletes.  They want to know if one of the groups has different ACT scores from the other.  


```r
act <- read.csv("act-scores.csv", header = T)
```


| Baseball | Non.athletes | Football |
|:--------:|:------------:|:--------:|
|    25    |      21      |    22    |
|    22    |      27      |    21    |
|    19    |      29      |    24    |
|    25    |      26      |    27    |
|    24    |      30      |    19    |
|    25    |      27      |    23    |
|    24    |      26      |    17    |
|    23    |      23      |          |

--- &radio
## Some Information about the ACT Data

What are $n_1$, $n_2$, $n_3$?  How about $y_{12}$?

1. 7; 8; 8; 27
2. _8; 8; 7; 21_
3. 8; 7; 8; 25
4. 8; 8; 7; 25
5. 7; 8; 8; 22
*** .hint
What is the sample size of each group?  What is the value of the first observation in group 2?

*** .explanation
There are 8 observations in both the baseball and non-athletes groups, but only 7 in the football group.  The first row in the second column is $y_{12}$.




