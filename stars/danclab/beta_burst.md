---
project: beta_burst
stars: 1
description:  Python to detect and analyze waveforms of beta bursts in M/EEG data.
url: https://github.com/danclab/beta_burst
---

* * *

Beta Bursts
===========

Overview
--------

**BetaBursts** is a Python package designed to detect beta bursts in brain signals, specifically EEG and MEG data. Beta bursts are rapid oscillations in the beta frequency band (13-30 Hz) and are crucial for movement-related cortical dynamics. This package provides a reliable method for detecting these bursts using advanced signal processing techniques.

The method is described in the paper by Maciek Szul et al. (2023) "Diverse beta burst waveform motifs characterize movement-related cortical dynamics" Progress in Neurobiology. https://doi.org/10.1016/j.pneurobio.2023.102490

The code have been developed by Maciek Szul, Sotirios Papadopoulos, Ludovic DARMET and Jimmy Bonaiuto, head of the DANC lab.

Features
--------

-   Detect beta bursts in EEG and MEG signals.
-   Analysis of the extracted bursts using PCA, to find specific waveforms modulated by the task.
-   Includes a suite of tests to ensure the accuracy and reliability of the detection algorithms.

Installation
------------

To install the BetaBurst package, clone the repository and run:

git clone https://github.com/danclab/beta\_burst
cd beta\_burst
pip install -e .

### Requirements

-   Python 3.x
-   numpy
-   scipy
-   sklearn
-   matplotlib
-   fooof

These dependencies will be installed automatically when you run the setup script.

Usage
-----

Here is a basic example of how to extract burst from M/EEG data:

from betaburst.detection.burst\_detection import TfBursts

\# Example usage with M/EEG data
meeg\_data \= ...  \# Your M/EEG data here
\# Burst detection parameters
freq\_step \= 0.5
freqs \= np.arange(5.0, 47.0, freq\_step)
upto\_gamma\_band \= np.array(\[5, 40\])
upto\_gamma\_range \= np.where(
    np.logical\_and(freqs \>= upto\_gamma\_band\[0\], freqs <= upto\_gamma\_band\[1\])
)\[0\]

tfbursts \=TfBursts(
        fs,
        freqs \= freqs,
        fr\_band \= upto\_gamma\_band,
        band\_search\_range \= upto\_gamma\_range,
        band\_limits\=\[8, 10, 35\],
        remove\_fooof\=False,
    )

bursts \= bm.burst\_extraction(epochs, band\="beta")
print("Detected bursts:", bursts)

\# You can access time-frequency decompositions (using superlets)
tfs \= bm.tfs
\# Or without running burts extraction
tfs \= bm.\_apply\_tf(meeg\_data)

It is then possible to study the bursts waveforms using PCA.

from betaburst.analysis.burst\_analysis import BurstSpace

bs \= BurstSpace(perc\=0.5, nb\_quartiles\=10, tmin\=0, tmax\=5, time\_step\=0.2)
\# Feat a PCA model (along the time axis of bursts) and compute a score
\# for each burst. The score is the distance to the PCA axis.
scores\_dists \= bs.fit\_transform(bursts)
\# Distribution of waveforms along each PC axis
bs.plot\_waveforms()

modulation\_index, comp\_waveforms \= bs.waveforms\_rate()
\# Heatmap of modulation index during time (bursts rates of each quartile)
bs.plot\_burst\_rates()

Testing
-------

To run the tests with `pytest`, use the following command:

pytest betaburst/tests

This will execute all tests located in the `betaburst/tests` directory, ensuring the correctness of the implementation.

Contributing
------------

Contributions are welcome! If you find any bugs or have ideas for improvements, feel free to open an issue or submit a pull request.

License
-------

This project is licensed under the MIT License - see the LICENSE file for details.
