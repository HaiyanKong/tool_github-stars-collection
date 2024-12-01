---
project: Data-code-for-https-doi.org-10.1101-2020.07.22.215517
stars: 1
description: null
url: https://github.com/ZHANGneuro/Data-code-for-https-doi.org-10.1101-2020.07.22.215517
---

Data-code-for-https-doi.org-10.1101-2020.07.22.215517
-----------------------------------------------------

This repository includes behavioral & neuroimaging analyzing codes (MRI/MEG) and data (MRI & MEG behavior) for the manuscript entitled "Distinct networks coupled with parietal cortex for spatial representations inside and outside the visual field"  
doi: https://doi.org/10.1101/2020.07.22.215517  
  
  
For MRI & MEG imaging datasets, and eye datasets, please contact Dr. Yuji Naya in the following address:  

Yuji Naya
Email: yujin@pku.edu.cn
McGovern Institute for Brain Research, Peking University
No. 52, Haidian Road, Wang Kezhen Building, Room 1707
Haidian District, Beijing 100805, China
Telephone: +86-10-62765734

  
  

Repository structure:
---------------------

Note: for more detailed code description or questions please contact bo.zhang@pku.edu.cn  
.  
|-- beh\_eyedata\_meg  
│     |-- sub\_x\_sx\_rawdata.txt   `` col indicates `sub_no` `exp_cond` `map_id` `enter_dir_id` `fac_cha_id` `tar_cha_id` `hn1_id` `hn2_id` `hn3_id` `prof_id` `ego_dir` `cue` `response` ``  
│      
│     |-- sub\_x\_sx\_timing.txt   `` col indicates onsets of `ITI` `session id` `noise screen` `facing period` `noise screen` `targeting period` `noise screen` `cue` `response` ``  
│      
|-- beh\_eyedata\_fmri  
│     |-- sub\_x\_formal\_rawdata.txt   `` col indicates `sub_no` `map_id` `enter_dir_id` `head nodding(HD)` `HD response` `HD outcome` `score` `fac_cha_id` `fac_dir_id` `target_dir` `tar_cha_id` `cue` `response` ``  
│      
│     |-- sub\_x\_formal\_Time\_record\_t.txt   `` col indicates onsets of `ITI` `session id` `noise screen` `facing period` `noise screen` `targeting period` `noise screen` `cue` `response` ``  
│      
|-- script\_R  
│     |-- script\_fmri\_beh\_format\_reorganize.R   `reorganize fMRI behavioral data format for further process`  
│     |-- script\_meg\_beh\_format\_reorganize.R   `reorganize MEG behavioral data format for further process`  
│     |-- script\_plot\_eyedata\_number\_meg.R   `plot number of fixation and saccade for MEG data`  
│     |-- script\_plot\_eyedata\_number\_mri.R   `plot number of fixation and saccade for fMRI data`  
│     |-- script\_plot\_eyedata\_pos\_barchart\_meg.R   `plot position of fixation and saccade for MEG data`  
│     |-- script\_plot\_eyedata\_pos\_barchart\_mri.R   `plot position of fixation and saccade for fMRI data`  
│     |-- Yuji\_bayesfactor.R   `Bayesian analyses including bayes factor, median and credible interval computation`  
│      
|-- script\_bash  
│     |-- script\_bandpass\_filtering.sh   `perform bandpass filtering on 4d bold signal series`  
│     |-- script\_fsf\_generator.sh   `generate FSL fsf file for 1st level GLM analysis`  
│     |-- script\_fun2stand.sh   `transforamtion script from native space to standard space`  
│     |-- script\_permutation.sh   `permutation test using FSL randomize function`  
│     |-- script\_run\_feat.sh   `script for parallel process`  
│     |-- script\_stand2fun.sh   `transforamtion script from standard space to native space`  
│      
|-- script\_matlab  
│     |-- script\_FC\_correlation.m   `perform correlation across brain between ROI and each brain voxel`  
│     |-- script\_FC\_extract\_targeting\_TRs.m   `extract RTs & generates targeting period 4-d data series for FC analysis`  
│     |-- script\_MRI\_activity\_volume\_contrast.m   `perform contrast in beta images of GLM model for each condition`  
│     |-- script\_MRI\_timingFile\_generator.m   `generate standard FSL timing file for GLM analysis`  
│     |-- script\_dicom2nii.m   `format transformation from dicom to nii`  
│     |-- script\_eyeData\_number\_meg.m   `extract number of fixation & saccade from MEG eye dataset`  
│     |-- script\_eyeData\_number\_mri.m   `extract number of fixation & saccade from MRI eye dataset`  
│     |-- script\_eyeData\_visual\_angle\_meg.m   `extract position from MRI eye dataset`  
│     |-- script\_eyeData\_visual\_angle\_mri.m   `extract position from MEG eye dataset`  
│     |-- script\_eyeDate\_gaze\_anova\_meg.m   `extract gaze from MEG eye dataset`  
│     |-- script\_eyeDate\_gaze\_anova\_mri2.m   `extract gaze from MRI eye dataset`  
│     |-- script\_load\_behavioral\_table\_fmri.m   `load behavioral data of MRI experiment`  
│     |-- script\_load\_behavioral\_table\_meg.m   `load behavioral data of MEG experiment`  
│     |-- script\_mni\_r\_brain\_session\_averaged\_from\_glm.m   `generate mean MRI volume file across sessions for each subject`  
│     |-- script\_ploting\_draw\_colorbar.m   `plot colorbar given value distribution from contrast analysis`  
│     |-- script\_statistic\_glm.m   `perform 2nd level group test (uncorrected)`  
│      
|-- script\_py  
│     |-- script\_MEG\_morph\_source\_to\_fsaverage.py   `generate MEG source map and plot on surface`  
│     |-- script\_MEG\_PLI.py   `perform MEG phase lag index analysis for specific frequency`  
│     |-- script\_MEG\_preprocessing\_artificial.py   `MEG preprocessing & artificial removal`  
│     |-- script\_MEG\_source\_ROI\_linechart.py   `plot MEG source time series from ROI`  
│     |-- script\_MEG\_source\_surface\_plot.py   `plot MEG source map on surface`  
│     |-- script\_MEG\_topo\_activity\_contrast.py   `perform topographic contrast among conditions`  
│     |-- script\_MEG\_topo\_activity\_main\_effect.py   `perform contrast of topographic map among conditions`  
│     |-- script\_MEG\_topo\_parietal\_mask\_linechart.py   `plot MEG topographic activity time series from ROI`  

  
  

Env & Dependency:
-----------------

MacOS Big Sur `11.4`  
Matlab `R2019b`  
R `4.0.2`  
R studio `1.3.1073`  
Python `3.3.8`  
Conda `4.9.2`  
MNE `v0.23.0`
