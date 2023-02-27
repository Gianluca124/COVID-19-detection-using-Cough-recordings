# COVID-19 detection using cough recording

## Table of contents
* [Abstract](#abstract)
* [Report](https://www.slideshare.net/GianlucaCavallaro3/medical-data-management-covid19-detection-using-cough-recordings-chest-xrays-classification-and-generation)
* [Requirements](#requirements)
* [Pre-processing](#pre-processing)
* [Data Augmentation](#data-augmentation)
* [Feature Extraction](#feature-extraction)
* [Training](#training)
* [Results](#results)


## Abstract

This is the first part of the project which also includes the work shown in [this repository](https://github.com/Gianluca124/CXR-ACGAN-chest-xray-generator-covid19-pneumonia).

The aim of this first part is to try to build a neural network capable of recognizing people positive to COVID-19 using cough recordings.

## Requirements

- python==3.8
- ipython
- ipykernel
- pandas
- numpy
- scipy
- os
- subprocess
- matplotlib
- librosa
- soundfile
- audiomentations
- pydub
- ffmpeg
- noisereduce
- sklearn
- tensorflow
- tensorflow_io
- cv2


## Pre-processing

### Step 1. Download and extract the dataset

Download the dataset from the [official repository](https://c4science.ch/diffusion/10770/).

### Step 2. Setup

Perform all the necessary setup steps using the `1_Setup.ipynb` notebook. All the data is extracted from the zipped folder. Then, all the necessary data cleaning operations are performed, using the information provided by the authors of the dataset. Further information on the dataset can be found in the [official paper](https://www.nature.com/articles/s41597-021-00937-4).

ATTENTION: Make sure to replace the paths with the specific ones for your machine.

### Step 3. Audio pre-processing

In the `2_Preprocessing.ipynb` notebook, all the required audio preprocessing steps are performed. In particular, operations were carried out to remove background noise, remove silence, and standardize the length of the audio tracks.


## Data Augmentation

Given the imbalance of the dataset, data augmentation techniques are proposed to increase the size of the minority class. Pitch shift, shift, gain, and time stretch techniques are proposed. All operations are inside the notebook `3_DataAugmentation.ipynb`


## Feature Extraction

In the `4_FeatureExtraction.ipynb` notebook, MFCC coefficients for audio classification are extracted for both original and augmented audio.


## Training

In the `5_ModelTraining.ipynb` notebook you can find the script for the training of the proposed CNN.


## Results

As can be seen in the [Report](https://www.slideshare.net/GianlucaCavallaro3/medical-data-management-covid19-detection-using-cough-recordings-chest-xrays-classification-and-generation), the results obtained are not satisfactory. The obtained results could be influenced by the poor quality of the original dataset, as it is a crowd-sourced dataset (tracks are recorded using only [this interface](https://coughvid.epfl.ch/), and the quality of the tracks has been evaluated only for 1000 items of the dataset). In the future, we will try to improve this work by trying to get our hands on a higher quality dataset, as well as attempting different approaches for audio track processing, such as applying SpecAugment.


# Contributors

* [Gianluca Cavallaro](https://github.com/Gianluca124) 
* [Giorgio Carbone](https://github.com/giocoal) 
* [Remo Marconzini](https://github.com/rmarconzini)
