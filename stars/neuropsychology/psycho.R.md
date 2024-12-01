---
project: psycho.R
stars: 145
description: An R package for experimental psychologists
url: https://github.com/neuropsychology/psycho.R
---

#### _Efficient and Publishing-Oriented Workflow for Psychological Science_

psycho
======

Name

psycho

Stable

Documentation

Blog

Examples

Questions

Authors

Reference

* * *

⚠️ **NOTE: This package is being deprecated in favour of the report package. Please check it out and ask for any missing features.**

* * *

Goal
----

The main goal of the `psycho` package is to provide tools for psychologists, neuropsychologists and neuroscientists, to facilitate and speed up the time spent on data analysis. It aims at supporting best practices by providing tools to format the output of statistical methods to directly paste them into a manuscript, ensuring standardization of statistical reporting.

Contribute
----------

**`psycho` is a young package in need of affection.** You can easily hop aboard the development of this open-source software and improve psychological science:

-   Need some help? Found a bug? Request a new feature? Just open an issue ☺️
-   Want to add a feature? Correct a bug? You're more than welcome to contribute!

Don't be shy, try to code and submit a pull request (PR). Even if unperfect, we will help you to make a great PR! All contributors will be very graciously rewarded. Someday.

Examples
--------

Check examples in the following vignettes:

-   Overview of the psycho package
-   Bayesian Analysis in Psychology

Or blog posts:

-   The end of errors in ANOVA reporting
-   Variable vs. Participant-wise Standardization
-   Formatted Correlation with Effect Size
-   Extracting a Reference Grid of your Data for Machine Learning Models Visualization
-   Copy/paste t-tests Directly to Manuscripts
-   Easy APA Formatted Bayesian Correlation
-   Fancy Plot (with Posterior Samples) for Bayesian Regressions
-   How Many Factors to Retain in Factor Analysis
-   Beautiful and Powerful Correlation Tables
-   Format and Interpret Linear Mixed Models
-   How to do Repeated Measures ANOVAs
-   Standardize (Z-score) a dataframe
-   Compute Signal Detection Theory Indices
-   Installing R, R Studio and psycho

General Workflow
----------------

The package revolves around the `psychobject`. Main functions from the package return this type, and the `analyze()` function transforms other R objects into psychobjects. Four functions can then be applied on a psychobject: `summary()`, `print()`, `plot()` and `values()`.

Installation
------------

-   To get the stable version from CRAN, run the following commands in your R console:

install.packages("psycho")
library("psycho")

-   To get the latest development version, run the following:

install.packages("devtools")
library("devtools")
install\_github("neuropsychology/psycho.R")
library("psycho")

Credits
-------

You can cite the package as following:

-   Makowski, (2018). _The psycho Package: an Efficient and Publishing-Oriented Workflow for Psychological Science_. Journal of Open Source Software, 3(22), 470. https://doi.org/10.21105/joss.00470

Contributors
------------

-   Viliam Simko
