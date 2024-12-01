---
project: Case-Studies-Python
stars: 152
description: An introduction to the practicing neuroscientist to data analysis in Python
url: https://github.com/Mark-Kramer/Case-Studies-Python
---

Case-Studies-Python
===================

This repository is a companion to the textbook Case Studies in Neural Data Analysis, by Mark Kramer and Uri Eden. That textbook uses MATLAB to analyze examples of neuronal data. The material here is similar, except that we use Python.

The intended audience is the _practicing neuroscientist_ - e.g., the students, researchers, and clinicians collecting neuronal data in the hospital or lab. The material can get pretty math-heavy, but we've tried to outline the main concepts as directly as possible, with hands-on implementations of all concepts. We focus on only two main types of data: spike trains and electric fields (such as the local field potential \[LFP\], or electroencephalogram \[EEG\]). If you're interested in other data (e.g., calcium imaging, or BOLD), you may still find the examples indirectly useful (for example, demonstrations of how to compute and interpret a power spectrum of a signal).

This repository was created by Emily Schlafly and Mark Kramer, with important contributions from Dr. Anthea Cheung.

**Thank you to:**

-   MIT Press for publishing the MATLAB version of this material.
-   NIH NIGMS R25GM114827 and NSF DMS #1451384 for support.

* * *

Quick start to learning Python for neural data analysis:
--------------------------------------------------------

-   Visit the web-formatted version of the book.
-   Watch this 2 minute video.
-   Read and interact with the Python code in your web browser.

* * *

Slow start to learning Python for neural data analysis:
-------------------------------------------------------

There are multiple ways to interact with these notebooks.

-   **Simple**: Visit the web-formatted version of the notebooks.
    
-   **Intermediate**: Open a notebook in Binder and interact with the notebooks through a JupyterHub server. Binder provides an easy interface to interact with this material; read about it in eLife.
    
-   **Advanced**: Download the notebooks and run them locally (i.e. on your own computer) in Jupyter. You'll then be able to read, edit and execute the Python code directly in your browser and you can save any changes you make or notes that you want to record. You will need to install Python and we recommend that you configure a Python environment as well.
    

* * *

Install Python
--------------

We assume you have installed Python and can get it running on your computer. Some useful references to do so include,

-   Python.org
    
-   Miniconda
    
-   Anaconda
    

If this is your first time working with Python, using Anaconda is probably a good choice. It provides a simple, graphical interface to start Jupyter.

* * *

Configure Python
----------------

If you have never used the terminal before, consider using Anaconda Navigator, Anaconda's desktop graphical user interface (GUI).

Once you have installed Anaconda or Miniconda, we recommend setting up an environment to run the notebooks. If you downloaded the repository from Github, then you can run the commands below in your terminal to configure your local environment to match the Binder environment. If you have never used the terminal before, consider using Anaconda Navigator, Anaconda's desktop graphical user interface (GUI). The environment file we use on Binder is located in the `binder` folder.

```
# create environment <case-studies>
conda env create --file environment.yml
conda activate case-studies  # activate environment <case-studies>
make config  # configure jupyter in environment
```

This will ensure that you have all the packages needed to run the notebooks. Note that you can use `make clean` to remove the changes made during `make config`.

Finally, whenever you are ready to work with the notebooks, activate your environment and start Jupyter:

```
conda activate case-studies  # activate python environment
jupyter notebook  # start jupyter in the current location
```

If you prefer, you can use `jupyter lab` instead of `jupyter notebook`.

* * *

Contributions
-------------

We very much appreciate your contributions to this material. Contribitions may include:

-   Error corrections
-   Suggestions
-   New material to include (please start from this template).

There are two ways to suggest a contribution:

-   **Simple**: Visit Case Studies Python, locate the file to edit, and follow these instructions.
    
-   **Advanced**: Fork Case Studies Python and submit a pull request
