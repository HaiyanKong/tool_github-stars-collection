---
project: mne-nirs
stars: 86
description: Process Near-Infrared Spectroscopy Data in MNE
url: https://github.com/mne-tools/mne-nirs
---

MNE-NIRS: Near-Infrared Spectroscopy Analysis
=============================================

**MNE-NIRS** is an MNE-Python compatible near-infrared spectroscopy processing package.

MNE-Python provides support for fNIRS analysis, this package extends that functionality and adds GLM analysis, helper functions, additional algorithms, data quality metrics, plotting, and file format support.

Documentation
-------------

Documentation for this project is hosted here.

You can find a list of examples within the documentation.

Features
--------

MNE-NIRS and MNE-Python provide a wide variety of tools to use when processing fNIRS data including:

-   Loading data from a wide variety of devices, including SNIRF files.
-   Apply 3D sensor locations from common digitisation systems such as Polhemus.
-   Standard preprocessing including optical density calculation and Beer-Lambert Law conversion, filtering, etc.
-   Data quality metrics including scalp coupling index and peak power.
-   GLM analysis with a wide variety of customisation including including FIR or canonical HRF analysis, higher order autoregressive noise models, short channel regression, region of interest analysis, etc.
-   Visualisation tools for all stages of processing from raw data to processed waveforms, GLM result visualisation, including both sensor and cortical surface projections.
-   Data cleaning functions including popular short channel techniques and negative correlation enhancement.
-   Group level analysis using (robust) linear mixed effects models and waveform averaging.
-   And much more! Check out the documentation examples and the API for more details.

Contributing
------------

Contributions are welcome (more than welcome!). Contributions can be feature requests, improved documentation, bug reports, code improvements, new code, etc. Anything will be appreciated. _Note_: this package adheres to the same contribution standards as MNE.

Acknowledgements
----------------

This package is built on top of many other great packages. If you use MNE-NIRS you should also acknowledge these packages.

MNE-Python: https://mne.tools/dev/overview/cite.html

Nilearn: http://nilearn.github.io/authors.html#citing

statsmodels: https://www.statsmodels.org/stable/index.html#citation

Until there is a journal article specifically on MNE-NIRS, please cite this article.

Docker
------

To start a jupyter lab server with a specified MNE-NIRS version, and mount a local directory on a mac or nix computer use:

docker run -p 8888:8888 -v \`pwd\`:/home/mne\_user ghcr.io/mne-tools/mne-nirs:v0.1.2 jupyter-lab --ip="\*"

Or on windows:

docker run -p 8888:8888 -v %cd%:/home/mne\_user ghcr.io/mne-tools/mne-nirs:v0.1.2 jupyter-lab --ip="\*"
