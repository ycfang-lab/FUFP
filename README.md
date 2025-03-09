# FUFPdataset
a dataset for familiar and unfamiliar face perception analysis using eeg signals
## dataset summary
The EEG signals of 66 channels are recored from 8 participants at a sampling rate of 1000 Hz. Each subject randomly watches 8 familiar faces (FFs) and 32 unfamiliar faces (UFs). This process is repeated 20 times, resulting in a total of 6400 samples.

For a more thorough explanation of the dataset collection and its contents, see [1].
## file listing
The following files are available:


|File name|Format|Contents|
|:----|:----|:----|
|FF|jpg|8 student ID photos of the subjects who know each other used as FF stimuli|
|UF|tif|32 frontal young faces from the CAS-PEAL-R1 dataset[2] used as UF stimuli|
|Subject1-8|mat|The preprocessed EEG data with 6 labels|

## data structure
|Variable name|Shape|Contents|
|:----|:----|:----|
|label|1×800|0 is UF, 1 is FF|
|resp|1×800|subject's button response, 1 is FF, 2 is UF|
|acc|1×800|whether the subject responds correctly to the stimulus|
|RT|1×800|the response time of the subject recorded in milliseconds|
|sti|1×800|the stimulus represented by "1" to "40", wherein the first 8 stimulus represents FF and the remaining 32 represents UF|
|label2|1×800|0 is UF, 1 is FF, 2 is the subject's own face|
|data|800×66×3000|the EEG signal|
