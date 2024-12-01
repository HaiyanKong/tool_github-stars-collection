---
project: laMEG
stars: 13
description: Toolbox for laminar inference with MEG
url: https://github.com/danclab/laMEG
---

Toolbox for laminar inference with MEG, powered by FreeSurfer and SPM

Operating system
----------------

-   Windows: Tested on WSL (using Ubuntu 24.04.1), follow instructions here
-   Mac: May work, not tested
-   Linux: Tested on Ubuntu and Debian

Requirements
------------

-   FreeSurfer v6.0
-   Python version 3.7
-   Anaconda (or miniconda)

Installation
------------

1.  Create a conda environment:
    
    conda create -n <env name> python=3.7
    
    replacing `<env name>` with the name of the environment you would like to create (i.e. 'lameg', or the name of your project)
    
2.  Activate the environment:
    
    conda activate <env name>
    
    replacing `<env name>` with name of the environment you created.
    
3.  Install FreeSurfer, following the instructions on this page
    
4.  To install `laMEG`, run:
    
    pip install lameg
    
    This also installs SPM standalone and Matlab runtime, which can take some time depending on your connection speed.
    
5.  Before using, deactivate and reactivate the environment for changes to environment variables to take effect:
    
    conda deactivate
    conda activate <env name>
    
6.  If you want to run the tutorials, download and extract the test data
    

Documentation and Tutorials
---------------------------

Once you have installed `laMEG`, check out the example notebooks, tutorials, and documentation.

Funding
-------

_Supported by the European Research Council (ERC) under the European Union's Horizon 2020 research and innovation programme grant agreement 864550, and a seed grant from the Fondation pour l'Audition._
