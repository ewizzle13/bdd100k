# BDD100K Scene Classification using Deep Learning

## Overview

This project focuses on building and evaluating a **deep learning (CNN-based) model** using the BDD100K dataset.


Scene classification is a critical task in computer vision that enables autonomous vehicles to interpret their surroundings by categorizing environments such as highways, residential areas, city streets, tunnels, and parking lots.

Initially, the Waymo dataset was considered; however, due to challenges with TFRecord formatting and data preprocessing, the project transitioned to BDD100K, which provided a more structured and accessible dataset.

---

## Objectives

* Develop and train deep learning models for scene classification
* Preprocess and prepare the BDD100K dataset for model training
* Build a **Conv2D-based deep learning model**
* Evaluate model performance using standard metrics
* Analyze challenges such as overfitting and dataset limitations

---

## Dataset

Source: BDD100K Scenario Classification Dataset

The dataset is a large-scale driving dataset designed for computer vision tasks in autonomous driving.

Dataset Features:
Organized into training, validation, and testing directories
Original test folder was empty, requiring a custom data split
Contains 7 scene classes:
Parking lot
Gas station
Residential
City street
Highway
Tunnel
Unknown

---

## Methodology

### 1. Data Processing

* Resized images to 224 × 224 (160 for VGG)
* Normalized pixel values to [0, 1]
* Batch size: 32
* Normalized image data

---

### 2. Model Architecture

* Convolutional Neural Network (CNN)
* Key components:

  * Conv2D layers for feature extraction
  * ReLU activation for non-linearity
  * MaxPooling for dimensionality reduction
  * Global Average Pooling
  * Dense output layer for classification

 A simplified VGG-style CNN used as a baseline for comparison.

Key Components:

*Stacked convolutional blocks (32 → 64 → 128 → 256 filters)
*Max-pooling layers
*Global Average Pooling
*Dense + Dropout layers
*Softmax output (7 classes)

---

### 3. Training

*Loss Function: Sparse Categorical Crossentropy
*Optimizer: Adam
*Learning Rate: 0.0001
*Batch Size: 32
*Epochs: 10
*Evaluation Metrics:
*Accuracy
*Training Loss
*Validation Loss

---

## Results

* Evaluated model performance on BDD100K scene classification dataset
* Compared performance of models
* Observed higher accuracy with ResNet, but with signs of overfitting, VGG achieved stable and consistent performance across epochs

---

## Key Insights

* Overfitting is a major challenge, especially with similar images
* Model architecture impacts performance
* Model performance depends heavily on preprocessing and data quality

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy / Pandas
* BDD100K Dataset

---

## Contributors

* **Tigist Tefera**
* **Meghan Garcia**
* **E’niya Madden**

---

## Future Work

* Apply data augmentation to improve generalization
* Explore transfer learning with pretrained models
* Implement more advanced detection architectures (e.g., YOLO, Faster R-CNN)
**Extend analysis to:

Different weather conditions
Day vs night classification

---

## Summary

This project demonstrates the application of deep learning models to scene classification in autonomous driving environments.
Overall, the project highlights the importance of model selection, dataset quality, and preprocessing in building reliable computer vision systems.
