# Dataset & management plan

Please provide information concerning the dataset you utilized, as well as it's management plan.

### How was the dataset search conducted?

 -> searched on open data websites like openneuro.org

### How was the dataset obtained?

 -> obtained dataset via download from openneuro.org

### What kind of data was utilized within the project?

 -> Dataset of EEG recordings containing high-frequency oscillation markings for 30 pediadric patients with epilepsy

### What kind of data was generated within the project?
 
 -> EEG data based on 10-20 system; high-frequency oscillations (HFO)
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

* What are the administrative and legal aspects of the data?

* How will the data be archived, exchanged and published?

* Who is responsible for the data and what are the duties associated with it?

* What costs and resources are associated with the project?


