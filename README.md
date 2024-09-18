# Brain Tumor Classification with CNN

## Project Overview
This project is aimed at building a Convolutional Neural Network (CNN) to classify brain MRI images into two categories:
Brain tumor detected
No brain tumor detected
The goal is to automate the detection of brain tumors from MRI scans using deep learning techniques, specifically CNNs, to assist in early diagnosis and treatment planning.

Dataset
The dataset consists of MRI images of brain scans, categorized into two classes:

<a href="https://drive.google.com/drive/folders/1UH61lf55bBR-jEQ6u9GdpkT_aFo3MNaW?usp=drive_link">Tumor</a>: MRI images showing the presence of a brain tumor.

<a href="https://drive.google.com/drive/folders/1SDuVwytGl6HHAsi-2NTUuiO2zMOvtxPb?usp=drive_link">No Tumor</a>: MRI images showing no signs of a brain tumor.
<br>
You can download the dataset from here or use your own labeled dataset for training.

```Dataset Structure:
bash

brain_tumor_dataset/
│
├── train/
│   ├── tumor/
│   └── no/
│
└── test/
    ├── tumor/
    └── no/
```
## Requirements

Make sure you have the following dependencies installed:

bash
```
pip install numpy
pip install tensorflow
pip install keras
pip install matplotlib
pip install scikit-learn
```
## Model Architecture

The CNN architecture is designed to perform binary classification. The key layers used in the architecture are:

Convolutional Layers: For feature extraction from images.
MaxPooling Layers: To downsample the image features.
Dense Layers: To perform the classification.
Dropout: For regularization to prevent overfitting.

## The model uses the following structure:

Input Layer: 224x224 images (preprocessed).
3 Convolutional layers followed by MaxPooling layers.
Flatten Layer to convert the features into a 1D vector.
Dense Layers: Fully connected layers for classification.
Output Layer: Sigmoid activation for binary classification (tumor/no tumor).

## Preprocessing

The images are preprocessed before being fed into the model:

Resized to 224x224 pixels.
Converted to arrays and normalized by dividing by 255 to scale pixel values between
0 and 1.

## Future Improvements

Model Optimization: Further optimize the CNN architecture for better performance.
Data Augmentation: Experiment with different augmentation techniques to improve the model's robustness.
Transfer Learning: Apply transfer learning with pre-trained models like VGG16 or ResNet to improve accuracy.
<br>
## Conclusion
This project provides a basic CNN model for binary classification of brain MRI images to detect the presence of brain tumors. With further tuning and dataset improvements, this model can be a useful tool for early diagnosis of brain tumors.
