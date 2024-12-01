---
project: ElectrophysiologyData
stars: 396
description: A list of openly available datasets in (mostly human) electrophysiology. 
url: https://github.com/openlists/ElectrophysiologyData
---

Open Datasets in Electrophysiology
==================================

This is a list of openly available electrophysiological data, including EEG, MEG, ECoG/iEEG, and LFP data.

Datasets and resources listed here should all be openly-accessible for research purposes, requiring, at most, registration for access. Be sure to check the license and/or usage agreements for any datasets you access.

To contribute a new link to a data source or resource, open an issue mentioning it, or a pull request with a link.

Table of Contents
-----------------

-   Data Formats
-   Repositories
-   EEG Data
-   MEG Data
-   Human Intracranial Data
-   Animal Data
-   Behavioral Data

Data Formats
------------

The datasets listed here are not guaranteed to be in any particular format. Whenever possible, using standardized data formats can help make datasets more inter-operable.

Standardized data formats for neurophysiological data include:

-   Neurodata Without Borders, or NWB, is a general data standard for neurophysiology, with the goal of promoting a common standard for storing, sharing, and archiving data. The NWB project also maintains a list of publicly available NWB datasets.
-   Brain Imaging Data Structure, or BIDS, is a set of data standards for imaging data, including MRI, EEG, MEG, and iEEG.

Repositories
------------

There are several repositories, journals, and search engines that can be checked and searched for relevant datasets.

#### Neuroscience Specific Data Repositories

-   OpenNeuro is a platform for analyzing and sharing neuroimaging data. Originally focused on MRI datasets, it now includes other modalities, including some electrophysiological data. Data on OpenNeuro is generally organized in BIDS formats.
-   The DANDI archive ('distributed archives for neurophysiological data integration') is a platform for sharing and processing neurophysiological data. It includes a list of public datasets. Data on DANDI is generally organized in NWB format.
-   The DABI repository ('data archive BRAIN initiative') is a platform for storing and processing invasive neurophysiological data, in particular for the BRAIN initiative.
-   The EBrains platform for the European Union's 'Human Brain Project' includes a data portal with available data, including some extra- and intra-cranial human recordings
-   CONP, the 'Canadian Open Neuroscience Platform', is a resource for sharing open-science workflows and neuroscience data, including all kinds of neuroscience data.

#### General Purpose Data Repositories

There are a few general purpose repositories that you can search for data:

-   Zenodo hosts datasets for individual studies. You can find available datasets by searching for 'eeg', 'meg', or similar, and selecting the 'Dataset' tag on the bottom left of the search page.
-   Open Science Framework is a platform for supporting open science, and includes data hosting of open-datasets for specific studies. It doesn't seem to be easily searchable by data modality in particular, but does host relevant datasets, some of which are included in the listings below.
-   Figshare is a general repository service for a broad range of materials, and includes datasets. You can search for resources, and select 'type' as 'Dataset' to see available datasets.
-   Dryad is a repository service for scientific datasets, and includes data linked to specific papers, including some EEG/MEG/ECoG datasets. There is a search function.
-   G-Node Open Data is a repository service for scientific datasets, by G-Node (the German Neuroinformatics Node), built on the G-Node data infrastructure services.
-   Harvard Dataverse is a general-purpose repository for research data, that includes some neuroscience data
-   Science Data Bank is a general-purpose repository for research data, that includes some neuroscience data
-   Kaggle is a private company that hosts data analysis competitions. These competitions typically include a dataset, and they also maintain a repository of available datasets.
-   The IEEE Data Port is a general purpose repository managed by IEEE (the institute of electrical and electronics engineers). Some datasets are freely available, however some require a DataPort subscription. For neuroscience related data, see the biophysiological signal section.

#### Data Journals

There are journals that specifically describe openly available datasets, and/or mandate that data be openly released, including:

