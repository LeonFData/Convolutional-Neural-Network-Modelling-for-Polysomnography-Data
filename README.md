## Convolutional Neural Network Modelling for Polysomnography Data of Obstructive Sleep Apnea Diagnosis

<p align="center">
  <img width="450" src="Master Thesis/Images/sleep_study.png">
</p>

- picture by Emily Roberts, Verywell

## Introduction
- This is a Master Thesis during my study in Wilfrid Laurier University (2018-2019)
  * Thesis Supervisor: [**Dr. Xu (Sunny) Wang**](https://www.wlu.ca/academics/faculties/faculty-of-science/faculty-profiles/xu-sunny-wang/index.html?ref=faculty-profiles%2Fscience%2Fxu-sunny-wang.html)
  * Examining Committee: [**Dr. Roman Makarov**](https://www.wlu.ca/academics/faculties/faculty-of-science/faculty-profiles/roman-makarov/index.html) &
  [**Dr. Yang Liu**](https://online.wlu.ca/faculty/yang-liu)

- The main goal of this project is to investigate how effective a CNN model could be used to classify high dimensional polysomnography signals. Based on the application on Polysomnography (PSG) data, I will find:

    * The proper CNN architectures for the PSG data.
    * The optimized hyperparameters for the performance of CNN models.
    * The performance visualization for the prediction of different OSA severity levels, i.e, different obstructive sleep apnea levels.

- Ultimately, the chosen CNN models can be used as a screening tool for those suspected suffer from OSA.

- Codes are shown on Jupyter Notebook (Click [**Here**](https://github.com/LeonFData/Convolutional-Neural-Network-Modelling-for-Polysomnography-Data/blob/master/Master%20Thesis/CNN_Modelling.ipynb))

## Data
The data are retrieved from the National Sleep Research Resource ([**NSRR**](https://sleepdata.org/)), which is a new National Heart, Lung, and Blood Institute resource designed to provide big data resources to the sleep research community. The PSG data are available for 517 participants at ages 16-19. Each anonymous record includes the summary results of a 12-hour overnight sleep study (awake and sleep stages) including annotation files with scored events and physiological signals from the sleep record. Each has a signal file in the European Data Format ([**EDF**](https://en.wikipedia.org/wiki/European_Data_Format)) exported from Compumedics Profusion. In this project, we conduct data pre-processing and CNN modeling on the data in EDF files which have an total size of 13 GB.

<p align="center">
  <img width="550" src="Master Thesis/Images/CCSHS.png">
</p>

## Requirements
- `Data access` to Cleveland Children's Sleep and Health Study ([**CCSHS**](https://sleepdata.org/datasets/ccshs)) database is approved via [**Dr. Xu (Sunny) Wang**](https://www.wlu.ca/academics/faculties/faculty-of-science/faculty-profiles/xu-sunny-wang/index.html?ref=faculty-profiles%2Fscience%2Fxu-sunny-wang.html)
- `Window 10 64 bit`
- `Python version 3.6`
- `Deep Learning Package: Tensorflow`
- `pyedflib Package to read PSG signal`
- `Google Colab GPU Platform`

## Some CNN Concepts on PSG Data
- Data Pre-processing (Segmentation)
  * In this project, the PSG data were segmented into 1-minute long events to avoid memory issues.

<p align="center">
  <img width="500" src="Master Thesis/Images/preprocessing.png">
</p>

- Feature Extraction (1-D Convolution + 1-D Maxpooling)
  * The example shows a 3-min piece of ECG channel, just for displaying how CNN does the automatic feature extraction on 1-D Data
 
<p align="center">
  <img width="700" src="Master Thesis/Images/FE.png">
</p>

- CNN Architecture ([**AlexNet**](https://en.wikipedia.org/wiki/AlexNet))

<p align="center">
  <img width="500" src="Master Thesis/Images/1dCNN.png">
</p>

## Modelling Results
- ECG
<center><image src="Master Thesis/Images/ECG.png"></image></center>

- EEG
<center><image src="Master Thesis/Images/EEG.png"></image></center>

- EMG
<center><image src="Master Thesis/Images/EMG.png"></image></center>

- Respiratory
<center><image src="Master Thesis/Images/Respiratory.png"></image></center>

## Reference
- Cen L., Yu Z.L., Tang Y., Shi W., Kluge T., Ser W. (2017) Deep Learning Method for Sleep Stage Classification. In: Liu D., Xie S., Li Y., Zhao D., El-Alfy ES. (eds) Neural Information Processing. ICONIP 2017. Lecture Notes in Computer Science, vol 10635. Springer, Cham

- Urtnasan, E., Park, JU., Joo, EY. et al. J Med Syst (2018) 42: 104. https://doi.org/10.1007/s10916-018-0963-0
