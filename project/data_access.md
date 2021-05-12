# Data access

Please provide information on how the data can be accessed.

- Information from BIDS-Validator v1.7.1
  - Dataset consists of 96 files, 15.07 GB
  - 30 Subjects
  - 1 Session
  - Available Tasks: hfo
  - Available Modalities: channels; eeg
- We will analyze the data with MNE-Python (MEG + EEG Analysis & Visualization)

* Raw data
- The data is from the dataset: https://openneuro.org/datasets/ds003555/versions/1.0.1

* Data derivatives 
- License: CC0
- Authors: Dorottya Cserpan, Ece Boran, Richard Rosch, San Pietro Lo Biundo, Georgia Ramantani, Johannes Sarnthein
- There are four different subfolders:
  - hfo/sub-** (Contains folder for each subject, named sub-<subject number> and session information)
  - hfo/sub-**/ses-01/eeg (Contains raw eeg data in .edf format for each subject. The duration is typically 3 hours, that was recorded in the beginning of the sleep. Details about the channels are given in the corresponding .tsv file)
  - hfo/derivates (Besides containingsubfolders for the raw data, there are two .json files. The events_description.json explains the meaning of the columns of the event description tsv files (in the subfolders).
The interval_description.json explains the meaning of the columns of the interval description tsv files (in the subfolders))
  - hfo/derivatives/sub-**/ses-01/eeg/ (Contains processed data for each subject. Based on the sleep annotations, first we identified the sleep stages. Then we cut 5 minutes data intervals from the N3 sleep stages. We applied bipolar referencing by considering all nearest neighbour chanels, thus resulting in 52 bipolar channels. Each run corresponds to one 5 minute data interval. The DataIntervals.tsv file provides information about how the various runs are related to the raw data by providing the start and end indeces. Besides the .edf and channel descriptor .tsv files there is an other .tsv file containing the detected candidate event details. Eg. sub-26_ses-01_task-hfo_run-01_events.tsv contains for subject 26 for the first processed data interval the event markings as indeces with additional features of this event described in the abovementioned events_description.json file.)
- Dataset DOI: 10.18112/openneuro.ds003555.v1.0.1
- Fundings of the original dataset: Swiss National Science Foundation (CRSK-3_190895 to G.R. and J.S.)
