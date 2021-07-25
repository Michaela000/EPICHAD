# Data analyses


- The data to analyze is from this dataset: https://openneuro.org/datasets/ds003555/versions/1.0.1
- The Program that we will use is MNE-Python 
- We will first look at the 30 subjects in order to find differences between children and adults with epilepsy. 
- Further questions about the analysis will be answered in the future. 

### Overview

Provide information concerning the different analysis parts, as well as links to respective notebooks.

**Step 1: Preprocessing in MNE**
- import modules
  - os
  - numpy
  - mne
  - matplotlib.pyplot
- set directory to data-folder to read in the edf.files
  - Important! Don't use derivatives data (bipolar electrodes)
- read in first subject
- check the raw data information: 
  - look at the raw channel names/types (important --> exclude reference channels A1, A2)
  - check data by plotting (timeplot)
  - set filter (low-frequency, high-frequency, method, phase, fir-window, fir-design)
  - plot again with filter 
- create montage
  - plot topomap 
- ICA
  - plotting

**Step 2: Data Analysis in MNE**
- creating fixed epochs 
- create Topomap for all subjects with all bands (Delta 0-4Hz; Theta 4-8Hz; Alpha 8-12Hz; Beta 12-30Hz; Gamma 30-45Hz)
  - Find out vmax and vmin for each frequency band and class (adults >7 years or children <7 years)
  - Create new topomaps with vmax/vmin 
  - Create for loop for all subjects


### Code
"source": [
""import pandas as pd\n",
""print("Hi! This is a cell. Click on it and press the ▶ button above to run it")\n"
]



### Outcomes

- Topomap outcomes for vmax and vmin: Adults: Delta 0.7-0.9; Theta 0.0-0.2; Alpha/Beta/Gamma 0.0-0.1 and Children: Delta 0.5-0.9; Theta 0.0-0.2; Alpha/Beta/Gamma 0.0-0.1
- Comparing the oscillation patterns of the two groups (Children and Adults)
