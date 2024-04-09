# Introduction to Bayesian Statistics

**Date**: April 2024

**Author**: Aislinn Keogh

This two-class course will introduce you to working with Bayesian Statistics. Distinct from frequentist statistics, which is concerned with accepting or rejecting the null hypothesis, Bayesian Statistics asks what the probability of different hypotheses is, given the data and our prior beliefs about the world.

On this course, we will talk through the conceptual underpinnings of Bayesian Statistics, and give you hands-on practice fitting Bayesian models in R.

Learning outcomes:

- Understand how beliefs about the world are formalised
- See how different priors influence a model's estimates
- Get to grips with interpreting posterior distributions
- Familiarise yourself with the workflow for running a Bayesian analysis
- Practise fitting and inspecting Bayesian models using the `brms` package in R

The course will be split into two sessions:

- **Week 1:** Theoretical introduction to Bayesian Statistics
- **Week 2:** Hands-on practice fitting Bayesian models in R

This is an advanced-level course. We will assume that you are comfortable using R and RStudio, and familiar with linear regression models (e.g. in `lme4`). You may want to have a quick read through the following articles to refresh your memory on some relevant theoretical concepts:

- [Basics of probability theory](https://www.khanacademy.org/math/statistics-probability/probability-library/basic-theoretical-probability/a/probability-the-basics)
- [Overview of null hypothesis significance testing](https://www.ncl.ac.uk/webtemplate/ask-assets/external/maths-resources/animal-science/hypothesis-tests/introduction-to-hypothesis-testing-and-confidence-intervals.html)

## Setup instructions

Please make sure to follow these instructions **before** the course begins as we won't have time to troubleshoot installation problems during the classes.

First, please make sure you have the latest version of [R](https://cloud.r-project.org/) and the latest version of [RStudio](https://www.rstudio.com/products/rstudio/download/#download).

### R packages

Next, you'll need to install a few R packages. 
We're going to be using `brms`, which is an R interface to fit Bayesian models using a backend language called Stan. 
You don't need to know anything about Stan to use `brms`, and the syntax should be very familiar if you're used to `lme4`!
The `bayesplot` package has some nice built-in functions for visualising distributions.
If you don't already use `tidyverse`, you'll need to install that too; we'll be using it for general data wrangling.

Open RStudio and run the following in the Console:

```
install.packages("brms")
install.packages("bayesplot")
install.packages("tidyverse")
```

If you get any error messages for any of these installs that you can't resolve by googling, please post in the Teams group to get help.

### C++ compiler

You'll also need a C++ compiler (because `brms` internally creates Stan code which is translated to C++ and compiled afterwards). 

- **On Windows:** Install [RTools](https://cran.r-project.org/bin/windows/Rtools/rtools44/rtools.html), **ensuring that you tick the box to add RTools to the system PATH**, then run `system("g++ -v")` in the R Console
- **On macOS:** Install XCode from the App Store, then run `system("clang++ -v")` in the R Console

You should see a few lines of indecipherable system code in the Console. As long as you don't see any warnings or errors, you're good to go!

## Materials

We're going to be using this wonderful tutorial created by [Elizabeth Pankratz](https://elizabethpankratz.github.io/) for the theoretical introduction (Week 1): [Bayes, stat! (Day 1)](https://elizabethpankratz.github.io/bayes_stat/day1/learningobj.html). 

Materials for the practical, hands-on class will be posted in this repo ahead of Week 2.

[![License: CC BY-NC 4.0](https://licensebuttons.net/l/by-nc/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc/4.0/)