## Convolutional Neural Network Modelling for Polysomnography Data of Obstructive Sleep Apnea Diagnosis



### Introduction
- This is a Master Thesis during my study in Wilfrid Laurier University (2018-2019)
  * Thesis Supervisor: [**Dr. Xu (Sunny) Wang**](https://www.wlu.ca/academics/faculties/faculty-of-science/faculty-profiles/xu-sunny-wang/index.html?ref=faculty-profiles%2Fscience%2Fxu-sunny-wang.html)
  * Examining Committee: [**Dr. Roman Makarov**](https://www.wlu.ca/academics/faculties/faculty-of-science/faculty-profiles/roman-makarov/index.html) &
  [**Dr. Yang Liu**](https://online.wlu.ca/faculty/yang-liu)

- The main goal of this project is to investigate how effective a CNN model could be used to classify high dimensional polysomnography signals. Based on the application on Polysomnography (PSG) data, I will find:

    * 1. The proper CNN architectures for the PSG data.
    * 2. The optimized hyperparameters for the performance of CNN models.
    * 3. The performance visualization for the prediction of different OSA severity levels, i.e, different obstructive sleep apnea levels.

- Ultimately, the chosen CNN models can be used as a screening tool for those suspected suffer from OSA.

### Data
The data are retrieved from the National Sleep Research Resource ([**NSRR**](https://sleepdata.org/)), which is a new National Heart, Lung, and Blood Institute resource designed to provide big data resources to the sleep research community. The PSG data are available for 517 participants at ages 16-19. Each anonymous record includes the summary results of a 12-hour overnight sleep study (awake and sleep stages) including annotation files with scored events and physiological signals from the sleep record. Each has a signal file in the European Data Format ([**EDF**](https://en.wikipedia.org/wiki/European_Data_Format)) exported from Compumedics Profusion. In this project, we conduct data pre-processing and CNN modeling on the data in EDF files which have an total size of 13 GB.

<center><image src="https://github.com/JONGGON/DeepHumanPrediction/blob/master/DeepHumanPrediction/HumanMotion_.png" width=1000 height=500></image></center>

### Requirements
- `Data access` to Cleveland Children's Sleep and Health Study ([**CCSHS**](https://sleepdata.org/datasets/ccshs)) database is approved via [**Dr. Xu (Sunny) Wang**](https://www.wlu.ca/academics/faculties/faculty-of-science/faculty-profiles/xu-sunny-wang/index.html?ref=faculty-profiles%2Fscience%2Fxu-sunny-wang.html)
- `Window 10 64 bit`
- `Python version 3.6`
- `Deep Learning Package: Tensorflow`
- `pyedflib Package to read PSG signal`
- `Google Colab GPU Platform`

## Some CNN Concepts on PSG Data
- Data Pre-processing (Segmentation)
In this project, the PSG data were segmented into 1-minute long events to avoid memory issues.




- Feature Extraction (1-D Convolution + 1-D Maxpooling)
The example shows a 3-min piece of ECG channel, just for displaying how CNN does the automatic feature extraction on 1-D Data



- [**AlexNet Architecture**](https://en.wikipedia.org/wiki/AlexNet)


## Modelling Results

#### ECG Channels

#### EEG Channels

#### EMG Channels

#### Respiratory Channels

