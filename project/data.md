# Dataset 

### How was the dataset search conducted?

 - searched on open data websites like openneuro.org

### How was the dataset obtained?

 - obtained dataset via download from openneuro.org

### What kind of data was utilized within the project?

 - Dataset of EEG recordings containing high-frequency oscillation markings for 30 pediadric patients with epilepsy
 - This study consists of 30 human subjects. 
 - 14 subjects were classified as children, with the age from 0.7-6.6 years. 
 - The other 16 subjects were classified as adults with the age 7.1-17.4 years. 
 - All subjects need to have focal or generalized epilepsy.

### What kind of data was generated within the project?
 
 - EEG data based on 10-20 system; high-frequency oscillations (HFO)
### How was the data organized?
 
 * Main directory (hfo/)
    Contains metadata files in the BIDS standard about the participants and the study. Folders are explained below

 * Subfolders
 
      hfo/sub-**/.
  Contains folders for each subject, named sub-<subject number> and session information.
  
   hfo/sub-**/ses-01/eeg.
  Contains the raw eeg data in .edf format for each subject. The duration is typically 3 hours, that was recorded in the beginning of the sleep. Details about the    channels are given in the corresponding .tsv file. 
  -> hfo/derivatives
  Besides containingsubfolders for the raw data, there are two .json files. The events_description.json explains the meaning of the columns of the event description tsv files (in the subfolders).
  The interval_description.json explains the meaning of the columns of the interval description tsv files (in the subfolders).

   hfo/derivatives/sub-**/ses-01/eeg/.
  Contains processed data for each subject. Based on the sleep annotations, first we identified the sleep stages. Then we cut 5 minutes data intervals from the N3 sleep stages. We applied bipolar referencing by considering all nearest neighbour chanels, thus resulting in 52 bipolar channels. Each run corresponds to one 5 minute data interval. The DataIntervals.tsv file provides information about how the various runs are related to the raw data by providing the start and end indeces. Besides the .edf and channel descriptor .tsv files there is an other .tsv file containing the detected candidate event details. Eg. sub-26_ses-01_task-hfo_run-01_events.tsv contains for subject 26 for the first processed data interval the event markings as indeces with additional features of this event described in the abovementioned events_description.json file.
 
Raw data information:
 ![raw_channel_info](https://user-images.githubusercontent.com/82948946/126980801-649e12df-8365-4b4c-b603-2cda5594e1f6.PNG)


### What are the administrative and legal aspects of the data?
- License: CC0
- Ethics Approvals: Kantonale Ethikkommission ZÃ¼rich ( KEK-ZH PB-2016-02055)

### How will the data be archived, exchanged and published?
- Citation: Dorottya Cserpan and Ece Boran and Richard Rosch and San Pietro Lo Biundo and Georgia Ramantani and Johannes Sarnthein (2021). Dataset of EEG recordings of pediatric patients with epilepsy based on the 10-20 system . OpenNeuro. [Dataset] doi: 10.18112/openneuro.ds003555.v1.0.1
- Dataset DOI: 10.18112/openneuro.ds003555.v1.0.1
- Code for HFO detection: https://github.com/ZurichNCH/Automatic-High-Frequency-Oscillation-Detector
- archived in OpenNeuro - free to download 

### Who is responsible for the data and what are the duties associated with it?
- Authors: Dorottya Cserpan, Ece Boran, Richard Rosch, San Pietro Lo Biundo, Georgia Ramantani, Johannes Sarnthein
- Support: For questions on the dataset or the task, contact Johannes Sarnthein at johannes.sarnthein@usz.ch.
- Updated on OpenNeuro by Dorottya Cserpan on 2021-03-05 

### What costs and resources are associated with the project?
- Funding: Swiss National Science Foundation (CRSK-3_190895 to G.R. and J.S.)