-   Scientific Data
    -   A general purpose journal that publishes brief reports on openly available datasets
-   Data in Brief
    -   A general purpose journal that publishes brief reports on openly available datasets
-   GigaScience
    -   A general topic journal that publishes papers for which all associated data must be made available
    -   Data is uploaded to their GigaDB database, that is searchable

#### Data Search Engines

Google has a dataset search tool that can be used to search for datasets.

EEG Data
--------

Openly available electroencephalography (EEG) datasets and large-scale projects with EEG data.

### ChildMind Institute

The ChildMind Institute is a non-profit that, amongst other things, is involved in large-scale research projects that release large datasets.

#### HBN - Healthy Brain Networks

A large project including rest and task EEG data across a large adult cohort (n=~1000).

Home Page - Data Portal - Paper

#### MIPDB - Multimodal Resource for Studying Information Processing in the Developing Brain

A project including rest and task EEG data across a young cohort, ages 6-44 (n=126).

Home Page - Data Portal - Paper

### Physionet

Physionet is an archive of physiology data, and includes some EEG data under the 'neuroelectric' tag.

Home Page - Data Portal - Paper

Available datasets include:

-   EEG Motor Movement / Imagery (n=109): Data

### PREDICT - Patient Repository for EEG Data + Computational Tools

PREDICT is a repository for EEG data, focused on patient data (collected in research settings).

Home Page - Data Portal - Paper

### TUH - Temple University Hospital Corpus

A large collection of EEG recorded in clinical settings (hospital data).

Home Page - Data Portal - Paper

The TUH includes multiple (described here), including:

-   The TUH EEG Corpus (TUEG), with over 30,000 hospital EEG recordings
-   The TUH Abnormal EEG Corpus (TUAB), with annotatations for if recordings are normal or abnormal
-   The TUH EEG Artifact Corpus (TUAR), with annotations of different artifacts
-   The TUH Epilepsy Corpus (TUEP), with a subset of subjects with and without epilepsy
-   The TUH EEG Events Corpus (TUEV), with annotations of specific events (sharp waves, epileptiform discharges, etc)
-   The TUH EEG Seizure Corpus (TUSZ), with annotations for seizures
-   The TUH EEG Slowing Corpus (TUSL), with annotations for slowing events

### EEGbase

EEGbase is a database for electrophysiological data.

Home Page - Paper

Note: you need to register, and the website has a 'Add to Cart' & 'Complete Order' workflow, but the datasets are free.

Available datasets include:

-   ERP Dataset, Visual P300 Paradigm (n=20): Paper
    -   Note that this data is also available on GigaDB
-   ERP OddBall Design, Number Guessing Game (n=250): Paper
-   ERP dataset on Developmental Coordination Disorder (n=32): Paper
-   EEG activity using a driving simulator (n=15): Paper

### Brain Clinics - TDBrain Dataset

The TDBrain dataset is a dataset of EEG data for 1200 subjects.

Homepage - Paper

### NITRC - Neuroimaging Tools & Resource Collaboratory

NITRC is a general purpose repository community board for neuroimaging tools, resources, and datasets. It is generally more focused on tools than datasets, but it does contain some available EEG datasets.

Home Page - Paper

Available datasets include:

-   Visual Oddball Task (n=18): Data - Paper
-   Categorization Task (n=14): Data
-   Resting State fMRI/EEG (n=8): Data

### ERP-CORE

ERP-CORE (Compendium of Open Resources and Experiments) is a resource with experiment paradigms and scripts, example data & example processing scripts for ERPs, including the N170, mismatch negativity (MMN), N2pc, N400, P300, lateralized readiness potential (LRP), and error-related negativity (ERN).

Data - Paper

### BNCI Horizon 2020

A collection of BCI related EEG datasets.

Home Page

### MASS - Montreal Archive of Sleep Studies

MASS is a collection of whole night sleep recordings from approximately 200 participants, from hospital based sleep laboratories.

