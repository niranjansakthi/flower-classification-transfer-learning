🌸 Flower Image Classification using Transfer Learning
Overview

This project is a deep learning-based image classification system that identifies five different flower categories:

Roses
Daisy
Dandelion
Sunflowers
Tulips

Instead of training a convolutional neural network from scratch, the project uses Transfer Learning with MobileNetV2, allowing the model to leverage knowledge learned from millions of images in the ImageNet dataset.

Problem Statement

Image classification models typically require large datasets and extensive training time.

This project explores how Transfer Learning can be used to build an accurate image classifier using a relatively small flower dataset while reducing training costs and improving performance.

Technologies Used
Python
TensorFlow
Keras
OpenCV
NumPy
Scikit-Learn
MobileNetV2
Deep Learning Concepts Implemented
Data Preprocessing
Image loading using OpenCV
Image resizing
Dataset creation
Train-test split
Pixel normalization
Data Augmentation

To reduce overfitting and improve generalization:

Random Horizontal Flip
Random Rotation
Random Zoom
Transfer Learning

Used pretrained MobileNetV2 trained on ImageNet.

Key steps:

Loaded pretrained weights
Removed classification head
Froze pretrained layers
Added custom classification layers
Regularization
Dropout layer to reduce overfitting
Classification

Multi-class image classification with:

Softmax output layer
Sparse Categorical Cross Entropy Loss
Model Architecture
Input Image (180x180x3)
        ↓
Data Augmentation
        ↓
MobileNetV2 (Pretrained)
        ↓
GlobalAveragePooling2D
        ↓
Dropout(0.2)
        ↓
Dense(5)
        ↓
Flower Prediction
Dataset

TensorFlow Flower Photos Dataset

Classes:

Roses
Daisy
Dandelion
Sunflowers
Tulips
