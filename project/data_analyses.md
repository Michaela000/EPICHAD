# Data analyses

Provide readers/users with a general outline of the conducted analyses and corresponding outcomes.

- The data to analyze is from this dataset: https://openneuro.org/datasets/ds003555/versions/1.0.1
- The Program that we will use is MNE-Python 
- We will first look at the 30 subjects in order to find differences between children and adults with epilepsy. 
- Further questions about the analysis will be answered in the future. 

## Overview

Provide information concerning the different analysis parts, as well as links to respective notebooks.

Step 1: Preprocessing in MNE
- import modules
  - os
  - numpy
  - mne
  - matplotlib.pyplot
- set directory to data-folder to read in the edf.files
  - Important! Don't use derivatives data (bipolar electrodes)
- read in first subject
- check the raw data information: 
  - look at the raw channel names/types 
  - check data by plotting (timeplot)
  - set filter (low-frequency, high-frequency, method, phase, fir-window, fir-design)
  - plot again with filter 
- create montage
  - plot topomap 
- ICA
  - plotting

## Outcomes

Provide information concerning the outcomes of the different analysis parts, as well as links to further
details on data access.