Home Page - Data Portal - Paper

### NSRR - National Sleep Research Resource

NSRR is a resource offering large collections of physiological signals, including polysomnography recordings with EEG from research studies and clinical collections.

Home Page - Data Portal - Paper

### The Cuban Human Brain Mapping Project

The CHBMP is an open dataset from 282 young and middle age healthy participants, including resting state EEG, and during hyperventilation.

Data - Paper

### LEMON - Leipzig Study for Mind-Body-Emotion Interactions

A large multimodal dataset (n=228), with cross-sectional sampling of young and old participants, and including MRI, EEG, physiological, clinical and cognitive measures.

Homepage - Data - Paper

### PEERS - The PENN Electrophysiology of Encoding and Retrieval Study

A large dataset of EEG data (n>300), covering 5 experiments in which subjects perform memory tasks, encoding and retrieving stimuli.

Homepage - Data - Paper

### Lab-Specific Data Collections

The following labs are collections of datasets from particular labs:

-   Narayanan lab: predominantly EEG datasets collected from humans, including Parkinson's patients: Datasets - Lab website

### Individual EEG Datasets - Research Tasks (Research Systems)

The following are datasets collected with research EEG systems:

-   Motor Imagery BCI Data (n=52): Data - Paper
-   Simultaneous EEG & NIRS during cognitive tasks (n=26): Data - Paper
-   EEG during grasp and lift (n=12): Data - Paper
-   EEG, MEG & fMRI data with perceptual task (n=19): Data - Paper
-   EEG data with TMS with visual perception task (n=16): Data - Paper
-   EEG with Motion Capture during treadmill walking (n=8): Data - Paper
-   EEG data with a visual spatial attention task (n=45): Data - Paper
-   EEG data with a visual working memory task, ERP design (n=104): Data - Paper
-   EEG data with a visual working memory task, CDA design (n=76): Data - Paper
-   EEG data with a covert visual spatial attention task (n=50): Data - Paper
-   OpenMIIR: EEG data during music perception and imagination (n=10): Home Page - Data
-   EEG data from subjects napping after a working memory task (n=22): Data - Paper
-   DEAP: Database for Emotion Analysis, EEG data + video recording, while watching videos (n=32): Data - Paper
-   A collection of EEG tasks with speech studies (n=84, split across 5 tasks): Data - Paper
-   EEG recordings with concurrent EMG while doing everyday tasks (n=27): Data
-   Multi-modal (EEG, EMG, EOG) recordings during movement tasks (n=25): Data - Paper
-   EEG BCI recordings during mental imagery, across sessions & interaction paradigms (n=13): Data - Paper
-   EEG resting state data, with MRI anatomical scans (n=12): Data - Paper
-   Multi-day, multi band SSVEP dataset for BCI applications (n=30): Data - Paper
-   Multi-day, dataset from sleep (naps) recorded after visual working memory task (n=22): Data - Paper
-   EEG dataset from subjects viewing images (n=24): Data - Paper
-   EEG data with resting state and visual working memory task (n=43): Dataset1 - Dataset2 - Paper
-   EEG from participants playing an 8-bit style video game (n=17): Data - Paper
-   An EEG/BCI dataset across multiple paradigms and recording sessions (n=54): Data - Paper
-   A large EEG dataset with a simple gambling task (n=500): Data - Paper
-   A dataset comparing different EEG systems, including 3 sessions per participant (n=14): Data
-   An EEG/BCI dataset for inner speech recognition (n=10): Data - Paper
-   An EEG/BCI sensorimotor dataset, with longitudinal data (n=62): Data - Paper
-   An EEG dataset of with rapid serial visual presentation (n=50): Data - Paper
-   A dataset of hdEEG during transcranial electrical stimulation (n=20): Data - Paper
-   Mobile BCI dataset of scalp and ear EEG with ERP and SSVEP paradigms while standing and moving (n=24): Data - Paper
-   Polysomnography dataset, including 3 EEG channels, for sleep apnea studies (n=212): Data - Paper
-   EEG and EMG data during perturbed walking and standing (n=30): Data - Paper
-   EEG data in subjects with claustrophobia, and controls, resting state in different sized rooms (n=22): Data - Paper
-   A dataset of arm motion in healthy and post-stroke subjects, with some EEG data (n=45 with EEG): Data - Paper
-   A dataset of EEG and behavioral data with a visual working memory task in virtual reality (n=47): Data - Paper
-   The Nencki-Symfonia EEG/ERP dataset, high-density EEG with rest data and three tasks, including a Multi-Source Interference Task, an oddball task and a simple reaction task (n=42): Data - Paper
-   EEG from infants age 1-7 months, with longitudinal recordings (n=19) Data - Paper
-   A dataset of EEG data during visual object recognition, with a large number of trials per participant (n=10): Data - Paper

