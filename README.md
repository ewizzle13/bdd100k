# Waymo Nighttime Object Detection Project

## Overview

This project focuses on building and evaluating a **deep learning (CNN-based) model** using the Waymo Open Dataset, with a specific emphasis on **nighttime driving conditions**.

The goal is to analyze how well object detection models perform in **low-light environments**, which present unique challenges such as reduced visibility, noise, and decreased feature clarity.

---

## Objectives

* Extract and preprocess Waymo dataset frames
* Filter data to include **nighttime driving scenarios only**
* Build a **Conv2D-based deep learning model**
* Evaluate model performance using standard metrics
* Analyze challenges of object detection in low-light conditions

---

## Dataset

* **Source:** Waymo Open Dataset
* **Format:** `.tfrecord` files
* **Data Used:**

  * Camera images
  * Object labels (vehicles, pedestrians, cyclists)
* **Filtering Criteria:**

  * `time_of_day == "Night"`

---

## Methodology

### 1. Data Processing

* Parsed Waymo `.tfrecord` files
* Extracted image frames from camera sensors
* Filtered frames using metadata (`time_of_day`)
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

---

### 3. Training

* Loss Function: Binary / Categorical Crossentropy (based on label structure)
* Optimizer: Adam
* Evaluation Metrics:

  * Accuracy
  * Precision
  * Recall
  * F1-score

---

## Results

* Evaluated model performance on **nighttime-only data**
* Compared model accuracy under low-light conditions
* Identified limitations in detecting objects with reduced visibility

---

## Key Insights

* Nighttime conditions significantly impact detection accuracy
* Feature extraction is more challenging due to lighting constraints
* Model performance depends heavily on preprocessing and data quality

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy / Pandas
* Waymo Open Dataset

---

## Contributors

* **Tigist Tefera**
* **Meghan Garcia**
* **E’niya Madden**

---

## Future Work

* Improve performance using data augmentation for low-light conditions
* Explore transfer learning with pretrained models
* Implement more advanced detection architectures (e.g., YOLO, Faster R-CNN)
**Extend analysis to different weather and lighting conditions** (We can talk about this)

---

## Summary

This project demonstrates the challenges and considerations of applying deep learning models to **real-world autonomous driving data**, particularly in **nighttime environments**, and highlights the importance of robust model design for safety-critical applications.
