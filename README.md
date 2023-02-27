# COVID-19 detection using cough recording

## Table of contents
* [Abstract](#abstract)
* [Report](https://www.slideshare.net/GianlucaCavallaro3/medical-data-management-covid19-detection-using-cough-recordings-chest-xrays-classification-and-generation)
* [Requirements](#requirements)
* [Pre-processing](#pre-processing)
* [Classification](#classification)
* [Clustering](#clustering)
* [Results](#results)

## Abstract

This is the first part of the project which also includes the work shown in [chest x-ray classification using GANs](https://github.com/Gianluca124/CXR-ACGAN-chest-xray-generator-covid19-pneumonia).

## Requirements

- python==3.8
- ipython
- ipykernel
- matplotlib
- pandas
- nltk
- gensim
- scikit-learn==1.2.0
- textblob
- yellowbrick


## Pre-processing

### Step 1. Download and extract the dataset

Download the dataset from the [official Kaggle Folder](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews).

### Step 2. Perform class splitting of the dataset
Perform all the necessary pre-processing steps using `Preprocessing.ipynb` notebook.


## Classification

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
