## Project Overview

This project focuses on classifying bird species based on their sound using neural networks. The primary goal is to train deep learning models to accurately identify bird species from audio clips, which can be valuable for environmental monitoring and species surveillance.
The study utilizes a dataset of bird sounds collected from the Xeno-Canto archive, specifically curated from a Birdcall competition. This dataset comprises 10 sound clips for each of 12 distinct bird species.



## Methodology

The core methodology involves:

Data Preprocessing: Converting raw audio clips into spectrograms, which are visual representations of audio frequencies over time. Each spectrogram is resized to 343×256 pixels.

Model Building: Developing and training Convolutional Neural Networks (CNNs) for both binary and multi-class classification tasks.

Binary Classification: Two CNN models were built to distinguish between "American Crow" (amecro) and "Blue Jay" (blujay). 

Multi-class Classification: Two CNN models were developed to classify all 12 bird species.

Model Evaluation: Assessing the performance of the trained models based on accuracy and loss metrics on both training and test datasets.

External Test Data Prediction: Using the best-performing multi-class model to predict bird species from three external raw sound clips. 


## Dataset

The dataset consists of audio clips from the following 12 bird species:

American Crow (amecro)

Barn Swallow (barswa)

Black-capped Chickadee (bkcchi)

Blue Jay (blujay)

Dark-eyed Junco (daejun)

House Finch (houfin)

Mallard (mallar3)

Northern Flicker (norfli)

Red-winged Blackbird (rewbla)

Stellar's Jay (stejay)

Western Meadowlark (wesmea)

White-crowned Sparrow (whcspa)



## Technologies and Libraries

Python

TensorFlow / Keras 

Numpy 

Pandas 

Matplotlib 

Scikit-learn (for data splitting and scaling) 

Librosa (for audio loading and feature extraction) 

HDF5 (for storing preprocessed spectrograms) 


## Computational Results

### Binary Model Performance
The following table summarizes the performance of the two binary classification models:

| | Training Accuracy | Test Accuracy | Train Loss | Test Loss |
|---|---|---|---|---|
| **Model 1** | 95.06%  | 100%  | 10.55% | 2.63% |
| **Model 2** | 100%  | 95.24% | 2.30% | 5.10% |

### Multi-class Model Performance
The following table summarizes the performance of the two multi-class classification models:

| | Training Accuracy | Test Accuracy | Training Loss | Test Loss |
|---|---|---|---|---|
| **Model 1** | 99.01% | 66.09% | 0.03% | 4.81% |
| **Model 2** | 100% | 68.39% | 0.00% | 5.51% |

### External Test Data Predictions
The multi-class model was used to predict species in three external raw sound clips. The top predicted species and their probabilities are shown below:

**Test 1**

| Species | Probability |
|---|---|
| American Crow (amecro) | 52.60% |
| Northern Flicker (norfli) | 45.98% |

**Test 2**

| Species | Probability |
|---|---|
| American Crow (amecro) | 51.60% |
| Northern Flicker (norfli) | 47.85% |

**Test 3**

| Species | Probability |
|---|---|
| Northern Flicker (norfli) | 57.29% |
| American Crow (amecro) | 42.28% |



## Key Findings
The binary classification models achieved excellent performance, with one model reaching 100% test accuracy.


The multi-class classification models demonstrated a reasonable accuracy of up to 68.39% for identifying 12 different bird species.


External test clips confirmed the ability of the multi-class model to detect multiple bird species within a single audio recording. The results indicated the presence of multiple bird species calls in each test clip, with "American Crow" and "Northern Flicker" being the most probable species identified.
