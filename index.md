---
title       : Home Loan Pre-Qualification Letter Issuing Screening
subtitle    : 
author      : Jie Qin
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---
## Executive Summary
<h5> Background </h5>
The bank needs to have an automated webpage to make a quick decision on whether to issue a home loan pre-qualified letter for their customers for their home search
<h5> Factors to Determine the Qualification:</h5>
  <h8><p>FICO score: Has to be over 700</h8></p>
  <h8><p>Employment Status: Has to be full time employee</h8></p>
  <h8><p>Bankcrupcy Status: Never filing BK before</h8></p>
  <h8><p>Foreclosure Status: Never filing foreclosure before</h8></p>
 
---

## Process Steps
These 4 factors will be inputed by the customer. Then the application will take the values to make the decision based on a R function:

```{r echo=TRUE)
makeVector <-function(fico,EmpStatus,BKStatus,FCStatus){
  if (fico >=700 && EmpStatus=="Full time" && BKStatus=="No" && FCStatus=="No")
    {m <-"Congratulation, you have passed the screen. We will write a home loan pre-qualification letter for your new home search"}
  else {m <-"Sorry, we can write a home loan pre-qualification letter for your new home search"}
  return(m)
```


