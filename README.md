# Improving MOS Prediction in Mobile Networks: A Segmentation-Based Approach

This project analyzes the Poqemon-QoE-Dataset to predict the Mean Opinion Score (MOS) for video streaming in mobile networks.

The core idea is to move from a single, global prediction model to a user-centric approach. By first segmenting users based on their behavior and network conditions, we can build more accurate and specialized models for each user group.

## Project Goal

The goal is to improve MOS prediction by:

* Training machine learning models to 
* Identifying distinct user clusters (segments) within the dataset using unsupervised learning.
predict MOS.
* Analyzing the performance and feature importance for different user segments.

---

## Methodology

### 1. User Segmentation
[cite_start]A K-Means clustering algorithm was applied to key user features to segment users into three distinct groups[cite: 3]. These groups were analyzed and identified as:

* [cite_start]**Cluster 0 (Standard Users)**: Average performance across metrics[cite: 3].
* [cite_start]**Cluster 2 (Frustrated User Group)**: Suffered from high buffering and low framerates, resulting in the lowest average MOS[cite: 3].

### 2. Predictive Modeling
[cite_start]A Random Forest classifier was trained on the entire dataset to predict the MOS value[cite: 1]. [cite_start]Model performance was evaluated using a confusion matrix, and feature importance was calculated to understand the key drivers of QoE[cite: 1].

---

## Key Findings

* [cite_start]**User-Centric Approach is Validated**: The three user clusters show significant variations in experience (MOS) and underlying technical factors (bitrate, buffering)[cite: 2, 3].
* [cite_start]**"One-Size-Fits-All" is Suboptimal**: The report concludes that a single, global model is not ideal, as different user groups are sensitive to different quality factors[cite: 2].
* [cite_start]**Feature Importance**: The initial Random Forest model identified key features like buffering and bitrate as highly important for predicting MOS[cite: 1].

---

## How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [YOUR_REPO_URL]
    cd [YOUR_PROJECT_NAME]
    ```

2.  **Create a virtual environment (Recommended):**
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows, use `env\Scripts\activate`
    ```

3.  **Install the required libraries:**
    (You should create a `requirements.txt` file for this)
    ```bash
    pip install pandas numpy matplotlib scikit-learn jupyter
    ```

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```

5.  **Run the notebooks:**
    Open the `notebooks/` folder and run the notebooks in order:
    1.  `User-Centric Modeling.ipynb` (to perform segmentation)
    2.  `exploration_preprocessing_models.ipynb` (to run the predictive model)

---

## Future Work

[cite_start]As recommended in the project report, the critical next step is to build separate, dedicated prediction models for each of the three identified user clusters[cite: 2]. [cite_start]This approach is expected to substantially increase prediction accuracy for each specific segment by allowing the models to learn the unique feature weights relevant to each group[cite: 2].
