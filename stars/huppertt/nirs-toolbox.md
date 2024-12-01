---
project: nirs-toolbox
stars: 91
description: Toolbox for fNIRS analysis
url: https://github.com/huppertt/nirs-toolbox
---

nirs-toolbox
============

The Github repository for the AnalyzIR Toolbox

The NIRS toolbox is s a Matlab based analysis program for NIRS that focuses on statistical analysis for functional and resting state studies. Developed an maintained by Dr. Ted Huppert's lab at University of Pittsburgh. http://huppertlab.net/nirs-toolbox-2/

And can be sited as: Santosa, H., Zhai, X., Fishburn, F., & Huppert, T. (2018). The NIRS brain AnalyzIR toolbox. Algorithms, 11(5), 73.

In order to get started with nirs toolbox first install Matlab and use github to download the latest release of nirs-toolbox. Then add the directories to Matlab

Add directories to the Matlab Path
----------------------------------

```
Note folders that start with “+”
(e.g. /+nirs) denote Matlab namespaces
and cannot be added directly to the
path. You must add the parent folder
containing this namespace.
```

1.  Add folder /nirs-toolbox
    
2.  Add with Subfolders /nirs-toolbox/external /nirs-toolbox/demos
    

Tutorial
--------

A full tutorial on nirs-toolbox is available here: http://huppertlab.net/wp-content/uploads/2018/05/1.1\_Intro\_Toolbox.pdf

Demos
-----

The toolbox includes several demos. Click below for a full walk through of some of these demos.

### fnirs\_analysis.m

http://huppertlab.net/auto-draft/ A demo that shows the basic structure of the toolbox and introduces the data, probe, and channelStats classes. This shows a basic first level statistical analysis. Data is downloaded from the web for the example.

### code\_testing\_demo.m

http://huppertlab.net/code\_testing\_demo-m/ This demo shows how to do regression testing of the toolbox’s main data types. This also demonstrates the built in receiver-operator-characteristic (ROC) analysis tools.

### compare\_software\_demo.m

http://huppertlab.net/compare\_software\_demo-m/ (Not yet completed) This demo takes data through HOMER, AR-IRLS, and NIRS-SPM tools to compare the sensitivity and specificity of the GLM statistics.
