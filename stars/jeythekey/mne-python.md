---
project: mne-python
stars: 2
description: MNE : Magnetoencephalography (MEG) and Electroencephalography (EEG) in Python
url: https://github.com/jeythekey/mne-python
---

MNE-Python
----------

MNE-Python software is an open-source Python package for exploring, visualizing, and analyzing human neurophysiological data such as MEG, EEG, sEEG, ECoG, and more. It includes modules for data input/output, preprocessing, visualization, source estimation, time-frequency analysis, connectivity analysis, machine learning, and statistics.

### Documentation

MNE documentation for MNE-Python is available online.

### Installing MNE-Python

To install the latest stable version of MNE-Python, you can use pip in a terminal:

pip install -U mne

**Note** that MNE-Python 0.17 will be the last release to support Python 2. From MNE-Python 0.18, only Python 3 will be supported.

For more complete instructions and more advanced installation methods (e.g. for the latest development version), see the getting started page.

### Get the latest code

To install the latest version of the code using pip open a terminal and type:

pip install -U https://api.github.com/repos/mne-tools/mne-python/zipball/master

To get the latest code using git, open a terminal and type:

git clone git://github.com/mne-tools/mne-python.git

Alternatively, you can also download a zip file of the latest development version.

### Dependencies

The minimum required dependencies to run MNE-Python are:

-   Python >= 3.5
-   NumPy >= 1.11.3
-   SciPy >= 0.17.1

For full functionality, some functions require:

-   Matplotlib >= 1.5
-   Mayavi >= 4.6
-   PySurfer >= 0.8
-   Scikit-learn >= 0.18
-   NiBabel >= 2.1.0
-   Pandas >= 0.18
-   Picard >= 0.3
-   CuPy >= 4.0 (for NVIDIA CUDA acceleration)
-   DIPY >= 0.10.1

### Contributing to MNE-Python

Please see the documentation on the MNE-Python homepage:

https://martinos.org/mne/contributing.html

### Mailing list

http://mail.nmr.mgh.harvard.edu/mailman/listinfo/mne\_analysis

### Licensing

MNE-Python is **BSD-licenced** (3 clause):

> This software is OSI Certified Open Source Software. OSI Certified is a certification mark of the Open Source Initiative.
> 
> Copyright (c) 2011-2017, authors of MNE-Python. All rights reserved.
> 
> Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
> 
> -   Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
> -   Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
> -   Neither the names of MNE-Python authors nor the names of any contributors may be used to endorse or promote products derived from this software without specific prior written permission.
> 
> **This software is provided by the copyright holders and contributors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. In no event shall the copyright owner or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.**
