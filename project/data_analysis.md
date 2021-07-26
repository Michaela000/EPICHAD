# Data analysis


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
  - define figure size
- set directory to data-folder to read in the edf.files
  - Important! Don't use derivatives data (bipolar electrodes)
- read in first subject
- check the raw data information: 
  - look at the raw channel names/types (important --> exclude reference channels A1, A2)
  - check data by plotting (timeplot)
  - set notch filter at 60 Hz
  - set a more precize filter (low-frequency, high-frequency, method, phase, fir-window, fir-design)
   - Hamming Window Design and frequency range from 0.1 - 40.0 Hz
  - plot again with filter 
- create 10-20 standard montage
  - plot topomap 
- setting up the ICA
  - ideal number of components here 8
  - create a copy of the raw data in order to apply a filter (low frequency at 1.0 Hz)
  - plotting the components

**Step 2: Data Analysis in MNE**
- creating fixed epochs 
  - duration of 2 seconds
  - resample of 500.0
- create Topomap for all subjects with all bands (Delta 0-4Hz; Theta 4-8Hz; Alpha 8-12Hz; Beta 12-30Hz; Gamma 30-45Hz)
  - Find out vmax and vmin for each frequency band and class (adults >7 years or children <7 years)
  - Create new topomaps with vmax/vmin 
  - exclude subject 4, 15 and 18 because of Problems with the channel Cz2
- create for loop for all subjects
  - import again all important modules
  - define the path to the dataset
  - path + add on (to sub-01-eeg data)
  - put in the path of all 27 subjects 
  - create 10-20 montage
  - split the files in order to only get the name of the subjects
  - read the raw data
  - drop the "reference channels" A1 and A2 and define "average" as the new reference 
  - apply notch and raw filter
  - apply the montage
  - create fixed epochs
  - create all figures (topomaps)
  - save them with fig.savefig (path)


### Outcomes

- Topomap outcomes for vmax and vmin: Adults: Delta 0.7-0.9; Theta 0.0-0.2; Alpha/Beta/Gamma 0.0-0.1 and Children: Delta 0.5-0.9; Theta 0.0-0.2; Alpha/Beta/Gamma 0.0-0.1
- Comparing the oscillation patterns of the two groups (Children and Adults)
