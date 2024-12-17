# Melanoma Skin Cancer Detection

## Abstract
Among over 200 forms of cancer, melanoma is the deadliest type of skin cancer. The diagnostic process for melanoma begins with clinical screening, followed by dermoscopic analysis and histopathological examination. Early identification significantly increases the curability of melanoma skin cancer. The initial step involves a visual examination of the affected skin area, during which dermatologists capture dermatoscopic images of skin lesions using high-speed cameras. These images achieve an accuracy rate of 65–80% in diagnosing melanoma without additional technical support. With further visual analysis by cancer specialists, the diagnosis accuracy improves to 75–84%. This project aims to develop an automated classification system using image processing techniques to classify skin cancer from skin lesion images effectively.

## Problem Statement
The current diagnostic process for melanoma involves a skin biopsy, where a dermatologist examines a portion of the skin lesion under a microscope. This procedure, from scheduling a dermatologist's appointment to receiving biopsy results, typically takes a week or more. The objective of this project is to reduce this timeline to just a couple of days by leveraging a predictive model. The approach utilizes a Convolutional Neural Network (CNN) to classify nine types of skin cancer from lesion images. This accelerated process has the potential to positively impact millions of lives.

## Motivation
The primary aim of this project is to contribute to reducing deaths caused by skin cancer. The driving motivation is to leverage advanced image classification technology for the betterment of society. Recent advancements in computer vision, powered by scalable machine learning and deep learning techniques, present an opportunity to make a significant difference in melanoma detection and treatment.

## Dataset
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

![datasetdf](https://github.com/vikrant19y/Melanoma_Detection/blob/main/ReadMe_Images/Count.png)

![datasetplot](https://github.com/vikrant19y/Melanoma_Detection/blob/main/ReadMe_Images/Plot_count.png)

To overcome the issue of class imbalance, used a python package Augmentor (https://augmentor.readthedocs.io/en/master/) to add more samples across all classes so that none of the classes have very few samples.

## Sample Image from Dataset
![SampleImages](https://github.com/vikrant19y/Melanoma_Detection/blob/main/ReadMe_Images/Visualization.png)

## CNN Architecture Design

To classify skin cancer using skin lesion images, I developed a custom CNN model for higher accuracy. Key components include:

- Rescaling Layer: Normalizes input data from the [0, 255] range to [0, 1].
- Convolutional Layer: Applies convolutions to extract features, reducing image size while retaining key information.
- Pooling Layer: Reduces the dimensions of feature maps to decrease computation and parameters.
- Dropout Layer: Randomly sets input units to 0 to prevent overfitting.
- Flatten Layer: Converts feature maps into a 1D array for the fully connected layer.
- Dense Layer: Deeply connected layer where each neuron receives input from all neurons in the previous layer.
- Activation Functions:
    - ReLU: Outputs positive input directly, aiding faster learning by overcoming the vanishing gradient problem.
    - Softmax: Used in the output layer to predict probabilities, ensuring outputs range between 0 and 1 and sum to 1.

### Model Architecture

![modelArchitecture](https://github.com/vikrant19y/Melanoma_Detection/blob/main/ReadMe_Images/model_plot.png)

![outputplot](https://github.com/vikrant19y/Melanoma_Detection/blob/main/ReadMe_Images/output.png)

## Model Evaluation

![Accuracy_plot](https://github.com/vikrant19y/Melanoma_Detection/blob/main/ReadMe_Images/Model_Accuracy.png)


