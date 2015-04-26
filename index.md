---
title       : Predicting Gas Mileage Per Gallon
subtitle    : Using Car Weight, Number of Engine, Transmission Type and Horsepower
author      : Myself
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Available Data

Standard R distributions typically include the "***mtcars***" dataset. It contains data on 32 automobile models from 1973-1974.
<p>
There are three attributes that are of interest for this study:
* wt - weight of the car in U.S. tons
* cyl - number of cylinders in the car's engine
* mpg - gas mileage (U.S. miles per U.S. gallon)

--- .class #id 

## The Model

We can easily create a linear model to estimate gas mileage given
a car's weight and the number of cylinders in its engine:

```{r}
model <- lm(mpg ~ wt + cyl, data=mtcars)
model
```

--- .class #id 

## Results

```{r}
model.summary <- summary(model)
model.summary[4]  # coeffecients
model.summary[8]  # r-squared
```

The model isn't great, but it's good enough for us to play with.

--- .class #d

## Interactive Demonstration

The following link provides an interactive demonstration of this model:   
http://jerrymcummings.shinyapps.io/developing-data-products   

You will be able to set the number of cylinders and the weight of
the car and see where the resulting predicted mileage fits in with
the rest of the cars.

<img src="/home/jerrymcummings/projects/coursera-developing-data-products/shiny.png" height="350px"/>