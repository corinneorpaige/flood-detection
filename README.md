# Utilizing Convolutional Neural Nets for Flood Detection

## Data from *Building Damage Annotation on Post-Hurricane Satellite Imagery Based on Convolutional Neural Networks* by Quoc Dung Cao and Youngjun Choe (2020)
[Link to files on Kaggle](https://www.kaggle.com/datasets/kmader/satellite-images-of-hurricane-damage)

## Main Motivation
Floods can be incredibly devastating, so being able to quickly and appropriately allocate aid is imperative. Locating regions that have more or less damage is an important part of correctly distributing resources. Satellite images using optical sensors are much easier to attain than information from synthetic aperture radar sensors, the current solution for damage assessment. Utilizing a more readily-available source of data along with a high-performing model could improve current damage identification methods for future disasters, helping relief organizations with their responses. 

## Goal
We sought to create a model that would accurately detect flood-damaged buildings after Hurricane Harvey in Houston, TX.

## General Methodology
Chose to test multiple convolutional neural networks for image prediction:
- Model 0 had 1 convolutional and 1 pooling layer, 3x3 window
- Model 1 had the same layer structure, 5x5 window
- Model 2 had 2 convolutional and 2 pooling layers, 3x3 window
- Model A was Model 2 with 3 layers of dropout (0.25, 0.25, 0.5)
- Model B was Model 2 with 3 layers of dropout (0.5, 0.5, 0.5)
- Model 3 had 3 convolutional and 3 pooling layers, 3x3 window

## Results
Our best model was #3. We received a testing accuracy of 98% and a training accuracy of 99.1% - slight overfit.

### References for Paper and Presentation
- https://ieee-dataport.org/open-access/detecting-damaged-buildings-post-hurricane-satellite-imagery-based-customized
- https://arxiv.org/pdf/1807.01688.pdf
- https://www.frontiersin.org/articles/10.3389/frai.2020.534696/full
- https://www.scientificamerican.com/article/new-maps-show-us-flood-damage-rising-26-percent-in-next-30-years/
- https://www.bbc.com/news/av/world-europe-61325769
- https://www.reuters.com/world/asia-pacific/half-million-face-flood-evacuation-sydney-braces-more-heavy-rains-2022-03-02/
- https://www.npr.org/2021/07/25/1020342822/flooding-continues-to-devastate-zhengzhou-city-in-central-china

### References for Code
- Code mainly taken from *Deep Learning with Python* by Francois Chollet
- https://towardsdatascience.com/convolutional-neural-networks-in-practice-406426c6c19a
- https://www.tensorflow.org/guide/keras/save_and_serialize
- https://stackoverflow.com/questions/66221788/tf-gradients-is-not-supported-when-eager-execution-is-enabled-use-tf-gradientta
- https://machinelearningmastery.com/how-to-visualize-filters-and-feature-maps-in-convolutional-neural-networks/
- https://stats.stackexchange.com/questions/147850/are-pooling-layers-added-before-or-after-dropout-layers

## Data Citation
Quoc Dung Cao, Youngjun Choe, December 13, 2018, "Detecting Damaged Buildings on Post-Hurricane Satellite Imagery Based on Customized Convolutional Neural Networks", IEEE Dataport, doi: https://dx.doi.org/10.21227/sdad-1e56.
