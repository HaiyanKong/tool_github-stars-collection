---
project: rmdformats
stars: 725
description: HTML output formats for RMarkdown documents
url: https://github.com/juba/rmdformats
---

rmdformats
==========

> **Note for quarto users:** these templates are only suitable for RMarkdown documents. I published one quarto custom format called bookup which is a porting of the `robobook` template.

This R package provides ready-to-use HTML output formats and templates for RMarkdown documents. The goal is to produce clean documents "out of the box", with or without the RStudio IDE.

Formats gallery
---------------

The package provides several HTML output formats. Click on any image to see an HTML output sample.

### `downcute`

Taken from the docute project theme and its adaptation by John Coene. Responsive, with a dynamic table of contents and a dark theme switcher.

`downcute chaos` is a variation created by Zac Garland. It has a slightly different color theme, and defaults to dark mode. To use it, add a `downcute_theme: "chaos"` option in your YAML preamble.

### `robobook`

Adapted from the bookdown theme, with Roboto family fonts. Fully responsive with dynamic table of contents and collapsible navigation.

### `material`

Format taken from the Material design theme for Bootstrap 3. Document is split into pages at each `<h1>` header, and the table of contents allows an animated navigation between these pages (you can use the `cards: false` preamble parameter to disable the splitting and display all the cards at once).

### `readthedown`

Adapted from the corresponding `readtheorg` theme of the org-html-themes project, fully responsive with dynamic table of contents and collapsible navigation.

### `html_clean`

Simple and clean template with dynamic table of contents, very similar to the one from the great knitrBootstrap package by Jim Hester.

### `html_docco`

Simple template, no table of contents. CSS heavily inspired from the default one of the docco project.

### `lockdown`

`lockdown` is an exact copy of the default RMarkdown `html_document` template, with an added functionality : each time you click on a link to get out, you'll see a friendly reminder to wash your hands and wear a mask. Yes, it is a (bad) attempt at a (bad) joke, sorry !

Features and helpers
--------------------

### Features matrix

Responsive

Dynamic TOC

Dark mode

Thumbnails / Lightbox

Code folding

Tabsets

Bad joke

**html\_docco**

x

x

x

x

**html\_clean**

x

x

x

x

x

**readthedown**

x

x

x

x

**material**

x

x

x

**robobook**

x

x

x

x

x

**downcute**

x

x

x

x

x

x

**lockdown**

x

### Helpers

The package also provides RStudio document templates to easily generate an empty and ready to use rmarkdown file with several configuration directives.

It also provides the `pilltabs()` helper function, which allows to display a crosstab dynamically. See one of the output samples for a live example.

Installation
------------

You can install the latest stable release from CRAN :

install.packages("rmdformats")

Or the latest development snapshot from GitHub :

install.packages(remotes)  # if necessary
remotes::install\_github("juba/rmdformats")

Creating a new document
-----------------------

Just create a new `Rmd` file and add the following in your YAML preamble :

\---
output: rmdformats::<template name>
---

Within RStudio , you can also choose `File` > `New File...` > `R Markdown...`, then select `From Template`. You should then be able to create a new document from one of the package templates.

Options
-------

Depending on the features provided by the template, you can add the following options to your YAML preamble. Look at the template function help page for a valid list :

-   `fig_width` : figures width, in inches
-   `fig_height` : figures height, in inches
-   `fig_caption` : toggle figure caption rendering
-   `highlight` : syntax highlighting
-   `thumbnails` : if TRUE, display content images as thumbnails
-   `lightbox` : if TRUE, add lightbox effect to content images
-   `gallery` : if TRUE, add navigation between images when displayed in lightbox
-   `use_bookdown` : if TRUE, will use `bookdown` instead of `rmarkdown` for HTML rendering, thus providing section numbering and cross references.
-   `embed_fonts` : if `TRUE` (default), use local files for fonts used in the template instead of links to Google Web fonts. This leads to bigger files but ensures that the fonts are available
-   additional aguments are passed to the base `html_document` RMarkdown template

Example preamble :

\---
title: "My document"
date: "\`r Sys.Date()\`"
author: John Doe
output:
  rmdformats::downcute:
    self\_contained: true
    thumbnails: true
    lightbox: true
    gallery: false
    highlight: tango
---

Credits
-------

-   Magnific popup lightbox plugin
-   The CSS for the `html_docco` format is heavily inspired from the default one of the docco project.
-   The CSS and JavaScript for `readthedown` is adapted from the corresponding `readtheorg` theme of the org-html-themes project, which is itself inspired by the Read the docs Sphinx theme.
-   The CSS and JavaScript for `material` has been taken from the Material design theme for Bootstrap 3 project and its presentation page.
-   The CSS for `robobook` is directly derived from the bookdown project template.
-   The CSS for `downcute` is directly derived from the default theme of the docute project and its adaptation by John Coene for some of its projects documentation.
-   The `downcute chaos` theme has been created by Zac Garland.
-   JavaScript and HTML code for code folding and tabbed sections are taken from the RStudio's default `rmarkdown` HTML template.
-   The `html_clean` styling and features are very similar to the ones from the knitrBootstrap package by Jim Hester.
