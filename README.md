# Improving MOS Prediction in Mobile Networks: A Segmentation-Based Approach

This project analyzes the Poqemon-QoE-Dataset (https://github.com/Lamyne/Poqemon-QoE-Dataset/tree/master) to predict the Mean Opinion Score (MOS) for video streaming in mobile networks.

The core idea is to move from a single, global prediction model to a user-centric approach. By first segmenting users based on their behavior and network conditions, we can build more accurate and specialized models for each user group.

## Project Goal

The goal is to improve MOS prediction by:

* Training machine learning models to 
* Identifying distinct user clusters (segments) within the dataset using unsupervised learning.
predict MOS.
* Analyzing the performance and feature importance for different user segments.

---

## Methodology

### 1. Predictive Modeling
A Random Forest classifier was trained on the entire dataset to predict the MOS value. Model performance was evaluated using a confusion matrix, and feature importance was calculated to understand the key drivers of QoE.

### 2. User Segmentation
A K-Means clustering algorithm was applied to key user features to segment users into three distinct groups. These groups were analyzed and identified as:

**Cluster 0 (Standard Users)**: Average performance across metrics.
**Cluster 1 (Premium User Group)**: Characterized by high bitrate and framerate, with a relatively high MOS[cite: 3].
**Cluster 2 (Frustrated User Group)**: Suffered from high buffering and low framerates, resulting in the lowest average MOS.


---

## Key Findings

**User-Centric Approach is Validated**: The three user clusters show significant variations in experience (MOS) and underlying technical factors (bitrate, buffering).
**"One-Size-Fits-All" is Suboptimal**: The report concludes that a single, global model is not ideal, as different user groups are sensitive to different quality factors.
**Feature Importance**: The initial Random Forest model identified key features like buffering and bitrate as highly important for predicting MOS.

---
