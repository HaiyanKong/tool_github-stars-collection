---
project: vitae
stars: 1231
description: R Markdown Résumés and CVs
url: https://github.com/mitchelloharawild/vitae
---

vitae
=====

_/ˈviːteɪ/_

Templates and tools for making a Résumé/CV
------------------------------------------

The _vitae_ package makes creating and maintaining a Résumé or CV with R Markdown simple. It provides a collection of LaTeX and HTML templates, with helpful functions to add content to the documents.

Installation
------------

You can install the **release** version from CRAN.

install.packages('vitae')

You can install the **development** version from GitHub.

# install.packages("remotes")
remotes::install\_github("mitchelloharawild/vitae")

This package requires LaTeX to be installed on your computer. If you’re encountering issues, please check that LaTeX is installed. The tinytex package makes it easy to setup LaTeX within R:

install.packages('tinytex')
tinytex::install\_tinytex()

Getting started
---------------

The _vitae_ package currently supports 6 popular CV templates. You can see some previews of the available templates below.

If you prefer a guided introduction in video form, check out Bryan Jenks’ freeCodeCamp tech talk:

Creating a new CV with `vitae` can be done using the RStudio R Markdown template selector:

These templates leverage the strength of rmarkdown to include common information in the YAML header (name, position, social links…) and extended information in the main body. The main body of the CV is written using markdown, and allows for data-driven generation of entries using the `*_entries` functions. This allows you to import your working history from other sources (such as ORCID, Google Scholar, or a maintained dataset), and include them programmatically into your CV.

Templates
---------

There are currently 6 templates available in this package:

**vitae::awesomecv**

**vitae::hyndman**

**vitae::latexcv**

**vitae::markdowncv**

**vitae::moderncv**

**vitae::twentyseconds**

Extending the package to add new templates is a somewhat simple process (details in the creating vitae templates vignette).

Examples of using vitae
-----------------------

-   Mitchell O’Hara-Wild
-   Rob Hyndman
-   Eric R. Scott
-   Nat Price
-   Sam Abbott (automatic deployment!)
-   JooYoung Seo (printing multiple bibliographic entries according to a given csl file)
-   Diogo M. Camacho
-   Han Zhang (custom csl files)
-   Bryan Jenks
-   Lorena Abad
-   Lampros Sp. Mouselimis (using Github Actions and a docker image to programmatically generate the CV file)
-   Adam Kirosingh
-   Marco Lombardi
-   Anthony Romero
-   André Calero Valdez This version uses a database to manage the content and automatically updates the content once a week using Github actions. PDF is then added as a release after rendering. Also uses a forked version of the package to remove the trailing dot in brief entries.

Add your vitae to the list using a PR.

* * *

Please note that the ‘vitae’ project is released with a Contributor Code of Conduct. By contributing to this project, you agree to abide by its terms.

The vitae project began as at rOpenSci’s OzUnconf 2018. A big thank you to rOpenSci and the event organisers for their work, which has played a big role in the formation of this package.