### Individual EEG Datasets - Research Tasks (Consumer Systems)

The following are available EEG datasets collected with consumer EEG systems:

-   MNIST of Brain Data from MindBigData (n=1 with 1.2 million trials): Data
-   ImageNet of the Brain from MindBigData (n=1 with 70,000 trials): Data

### Individual EEG Datasets - Clinical Recordings

The following are available EEG datasets collected in the context of clinical recordings / disease states:

-   Resting state data from Parkinson's patients, with healthy controls (n=28): Data - Paper
-   Data from neonatal EEG recordings with seizure annotations (n=79): Data - Paper
-   A dataset of EEG recordings from pediatric subjects with intractable seizures (n=22): Data - Paper
-   EEG recordings containing HFO markings for pediatric patients with epilepsy (n=30): Data
-   EEG recordings from children pre- and post-surgery for epilepsy (n=11): Data - Paper

### Other lists of EEG Data

There are some other lists of available EEG data, including:

-   A publicly curated list list of EEG data
-   The SCCN list of public EEG data

MEG Data
--------

Openly available magnetoencephalography (MEG) datasets and large-scale projects with MEG data.

### OMEGA - Open MEG Archive

OMEGA is a open-access repository for MEG data, in which individual researchers can deposit their data.

Home Page - Paper

### HCP - Human Connectome Project

The Human-Connectome Project is a large, multi-site project, mostly focused on MRI, that also includes a subset of MEG data.

Home Page

### CAMCAN - Cambridge Center for Ageing Neuroscience

CAMCAN includes task & rest MEG data from a large cohort, balanced in age from age 18-88 (n=652).

Home Page

### Individual MEG Datasets

The following are openly available datasets with MEG data:

-   'Mother of unification studies' (MOUS) dataset, resting state and language task (n=204): Data - Paper
-   Classification of Multimodal Stimulus Presentation - Visual & Auditory (n=52): Data - Paper
-   Multi-subject, multimodal face processing dataset including fMRI, MEG, EEG (n=16): Data - Paper
-   Decaf dataset, movie clip watching (n=30): Data
-   MEG data during four mental imagery tasks, for BCI analyses (n=17): Data - Paper
-   MEG data during pharmacological manipulation including taigabine, ketamine, and LSD (n=68): Data - Paper
-   MEG-MASC, a dataset of English speakers listening to naturalistic stories (n=27): Data - Paper

Human Intracranial Data
-----------------------

This section contains intracranial EEG (iEEG) data from humans participants (collected in clinical contexts), including electrocorticography (ECoG) and stereo-EEG (sEEG) recordings, as well as any available human single unit data.

### MNI Open iEEG Atlas

The MNI Open iEEG atlas is a multi-center repository of curated iEEG data, including resting state (n=106) and sleep (n=91) data.

Home Page - Paper (rest data) - Paper (sleep data)

### iEEG.org

iEEG.org is an NIH supported repository of intracranial EEG data.

