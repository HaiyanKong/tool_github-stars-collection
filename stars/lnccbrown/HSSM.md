---
project: HSSM
stars: 82
description: Development of HSSM package
url: https://github.com/lnccbrown/HSSM
---

HSSM - Hierarchical Sequential Sampling Modeling
------------------------------------------------

### Overview

HSSM is a Python toolbox that provides a seamless combination of state-of-the-art likelihood approximation methods with the wider ecosystem of probabilistic programming languages. It facilitates flexible hierarchical model building and inference via modern MCMC samplers. HSSM is user-friendly and provides the ability to rigorously estimate the impact of neural and other trial-by-trial covariates through parameter-wise mixed-effects models for a large variety of cognitive process models. HSSM is a BRAINSTORM project in collaboration with the Center for Computation and Visualization and the Center for Computational Brain Science within the Carney Institute at Brown University.

-   Allows approximate hierarchical Bayesian inference via various likelihood approximators.
-   Estimate impact of neural and other trial-by-trial covariates via native hierarchical mixed-regression support.
-   Extensible for users to add novel models with corresponding likelihoods.
-   Built on PyMC with support from the Python Bayesian ecosystem at large.
-   Incorporates Bambi's intuitive `lmer`\-like regression parameter specification for within- and between-subject effects.
-   Native ArviZ support for plotting and other convenience functions to aid the Bayesian workflow.
-   Utilizes the ONNX format for translation of differentiable likelihood approximators across backends.

### Official documentation.

Cite HSSM
---------

Fengler, A., Xu, P., Bera, K., Omar, A., Frank, M.J. (in preparation). HSSM: A generalized toolbox for hierarchical bayesian estimation of computational models in cognitive neuroscience.

Example
-------

Here is a simple example of how to use HSSM:

import hssm

\# Load a package-supplied dataset
cav\_data \= hssm.load\_data('cavanagh\_theta')

\# Define a basic hierarchical model with trial-level covariates
model \= hssm.HSSM(
    model\="ddm",
    data\=cav\_data,
    include\=\[
        {
            "name": "v",
            "prior": {
                "Intercept": {"name": "Normal", "mu": 0.0, "sigma": 0.1},
                "theta": {"name": "Normal", "mu": 0.0, "sigma": 0.1},
            },
            "formula": "v ~ theta + (1|participant\_id)",
            "link": "identity",
        },
    \],
)

\# Sample from the posterior for this model
model.sample()

To quickly get started with HSSM, please follow this tutorial. For a deeper dive into HSSM, please follow our main tutorial.

Installation
------------

HSSM can be directly installed into your conda environment on Linux and MacOS. Installing HSSM on windows takes only one more simple step. We have a more detailed installation guide for users with more specific setups.

### Install HSSM on Linux and MacOS (CPU only)

Use the following command to install HSSM into your virtual environment:

conda install -c conda-forge hssm

### Install HSSM on Linux and MacOS (with GPU Support)

If you need to sample with GPU, please install JAX with GPU support before installing HSSM:

conda install jaxlib=\*\=\*cuda\* jax cuda-nvcc -c conda-forge -c nvidia
conda install -c conda-forge hssm

### Install HSSM on Windows (CPU only)

Because dependencies such as `jaxlib` and `numpyro` are not up-to-date on Conda, the easiest way to install HSSM on Windows is to install PyMC first and install HSSM via `pip`:

conda install -c conda-forge pymc
pip install hssm

### Install HSSM on Windows (with GPU support)

You simply need to install JAX with GPU support after installing PyMC:

conda install -c conda-forge pymc
pip install hssm\[cuda12\]

### Support for Apple Silicon, AMD, and other GPUs

JAX also has support other GPUs. Please follow the Official JAX installation guide to install the correct version of JAX before installing HSSM.

Advanced Installation
---------------------

### Install HSSM directly with Pip

HSSM is also available through PyPI. You can directly install it with pip into any virtual environment via:

pip install hssm

**Note:** While this installation is much simpler, you might encounter this warning message `WARNING (pytensor.tensor.blas): Using NumPy C-API based implementation for BLAS functions.` Please refer to our advanced installation guide for more details.

### Install the dev version of HSSM

You can install the dev version of `hssm` directly from this repo:

pip install git+https://github.com/lnccbrown/HSSM.git

### Install HSSM on Google Colab

Google Colab comes with PyMC and JAX pre-configured. That holds true even if you are using the GPU and TPU backend, so you simply need to install HSSM via pip on Colab regardless of the backend you are using:

!pip install hssm

Troubleshooting
---------------

**Note:** Possible solutions to any issues with installations with hssm can be located here. Also feel free to start a new discussion thread if you don't find answers there. We recommend installing HSSM into a new conda environment with Python 3.10 or 3.11 to prevent any problems with dependencies during the installation process. Please note that hssm is only tested for python 3.10, 3.11. As of HSSM v0.2.0, support for Python 3.9 is dropped. Use unsupported python versions with caution.

License
-------

HSSM is licensed under Copyright 2023, Brown University, Providence, RI

Support
-------

For questions, please feel free to open a discussion.

For bug reports and feature requests, please feel free to open an issue using the corresponding template.

Contribution
------------

If you want to contribute to this project, please follow our contribution guidelines.

Acknowledgements
----------------

We would like to extend our gratitude to the following individuals for their valuable contributions to the development of the HSSM package:

-   Bambi - A special thanks to the Bambi project for providing inspiration, guidance, and support throughout the development process. Tomás Capretto, a key contributor to Bambi, provided invaluable assistance in the development of the HSSM package.

Those contributions have greatly enhanced the functionality and quality of the HSSM.
