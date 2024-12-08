---
project: HyPyP
stars: 75
description: The Hyperscanning Python Pipeline
url: https://github.com/ppsp-team/HyPyP
---

HyPyP 🐍〰️🐍
============

The **Hy**perscanning **Py**thon **P**ipeline

⚠️ This software is in beta and thus should be considered with caution. While we have done our best to test all the functionalities, there is no guarantee that the pipeline is entirely bug-free.

📖 See our paper for more explanation and our plan for upcoming functionalities (aka Roadmap).

🤝 If you want to help you can submit bugs and suggestions of enhancements in our Github Issues section.

🤓 For the motivated contributors, you can even help directly in the developpment of HyPyP. You will need to install Poetry (see section below).

Contributors
------------

Original authors: Florence BRUN, Anaël AYROLLES, Phoebe CHEN, Amir DJALOVSKI, Yann BEAUXIS, Suzanne DIKKER, Guillaume DUMAS New contributors: Ghazaleh RANJBARAN, Quentin MOREAU, Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO, Julie BONNAIRE

Installation
------------

```
pip install HyPyP
```

Documentation
-------------

HyPyP documentation of all the API functions is available online at hypyp.readthedocs.io

For getting started with HyPyP, we have designed a little walkthrough: getting\_started.ipynb

Core API
--------

🛠 io.py — Loaders (Florence, Anaël, Ghazaleh, Franck, Jonas, Guillaume)

🧰 utils.py — Basic tools (Amir, Florence, Guilaume)

⚙️ prep.py — Preprocessing (ICA & AutoReject) (Anaël, Florence, Guillaume)

🔠 analyses.py — Power spectral density and wide choice of connectivity measures (Phoebe, Suzanne, Florence, Ghazaleh, Juan, Guillaume)

📈 stats.py — Statistics (permutations & cluster statistics) (Florence, Guillaume)

🧠 viz.py — Inter-brain visualization (Anaël, Amir, Florence, Guillaume)

🎓 Tutorials - Examples & documentation (Anaël, Florence, Yann, Ghazaleh, Caitriona, Guillaume)

Poetry installation (only for developpers and adventurous users)
----------------------------------------------------------------

Step 1: `pip install poetry`

Step 2: `git clone git@github.com:ppsp-team/HyPyP.git`

Step 3: `cd HyPyP`

Step 4: `poetry install`

Step 5: `poetry shell`

You can now use `jupyter notebook` or `ipython`!

⚠️ If you need to install a new dependency (not recommended), you have to use `poetry add THE_NAME_OF_THE_LIBRARY` instead of your usual package manager.
