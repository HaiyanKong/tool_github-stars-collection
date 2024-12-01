---
project: quarto-cv
stars: 80
description: A CV template for quarto
url: https://github.com/mps9506/quarto-cv
---

Quarto-cv Format
================

A Quarto template for generating a CV in pdf format. The template is based entirely on Steven Miller's R Markdown templates.

Installing
----------

System Requirements:

-   quarto >= 1.4
-   latex

quarto install extension mps9506/quarto-cv

This will install the template for use with existing Quarto projects or documents.

_or_ To install the extension and create an example qmd file and project (easiest way to start):

quarto use template mps9506/quarto-cv

If you need to use an old version of quarto, install a previous quarto-cv release:

quarto install extension mps9506/quarto-cv@v1.0.3

Usage
-----

To use with with quarto in the cli:

quarto render your\_cv.qmd --to quarto-cv.pdf

or specify in the document yaml:

format:
  quarto-cv-pdf: default

Format Options
--------------

### Contact Block

The contact block at the top of the CV is rendered using the following metadata:

author: First Name Last Name
address: Street, City, State, Country
# The following are optional
phone: your contact number
email: you@email.com
github: github account
orcid: orcid identfier
osf: five character osf id
twitter: twitter handle
web: web address (no \`https://\`)

### Bibliographies

The template includes a lua filter to easily incorporate multiple bibliographies using `.bib` files if you choose to manage publications this way. This is a good option for separating out book/chapter, journal articles, white papers, datasets, and software.

In the document yaml header simply point to your `.bib` files and provide a unique name:

bibliography:
  peer: peer.bib
  reports: reports.bib
  books: books.bib
  software: software.bib
validate-yaml: false

Note, that the `validate-yaml` key must be false in quarto because it expects a character value when it vaildates the yaml header.

Now create different bibliographies for each one:

```
# Journal Articles

::: {#refs-peer}
:::

# Software

::: {#refs-software}
:::
```

You can specify the bibliographic style using the csl variable. By default it points to an APA style sorted by descending date. Other styles can be found here.

### Fonts

The default font is EB Garamond. There are two primary methods for changing the font used. First you can use fonts provided through various LaTeX font packages using the `fontfamily:` yaml key. The `fontfamilyoptions:` can optionally be used in conjunction to set the LaTeX font package option. This is probably the easiest method if there is a package with the font you want to use.

fontfamily: electrum
fontfamilyoptions: lf

The second option is to point the `mainfont:` yaml key to a locally installed font.

mainfont: Ubuntu

Note that `fontfamily:` will override `mainfont:` so specify just one.

### Asian scripts

Support for Chinese, Japanese, and other Asian language characters are provided through the `xeCJK` package. The pdf will have to be rendered using xelatex instead of the default luatex:

title: CV
format:
  quarto-cv-pdf:
    pdf-engine: xelatex
CJKmainfont: Noto Sans CJK JP

The `CJKmainfont:` yaml key should point to a locally installed font.

Example
-------

Here is the source code for a minimal sample document: template.qmd.

License
=======

The template is based entirely on Steven Miller's R Markdown templates licensed under GPL-2. A copy of the pandoc `multibib` lua filter licensed under MIT is included as part of this template.

Release Notes
=============

dev
---

-   add support for fontawesome5 (thanks to @fecet #16).

v2.0.0
------

-   Update tex template for changes to citeproc in pandoc >=3.1.8 (Fixes #4).
-   Requires quarto >1.4.

v1.0.3
------

-   Add support for `xeCJK` (Fixes #9).

v1.0.2
------

-   Add user specified fonts (Fixes #7).

v1.0.1
------

-   Properly embed pandoc-ext `multibib` extension (Fixes #2).
-   Add CI test for pull requests on main.
-   Add .quartoignore to avoid copying extra files.
-   Fix README.md install instructions (@anielsen001) (#1).

v1.0.0
------

-   Initial Release
