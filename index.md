---
title       : Using Estimated Creatinine Clearance-Rate in Shiny
subtitle    : Coursera Developing Data Products project part 2
author      : Roy Chen
job         : Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [] # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

> 1. Shiny is a platform for providing an interactive R environment on a webpage.
> 2. Slidify is a convinient way of presenting materials from R onto slides.
> 3. Here I demonstrated a simple real-life application of using both shiny 
        and slidify.
> 4. In this shiny app, it computes the estimated creatinine clearance rate (eCcr) 
        based on the Cockcroft-Gault formula. 
> 5. It is a good estimation for the glomerular filtration rate, which is an 
        indication of kidney function.

--- .class #id 

## Estimated creatinine clearance rate

The estimated creatinine clearance rate (eCcr) is an estimate of one's 
glomerular filtration rate (GFR), which in turn, is a measure 
of one's kidney function. 
        
The calculation in this shiny demo interface is based on the 
Cockcroft-Gault formula.
        
It ultilizes the measurement of serum or plasma 
creatinine in computing the GFR, while adjusting 
for mass, sex, and age. The normal range of GFR is 100-130 mL/min.

The formula depends on whether the creatinine results is reported in units of 
umol/L or mg/dL.

--- .class #id

## cockcroft-Gault Formula

Units in umol/L:

eCcr = (140 - age) * weight * sex / creatine

Where sex is an adjustment factor (1.23 for male or 1.04 for female).


Units in mg/dL:

eccr = (140 - age) * weight * sex / (72 * creatinine)

Where sex is an adjustment factor (1 for male, and 0.85 for female).


As you can see, the formula can be a hassle to calculate, and that is where
the demo shiny app comes to the rescue.

--- .class #id

## Example of shiny app:

Example of codes:


```r
#library(shiny)
#runGitHub("Crazydiamond13/eccr")
#If you run this, it would fetch files hosted on my github
```


Please visit the site to try it out!

https://crazydiamond13.shinyapps.io/eccr/