Home Page

### University of Pennsylvania Computational Memory Lab

The cognitive electrophysiology data portal has a list of publications that have available electrophysiological data.

Home Page

The 'Restoring Active Memory' project is coordinate collection of ECoG data, with memory tasks (n=251).

Home Page

### Kai Miller's Collection of ECoG Data

A collection of ECoG recordings, including 204 sessions from across 16 different tasks (n=34).

Home Page - Paper

### Individual iEEG Datasets - Research Recordings

The following are openly available datasets with human intracranial data:

-   Multicenter resting state and sleep ECoG data, annotated for artifacts (n=39): Data - Paper
-   ECoG data from a study looking at sensorimotor alpha and beta activity (n=3): Data - Paper
-   Multimodal dataset of iEEG & fMRI data while watching a short movie (n=51 iEEG subjects): Data - Paper
-   A dataset of long-term iEEG recordings of naturalistic data & pose estimation (n=12): Data - Paper
-   Data from subjects with simultaneous EEG recordings and intracranial electrical stimulation (n=7): Data - Paper
-   Intracranial data during visual scene recognition of famous landmarks (n=50): Data - Paper
-   Intracranial data during memory tasks with pupillometry (n=10): Data - Paper
-   Intracranial data investigating responses to single-pulse stimulation (n=52): Data - Paper

### Individual iEEG Datasets - Clinical Recordings

The following are openly available datasets that contain seizures and/or are annotated for epilepsy:

-   A multicenter collection of iEEG data, including seizures (n=30): Data - Paper
-   A dataset of iEEG recordings from epilepsy patients, organized in BIDS (n=12): Data - Paper
-   Interictal iEEG during slow-wave sleep with HFO markings (n=20): Data - Paper
-   Intraoperative pre- and post-resection ECoG from epilepsy patients (n=22): Data - Paper

### Human Single Unit Data

Available datasets with single unit data from humans:

-   Human single units with a declarative memory task (n=59): Data - Paper - Associated Code
-   Human single units with a verbal working memory task, also including iEEG data (n=9): Data - Paper
-   Human single units from the amygdala, with visual presentation of neutral and aversive stimuli (n=9): Data - Paper
-   Single unit data from neuropixel probes in human cortex (n=3): Data - Paper

Animal Data
-----------

Openly available animal datasets with electrophysiological recordings collected from animal models, including local field potential (LFP) and/or single-unit activity collected from single-electrodes, multi-electrode arrays, animal ECoG, or similar recordings.

### NeuroTycho

NeuroTycho is as collection of mostly monkey ECoG data.

Home Page

### Collaborative Research in Computational Neuroscience (CRCNS)

A collection of data, including extra-cellular recordings, and some ECoG & iEEG, from various species.

Home Page - Data Portal - Paper

### Lab-Specific Data Collections

The following labs are collections of datasets from particular labs:

-   Buzsáki lab: electrophysiological datasets collected from rodents: Datasets - Lab website
-   Giocomo Lab: neural data recorded from rodents: Datasets - Lab website

### Individual Datasets

The following are available individual LFP and related datasets:

-   LFP during during delayed reach-to-grasp task (macaque monkey, n=2): Data - Paper
-   Raw LFP recordings and spiking data during anesthesia (rats, n=20): Data - Paper
-   Whole-cell intracellular recordings from somatosensory cortex (mouse, n=195): Data - Paper
-   High channel count (1024) Utah array recordings in macaque V1 and V4 from resting state (n=2): Data - Paper
-   Electrophysiological dataset from macaque visual cortical area MST (n=3): Data - Paper
-   Spiking activity from macaque primary motor and dorsal premotor cortex during delated reaching (n=1): Data
-   Data from high-density CMOS probes recorded from rats (n=3): Data

Behavioral Data
---------------

This list does not currently track behaviour-only data.

See this list of available behavioral data.
