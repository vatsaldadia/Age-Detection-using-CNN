
# Age Detection Using Convolutional Neural Networks  

## Overview

This repository focuses on an AI project for **age detection from facial images** using Convolutional Neural Networks (CNNs). It includes Jupyter notebooks for data preprocessing, training, and evaluation of models like **VGGNet**, **DenseNet**, and **EfficientNet** on diverse datasets (**Adience** and **UTKFace**). The repository handles tasks such as cleaning noisy images, applying augmentations, and training models to classify images into predefined age groups. Reports provide a detailed comparative analysis of model performances, metrics, and visualizations.

## Datasets

We used the following datasets to train and test the models:

- UTKFace Dataset: 20,000 images across 15 balanced age groups.
- Adience Dataset: 19,400 natural images distributed into 8 age groups.
- FacialAge Dataset: 9,778 images divided into 4 broad age groups.
The images were preprocessed (cropping, alignment, and resizing to 224x224) and augmented for better generalization.

## Project Links

- [GitHub Repository](https://github.com/vatsaldadia/comp6721_project)
- [Video Presentation](https://drive.google.com/file/d/1wYOFcui9W8cbsqQ7X2nkmptP9I8plJlX/view?usp=drive_link)


## CNN Architectures Used
- VGGNet-16:
Deep architecture with uniform 3x3 convolutional layers.
Activations: ReLU with max-pooling.
- DenseNet-121:
Utilizes dense connectivity where each layer connects to all previous layers.
Efficient feature reuse across layers.
- EfficientNet:
Computationally efficient using depthwise separable convolutions.
Captures fine details such as wrinkles and textures using global pooling.

## How to Run this Project

To run this project check on the file named [HOW_TO_RUN.md](HOW_TO_RUN.md)

## Methodology
### Preprocessing:
Images resized to 224x224.
Normalization applied as per ImageNet standards.
Data augmentation: random rotations, flips, color jittering, and brightness adjustments.
### Training:
Optimizer: Adam Optimizer (Learning rate = 0.001, step scheduling applied).
Loss Function: Cross-Entropy Loss.
Batch Size: 32 | Epochs: 5, 10, and 20.
Early stopping used to prevent overfitting.

### Evaluation Metrics
- Accuracy: Overall classification performance.
- Precision, Recall, and F1 Score: Detailed analysis using classification reports.
- Visualization: t-SNE for feature embeddings and loss vs. epoch curves.

### Results
- EfficientNet achieved the best accuracy and computational efficiency across all datasets.
- VGGNet underperformed compared to DenseNet and EfficientNet.
- Generalizability challenges observed when using transfer learning from ImageNet weights.
