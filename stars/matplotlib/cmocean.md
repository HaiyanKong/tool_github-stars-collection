---
project: cmocean
stars: 233
description: Colormap setup for standardizing commonly-plotting oceanographic variables.
url: https://github.com/matplotlib/cmocean
---

cmocean
=======

Documentation available: http://matplotlib.org/cmocean/.

We have a paper with guidelines to colormap selection for your application and a description of the `cmocean` colormaps: Thyng, K. M., Greene, C. A., Hetland, R. D., Zimmerle, H. M., & DiMarco, S. F. (2016). True colors of oceanography. Oceanography, 29(3), 10. link: http://tos.org/oceanography/assets/docs/29-3\_thyng.pdf

Besides Python, the cmocean colormaps are also available:

-   For MATLAB by Chad Greene
-   For R cmocean, which includes ggplot2 compatible functions. Also included in Oce: an oceanographic analysis package by Dan Kelley and Clark Richards.
-   For Julia, included in Plots.jl and Makie.jl
-   For Ocean Data Viewer
-   For Generic Mapping Tools (GMT) at cpt-city and on github
-   For Paraview inspired by Phillip Wolfram
-   In Plotly
-   Chad Greene's Antarctic Mapping Tools in Matlab uses `cmocean`
-   For Tableau as a preferences file on github
-   For ImageJ as LUTs
-   For ncview via ncmaps.
-   For SeaDAS, and should work with BEAM/SNAP as well.

To install: `pip install cmocean`

To install with Anaconda: `conda install -c conda-forge cmocean`

If you want to be able to use the `plots` submodule, you can instead install with:

`pip install "cmocean[plots]"`

which will also install `viscm` and `colorspacious`.
