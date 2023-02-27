# COVID-19 detection using cough recording

## Table of contents
* [Abstract](#abstract)
* [Report](https://www.slideshare.net/GianlucaCavallaro3/medical-data-management-covid19-detection-using-cough-recordings-chest-xrays-classification-and-generation)
* [Requirements](#requirements)
* [Pre-processing](#pre-processing)
* [Data Augmentation](#data-augmentation)


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

In the `Classification.ipynb` notebook both binary and multi-class classification are performed. For both tasks several algorithm are proposed.


## Clustering

In the `Clustering.ipynb` notebook the clustering task is proposed via K-Means clustering and Agglomerative Clustering.


## Results

Check out the [Google Drive folder](https://drive.google.com/drive/u/1/folders/1veNClNl7CxCTFHVNY2Fp29hcMoEj-the) with all the trained models and results.

## Status

 Project is: ![##c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)  _Done_


# Contributors

* [Gianluca Cavallaro](https://github.com/Gianluca124)  
* [Remo Marconzini](https://github.com/rmarconzini)
