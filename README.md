# Helmet Detection for Road Safety Using Convolutional Neural Networks

## Project Overview

Currently accidents on roads involving motorcyclists remain a major safety concern around the world.  Wearing safety helmets helps to reduce the risk of severe head injuries and deaths to a large extent. The main challenge is the accurate detection and monitoring of helmet usage among motorcycle riders, particularly in crowded environments and high-traffic areas, where manual observation becomes difficult and inefficient. Recent development in Artificial Intelligence (AI) and Deep Learning have made it possible to create automated image processing systems which can spot safety violations in real time. 

The main goal of this study is to develop a Convolutional Neural Network (CNN)-based image classification model to automatically identify whether a motorcycle rider is wearing a helmet or not. Such systems can assist traffic authorities in implementing safety regulations and improving road safety. 


## Problem Statement

Manual monitoring of helmet compliance is laborious, time-consuming, and difficult to implement consistently in high-traffic places. With this continuous growth of intelligent transportation systems, there is a need for an automated and effective solution that can identify helmet usage from images captured by traffic monitoring cameras. 

This project resolves this challenge by developing a deep learning-based helmet detection system using Convolutional Neural Networks (CNNs). This system automatically classifies rider images into two categories: With Helmet and Without Helmet. The performance of the proposed CNN model is further evaluated and compared with a MobileNetV2-based transfer learning model to determine its suitability for real-world road safety monitoring and traffic enforcement applications. 

---

### Dataset
Helmet Detection Dataset

### Dataset Description

The Helmet Detection dataset contains images of motorcycle riders collected for road safety and helmet compliance monitoring. Every image in the dataset comes along with an XML annotation file that provides object labels, and bounding box coordinates identifying rider head regions. From the annotations, it can understand whether the rider is wearing a helmet or not, making the dataset suitable for supervised image classification tasks. 
The dataset contains motorcycle rider images along with XML annotation files that provide:

- Object labels
- Bounding box coordinates
- Helmet usage information

During preprocessing:

- XML annotations are parsed
- Rider head regions are cropped using bounding boxes
- Images are resized to 224 × 224 pixels
- Images are normalized before training

### Dataset Summary

| Property | Value |
|-----------|--------|
| Total Images | 1434 |
| Image Size | 224 × 224 |
| Number of Classes | 2 |

### Class Distribution

| Class | Count |
|---------|---------|
| Without Helmet | 482 |
| With Helmet | 952 |

### Image Type

- RGB Images
- JPEG Format
- Resized to 224 × 224 pixels

---

## Research Questions

- Can a custom CNN accurately classify helmet and non-helmet rider images?
- How effective is data augmentation in improving model performance?
- How does a custom CNN compare with MobileNetV2 for helmet detection?
- Can Grad-CAM provide visual explanations for model predictions?
- Which model provides better accuracy for road safety applications?

---

## Proposed Methodology

The project follows the following workflow:

1. Dataset Collection
2. XML Annotation Parsing
3. Image Cropping using Bounding Boxes
4. Image Resizing (224 × 224)
5. Pixel Normalization
6. Dataset Splitting
   - Training Set (70%)
   - Validation Set (15%)
   - Test Set (15%)
7. Data Augmentation
8. CNN Model Development
9. Model Training
10. Model Evaluation
11. Grad-CAM Visualization
12. Model Comparison

---

## CNN Architecture

The custom CNN architecture consists of:

- Input Layer (224 × 224 × 3)
- Conv2D (32 Filters) + ReLU
- MaxPooling2D
- Conv2D (64 Filters) + ReLU
- MaxPooling2D
- Conv2D (128 Filters) + ReLU
- MaxPooling2D
- Conv2D (256 Filters) + ReLU
- Global Average Pooling
- Dense Layer (64 Neurons)
- Dropout (0.3)
- Output Layer (Sigmoid)

---

## Transfer Learning Model

### MobileNetV2

MobileNetV2 was used as a transfer learning model for comparison purposes. The model serves as a feature extractor followed by additional dense and dropout layers for binary classification.

---

## Evaluation Metrics

The following metrics were used:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC Curve
- AUC Score
- Classification Report

---

## Results

### CNN Performance

| Metric | Value |
|----------|----------|
| Accuracy | 74.07% |

### MobileNetV2 Performance

| Metric | Value |
|----------|----------|
| Accuracy | 66.20% |

### Model Comparison

| Model | Accuracy |
|----------|----------|
| CNN | 74.07% |
| MobileNetV2 | 66.20% |

The custom CNN achieved higher accuracy than MobileNetV2 on the helmet detection dataset.

---

## Output Figures

The project generates the following outputs:

- Sample Rider Images
- Dataset Distribution
- CNN Architecture
- Training Accuracy Curve
- Validation Accuracy Curve
- Training Loss Curve
- Validation Loss Curve
- Confusion Matrix
- ROC Curve
- Grad-CAM Visualization
- CNN vs MobileNetV2 Accuracy Comparison 

---

## Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
---

## How to Run

1. Download the dataset.or Jupyter Notebook.
3. Install required libraries.
4. Run all notebook cells sequentially.
5. Generated figures and trained models will be saved automatically.

---

## Conclusion

This project successfully developed a CNN-based helmet detection system for road safety applications. The custom CNN achieved an accuracy of 74.07%, outperforming MobileNetV2, which achieved an accuracy of 66.20%.

The results demonstrate that deep learning techniques can effectively support automated traffic monitoring and helmet compliance enforcement. Future work may include larger datasets, advanced transfer learning models, and real-time deployment for intelligent transportation systems.

