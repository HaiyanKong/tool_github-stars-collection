---
project: mne-ari
stars: 17
description: All-resolutions Inference for M/EEG in Python
url: https://github.com/john-veillette/mne-ari
---

MNE-ARI: All-resolutions Inference for M/EEG in Python.
=======================================================

Background
----------

The analysis of M/EEG data (or high dimensional data in general) frequently involves thousands of "mass univariate" statistical tests being performed at each channel/time/frequency in the interval of interest; without correction for mutliple comparisons, many spuriously significant results are expected. It is now standard to control the familywise error rate (FWER) using something like a cluster-based permutation test, which is now a standard inference method in popular open-source M/EEG analysis packages such as MNE, FieldTrip, EEGLAB, and Brainstorm, as well as in propriety softwares such as BESA.

Cluster-based approaches, while excellent at providing strong FWER control without sacrificing statistical power (accomplished by adapting to the autocorrelation structure of the data), lend themselves to misinterpretation (by no fault of their creators, who warn about this problem in their original paper and in their package documentation). The null hypothesis of a cluster-based permutation test pertains to whether the data from different conditions come from the same probability distribution over the _full range of data tested_ and not at any particular time/place/frequency; thus, the often used language "there is a significant cluster at ..." inappropriately conveys certainty about the extent of the effect. In fact, cluster-based tests don't control the error rate at the individual space/time/frequency level, and interpreting the extent of a cluster as the extent of an effect leads to large overestimates of the effect's true extent.

While the recommended language for talking about cluster-based permutation test results (e.g. "we rejected the null hypothesis on the basis of a cluster in area X, between time point A and B" instead of "we found a significant cluster in area X, between time point A and B") is more technically accurate, for some reason I doubt readers who aren't familiar with the method read too much into that nuance. Wouldn't it be nice if there was a way to identify clusters that _did_ provide error-rate guarantees for within-cluster inference?

Enter All-resolutions Inference (ARI), which does exactly that. ARI is a closed-testing procedure which obtains simultaneous confidence bounds for the false discovery proportion in all subsets of hypotheses, allowing for valid circular inference without falling prey to the inference problems of double-dipping that have plagued the neuroimaging field. ARI can be used to compute the true discovery proportion (TDP) of an unlimited number of candidate clusters, and if the TDP is sufficiently high, you can safely make claims like "we found a signficant effect in area X, between time point A and B," which will be both more interpretable to your readers and far more useful for subsequent replication attempts.

This package implements both parametric and permutation-based ARI, and is meant to be compatible with the MNE-Python ecosystem. So far as I know, it's the only implementation tailored to M/EEG data, though fMRI centric implementations are available in R and parametric ARI is now the default cluster inference method in Python's popular nilearn package for fMRI analysis. I believe this is the only permutation-based implementation outside of R. (Update: This is no longer true! Check out the sanssouci and PyPerm packages, which implement permutation-based approaches to post-hoc inference.)

Installation
------------

You can install a stable version using:

```
pip install mne-ari
```

Or you can install the latest version from Github using:

```
pip install git+https://github.com/john-veillette/mne-ari.git
```

Another option is to install using conda:

```
conda install -c conda-forge mne-ari
```

MNE-ARI is also included in the standalone MNE installers if you prefer an installation option with a GUI.

Usage
-----

Basic usage is as follows:

```
from mne_ari import all_resolutions_inference
p_vals, tdp, clusters = all_resolutions_inference(data, alpha = 0.05)
```

You can use the argument `ari_type = 'permutation'` or `'parametric'` to specify the type of ARI to use. `'permutation'` is the default, since it has better unit test coverage.

Check out the examples notebook for more advanced usage examples such as clustering, different data types/dimensions, and custom statistics functions.

Also read the docstring for `mne_ari.all_resolutions_inference`.

If you know what you're doing, feel free to use the lower-level APIs for parametric (`mne_ari.ari.parametric.ARI`) and permutation (`mne_ari.ari.permutation.pARI`) ARI, which implement multiple comparisons control without any of the cluster-identification stuff. (These classes are not really "low-level"; they're easy to use, just poorly documented. But they'll let you select subsets/clusters however you want or use ARI on arbitrary data, which is potentially handy.)

You can also check out this video recording (direct link) of a live tutorial given to the users of the National Institute of Health's MEG Core Facility. Check out MNE-ARI's tutorial and some of the other tutorials given to their journal club here!

Future
------

I hope to get to these improvements myself eventually, but I'm also open to contributions from the impatient.

-   Once I've used the package enough in my own projects to know if my design choices (e.g. default parameter settings) are sensible, I'll do some mild tweaking and a new release. Until then, you may need to play with parameters like the cluster `thresholds` in the `mne_ari.all_resolutions_inference` function a little more than you would otherwise (but that's fine, since ARI lets you try unlimited cluster selection criteria without invalidating your inference!).
-   Parametric ARI is polished and frequently cross-checked against nilearn's implementation for consistency. Permutation ARI has room for more features. For example, the permutation ARI paper described several families of candidate critical vectors, and I've currently only implemented the Simes-inspired family.
-   The Notip procedure does away with the need for paramtetric critical vector families altogether, which comes with an advantage in power, so that's definitely worth implementing.

References
----------

If you use ARI, please cite:

> Rosenblatt, J. D., Finos, L., Weeda, W. D., Solari, A., & Goeman, J. J. (2018). All-resolutions inference for brain imaging. Neuroimage, 181, 786-796.

And for the permutation-based version:

> Andreella, A., Hemerik, J., Weeda, W., Finos, L., & Goeman, J. (2020). Permutation-based true discovery proportions for fMRI cluster analysis. arXiv preprint arXiv:2012.00368.

And if you're using this package, please cite this code as well! There will be a DOI issued for each release, which will be displayed on a badge at the top of this README, so make sure you're using the DOI that matches the version you use. An example citation is:

> Veillette, J. P. (2022). MNE-ARI: All-Resolutions Inference For M/EEG in Python. doi:10.5281/zenodo.5813808
