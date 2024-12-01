---
project: mne-rsa
stars: 58
description: Representational Similarity Analysis on MEG and EEG data
url: https://github.com/wmvanvliet/mne-rsa
---

Representational Similarity Analysis
------------------------------------

This is a Python package for performing representational similarity analysis (RSA) using MNE-Python data structures. The RSA is computed using a “searchlight” approach.

Read more on RSA in the paper that introduced the technique:

Nikolaus Kriegeskorte, Marieke Mur and Peter Bandettini (2008). Representational similarity analysis - connecting the branches of systems neuroscience. Frontiers in Systems Neuroscience, 2(4). https://doi.org/10.3389/neuro.06.004.2008

Installation
------------

The package can be installed either through PIP: `pip install mne-rsa` or through conda using the conda-forge channel: `conda install -c conda-forge mne-rsa`

Use cases
---------

This is what the package can do for you:

-   Compute RDMs on arbitrary data
-   Compute RDMs in a searchlight across:
    -   vertices/voxels and samples (source level)
    -   sensors and samples (sensor level)
    -   vertices/voxels only (source level)
    -   sensors only (sensor level)
    -   samples only (source and sensor level)
-   Use cross-validated distance metrics when computing RDMs
-   And of course: compute RSA between RDMs

Supported metrics for comparing RDMs:

-   Spearman correlation (the default)
-   Pearson correlation
-   Kendall’s Tau-A
-   Linear regression (when comparing multiple RDMs at once)
-   Partial correlation (when comparing multiple RDMs at once)

Juicy bits of the API
---------------------

compute\_rdm(data, metric\='correlation', \*\*kwargs)

rsa\_stcs(stcs, rdm\_model, src, spatial\_radius\=0.04, temporal\_radius\=0.1,
         stc\_rdm\_metric\='correlation', stc\_rdm\_params\=dict(),
         rsa\_metric\='spearman', y\=None, n\_folds\=1, sel\_vertices\=None,
         tmin\=None, tmax\=None, n\_jobs\=1, verbose\=False)

rsa\_evokeds(evokeds, rdm\_model, noise\_cov\=None, spatial\_radius\=0.04,
            temporal\_radius\=0.1, evoked\_rdm\_metric\='correlation',
            evoked\_rdm\_params\=dict(), rsa\_metric\='spearman', y\=None,
            n\_folds\=1, picks\=None, tmin\=None, tmax\=None, n\_jobs\=1,
            verbose\=False)

rsa\_epochs(epochs, rdm\_model, noise\_cov\=None, spatial\_radius\=0.04,
           temporal\_radius\=0.1, epochs\_rdm\_metric\='correlation',
           epochs\_rdm\_params\=dict(), rsa\_metric\='spearman', y\=None,
           n\_folds\=1, picks\=None, tmin\=None, tmax\=None, n\_jobs\=1,
           verbose\=False)

rsa\_nifti(image, rdm\_model, spatial\_radius\=0.01,
          image\_rdm\_metric\='correlation', image\_rdm\_params\=dict(),
          rsa\_metric\='spearman', y\=None, n\_folds\=1, roi\_mask\=None,
          brain\_mask\=None, n\_jobs\=1, verbose\=False)

Example usage
-------------

Basic example on the EEG “kiloword” data:

import mne
import rsa
data\_path \= mne.datasets.kiloword.data\_path(verbose\=True)
epochs \= mne.read\_epochs(data\_path + '/kword\_metadata-epo.fif')
\# Compute the model RDM using all word properties
rdm\_model \= rsa.compute\_rdm(epochs.metadata.iloc\[:, 1:\].values)
evoked\_rsa \= rsa.rsa\_epochs(epochs, rdm\_model,
                            spatial\_radius\=0.04, temporal\_radius\=0.01,
                            verbose\=True)

Documentation
-------------

For quick guides on how to do specific things, see the examples.

Finally, there is the API reference documentation.

Integration with other packages
-------------------------------

I mainly wrote this package to perform RSA analysis on MEG data. Hence, integration functions with MNE-Python are provided. There is also some integration with nipy for fMRI.

Performance
-----------

This package aims to be fast and memory efficient. An important design feature is that under the hood, everything operates on generators. The searchlight routines produce a generator of RDMs which are consumed by a generator of RSA values. Parallel processing is also supported, so you can use all of your CPU cores.

Development
-----------

Here is how to set up the package as a developer:

git clone git@github.com:wmvanvliet/mne-rsa.git
cd mne-rsa
python setup.py develop --user

.. toctree::
   :hidden:

   Examples <auto\_examples/index>
   API Reference <api>
