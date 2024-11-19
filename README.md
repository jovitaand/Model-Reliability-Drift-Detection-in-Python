# Drift Detection in Machine Learning Models

This project explores the concept of **drift** in machine learning, specifically focusing on **data drift** and **concept drift**. Using the Evidently library, we detect and monitor data drift in a healthcare dataset and simulate synthetic production data to evaluate the robustness of drift detection.

## Overview

Drift refers to changes in the statistical properties of data that can degrade the performance of machine learning models over time. It is categorized into:
1. **Concept Drift**: Changes in the relationship between input features and target variables.
2. **Data Drift**: Changes in the distribution of input features.

The project demonstrates:
- Identification of drift in numerical and categorical features.
- Application of drift detection tools using Evidently.
- Strategies to simulate drift and interpret detection results.

## Tools and Technologies

- **Python**: For data preprocessing, model training, and analysis.
- **Evidently**: An open-source library for drift detection and monitoring.
- **Scikit-learn**: For machine learning model development.
- **Matplotlib & Seaborn**: For data visualization.

## Dataset

The dataset is sourced from the UCI Machine Learning Repository and contains healthcare data with features such as patient demographics, medical conditions, and treatment outcomes. The target variable is readmission within 30 days.

## Key Features

1. **Baseline Model Training**:
   - Logistic regression model trained on historical data.
   - Evaluation using metrics like balanced accuracy and ROC-AUC.

2. **Drift Simulation**:
   - Synthetic drift introduced in numerical (e.g., `num_lab_procedures`) and categorical (e.g., `gender_Female`) features.
   - Analysis of drift impact on the dataset.

3. **Drift Detection**:
   - Evidently used to generate drift reports.
   - Statistical tests applied to identify changes in feature distributions.

## Example Results

### Before Drift
- No drift detected across features.
- Baseline performance maintained.

### After Drift
- Drift detected in `num_lab_procedures` (numerical) and `gender_Female` (categorical).
- Increased share of drifted columns reflects data changes.

## How to Use

1. Clone this repository:
   ```bash
   git clone <repository_url>
    ```
2. Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook
    ```
4. Explore the Evidently reports to understand drift impact

## References

- [Evidently AI Documentation](https://docs.evidentlyai.com)
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php)


