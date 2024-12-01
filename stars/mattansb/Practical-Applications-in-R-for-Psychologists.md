---
project: Practical-Applications-in-R-for-Psychologists
stars: 126
description: Lesson files for Practical Applications in R for Psychologists.
url: https://github.com/mattansb/Practical-Applications-in-R-for-Psychologists
---

Practical Applications in R for Psychologists
=============================================

  

_Last updated 2023-09-03._

This Github repo contains all lesson files for _Practical Applications in R for Psychologists_. The goal is to impart students with the basic tools to process data, describe data (w/ summary statistics and plots), and the foundations of **building, evaluating and comparing statistical models in `R`**, focusing on linear regression modeling (using both frequentist and Bayesian approaches).

These topics were taught in the graduate-level course _**Advanced Research Methods for Psychologists**_ (Psych Dep., Ben-Gurion University of the Negev), laying the foundation for the following topic-focused courses:

-   Hierarchical linear models (_HLM_)
-   Machine Learning (_ML_)
-   Structural equation modelling (_SEM_)
-   Analysis of Factorial Designs (_ANOVA_)

**Notes:**

-   This repo contains only materials relating to _Practical Applications in R_. Though statistics are naturally discussed in many lessons, the focus is generally on the application and not on the theory.
-   Please note that some code does not work _on purpose_ and without warning, to force students to learn to debug.

Setup
-----

You will need:

1.  A fresh installation of **`R`** (preferably version 4.1.1 or above).
2.  RStudio IDE (optional, but recommended).
3.  The following packages, listed by lesson:

Lesson

Packages

01 intro

02 data wrangling

**`haven`**, **`tidyverse`**, **`readxl`**, **`dplyr`**, **`datawizard`**, **`summarytools`**, **`parameters`**, **`psych`**, **`finalfit`**, **`Hmisc`**, **`mice`**

03 plotting

`dplyr`, **`ggplot2`**, **`ragg`**, **`tidyr`**

04 hypothesis testing and power

**`effectsize`**, **`correlation`**, **`BayesFactor`**, `dplyr`, **`pwr`**, `ggplot2`

05 regression 101

`effectsize`, `parameters`, **`performance`**, **`ggeffects`**, **`psychTools`**

06 categorical predictors and model comparison

`dplyr`, `parameters`, **`emmeans`**, `ggeffects`, **`bayestestR`**, `performance`

07 moderation and curvilinear

`dplyr`, `datawizard`, `parameters`, `performance`, `bayestestR`, `emmeans`, `ggeffects`, `ggplot2`, **`modelbased`**

08 generalized linear models

`dplyr`, `parameters`, `performance`, `ggeffects`, `emmeans`, **`marginaleffects`**

09 assumption checks and violations

`ggeffects`, `performance`, **`see`**, **`bayesplot`**, **`qqplotr`**, `datawizard`, **`permuco`**, `parameters`, **`insight`**

10 ANOVA

**`afex`**, `emmeans`, `effectsize`, `ggeffects`, `tidyr`

11 mediation

**`mediation`**, **`tidySEM`**

_(Bold denotes the first lesson in which the package was used.)_

You can install all the packages used by running:

```
# in alphabetical order:

pkgs <- c(
  "afex", "BayesFactor", "bayesplot", "bayestestR", "correlation",
  "datawizard", "dplyr", "effectsize", "emmeans", "finalfit", "ggeffects",
  "ggplot2", "haven", "Hmisc", "insight", "marginaleffects", "mediation",
  "mice", "modelbased", "parameters", "performance", "permuco",
  "psych", "psychTools", "pwr", "qqplotr", "ragg", "readxl", "see",
  "summarytools", "tidyr", "tidySEM", "tidyverse"
)

install.packages(pkgs, repos = c("https://easystats.r-universe.dev", getOption("repos")))
```

_Package Versions_

Run on Windows 11 x64 (build 22621), with R version 4.3.1.

The packages used here:

-   `afex` 1.3-0 (_CRAN_)
-   `BayesFactor` 0.9.12-4.4 (_CRAN_)
-   `bayesplot` 1.10.0 (_CRAN_)
-   `bayestestR` 0.13.1.2 (_Local version_)
-   `correlation` 0.8.4 (_CRAN_)
-   `datawizard` 0.8.0.7 (_Local version_)
-   `dplyr` 1.1.2 (_CRAN_)
-   `effectsize` 0.8.5 (_Local version_)
-   `emmeans` 1.8.7 (_CRAN_)
-   `finalfit` 1.0.6 (_CRAN_)
-   `ggeffects` 1.3.0.5 (_Github: strengejacke/ggeffects_)
-   `ggplot2` 3.4.3 (_CRAN_)
-   `haven` 2.5.3 (_CRAN_)
-   `Hmisc` 5.1-0 (_CRAN_)
-   `insight` 0.19.3.3 (_Github: easystats/insight_)
-   `marginaleffects` 0.13.0 (_CRAN_)
-   `mediation` 4.5.0 (_CRAN_)
-   `mice` 3.16.0 (_CRAN_)
-   `modelbased` 0.8.6 (_CRAN_)
-   `parameters` 0.21.1 (_CRAN_)
-   `performance` 0.10.4 (_CRAN_)
-   `permuco` 1.1.2 (_CRAN_)
-   `psych` 2.3.6 (_CRAN_)
-   `psychTools` 2.3.6 (_CRAN_)
-   `pwr` 1.3-0 (_CRAN_)
-   `qqplotr` 0.0.6 (_CRAN_)
-   `ragg` 1.2.5 (_CRAN_)
-   `readxl` 1.4.3 (_CRAN_)
-   `see` 0.8.0.2 (_Local version_)
-   `summarytools` 1.0.1 (_CRAN_)
-   `tidyr` 1.3.0 (_CRAN_)
-   `tidySEM` 0.2.4 (_CRAN_)
-   `tidyverse` 2.0.0 (_CRAN_)
