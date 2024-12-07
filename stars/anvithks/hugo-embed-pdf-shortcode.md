---
project: hugo-embed-pdf-shortcode
stars: 136
description: A shortcode for Hugo(https://gohugo.io/) which allows you to embed a PDF file in a page using Pdf.js (https://mozilla.github.io/pdf.js/)
url: https://github.com/anvithks/hugo-embed-pdf-shortcode
---

hugo-embed-pdf-shortcode
========================

* * *

Table of Contents
=================

-   Online Demo
-   Introduction
-   Setup
-   Usage
-   FAQ
-   Support
-   Who uses embed-pdf
-   License

* * *

Introduction
------------

\[Back to Top\]

This is a Hugo Shortcode developed for use in Hugo based websites. This shortcode allows you to embed a PDF file in a page on your Hugo website. It is developed using the PDF.js library by Mozilla.

Setup
-----

\[Back to Top\]

**Note:** This shortcode is for use in Hugo based websites. It will not work anywhere else.

Hugo embed-pdf can be installed in two ways.

### Method 1 - Install as a Git submodule

1.  Add this shortcode as a Git submodule

git submodule add  https://github.com/anvithks/hugo-embed-pdf-shortcode.git themes/hugo-embed-pdf-shortcode

1.  Edit `config.toml` as follows

```
theme = ["hugo-embed-pdf-shortcode", "YourCurrentTheme"]
enableInlineShortcodes = true
```

**To learn more about "Theme components", see the Hugo documentation**

* * *

### Method 2 - Clone this repository

1.  Clone this repository

  

git clone https://github.com/anvithks/hugo-embed-pdf-shortcode.git
cd hugo-embed-pdf-shortcode

1.  Copy the file `./layouts/shortcodes/embed-pdf.html` to `./layouts/shortcodes` in your Hugo website directory.

  

**Note:** If you do not have a `./layouts/shortcodes` directory you can create it.

cp ./layouts/shortcodes/embed-pdf.html /path/to/your/hugo/website/layouts/shortcodes

  

1.  Copy the pdf.js library files from `./static/js/pdf-js` to `./static/js` in your Hugo website directory.

  

**Note:** If you do not have a `./static/js` directory you can create it.

cp -R ./static/js/pdf-js /path/to/your/hugo/website/static/js/

* * *

Usage
-----

\[Back to Top\]

In your Hugo website place the following shortcode in any of the markdown pages.

```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" >}}

```

To hide pagination

```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" hidePaginator="true" >}}
```

To render a selected page number

```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" renderPageNum="5" >}}
```

To hide loading spinner

```
{{< embed-pdf url="./path/to/pdf/file/example.pdf" hideLoader="true" >}}
```

### Parameters

-   **url (required)** : The relative location of the file.
    
-   **hidePaginator (optional)**: Boolean which expects `true` or `false`. Hides the paginator for single page documents.
    
-   **renderPageNum (optional)**: Integer which expects any number from `1` up to the last page number in the document. Will render that specific page on initial load.
    
-   **hideLoader (optional)**: Boolean which expects `true` or `false`. Hides the loading spinner while your document loads.
    

  

**Note:** Currently supports local file embed. If absolute URL from the remote server is provided, configure the CORS header on that server.

FAQ
---

\[Back to Top\]

1.  I have installed hugo-embed-pdf in my website locally by cloning the repository and copying the files, but it does not work?  
    A. hugo-embed-pdf uses pdf.js from mozilla. Pdf.js is now being served using a CDN.  
    If you would like to use a local copy of PDf.js then you can make the following changes to the `embed-pdf.html` file.

-   Change the script tag at the top of the file from

<script src\="https://cdn.jsdelivr.net/npm/pdfjs-dist@3.4.120/build/pdf.min.js" integrity\="sha256-UZQVSEoMbJ82/3uFjt4mYOTVVHIImtkp7u3L6LMH6/Y=" crossorigin\="anonymous"\></script\>

**to**

<script type\="text/javascript" src\='{{"/js/pdf-js/build/pdf.js" | relURL}}'\></script\>

-   Change the path to the `pdf.worker.js` file at line number 124 from

pdfjsLib.GlobalWorkerOptions.workerSrc \= 'https://cdn.jsdelivr.net/npm/pdfjs-dist@3.4.120/build/pdf.worker.min.js';

**to**

pdfjsLib.GlobalWorkerOptions.workerSrc \= "{{.Site.BaseURL}}" + 'js/pdf-js/build/pdf.worker.js';

Support
-------

\[Back to Top\] You an reach me at:

-   Twitter : @anvith3

For any bugs, enhancement requests, feature requests please raise issues here

Who uses Hugo Embed Pdf Shortcode
---------------------------------

\[Back to Top\]

Dirk's Changelog  
SYSADMIN - Administration, security and hardening of Linux

License
-------

\[Back to Top\]

-   **MIT license**
