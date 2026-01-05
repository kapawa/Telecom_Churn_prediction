# Telecom Customer Churn Prediction

## Overview
This project performs end-to-end data analysis and supervised learning to predict customer churn using a telecom dataset of 7,000+ customers.

## Dataset
- Telecom customer dataset with demographic, service, and billing features
- Binary classification task (churn vs non-churn)

## Approach
- Data cleaning and preprocessing
- Feature engineering, encoding, scaling, and missing-value imputation
- Model comparison to identify optimal churn predictors

## Models
- Logistic Regression
- K-Nearest Neighbors (KNN)

## Results
- Logistic Regression achieved 78% accuracy and 0.72 macro F1-score
- Outperformed KNN (73% accuracy, 0.43 F1-score)
- Identified ~58% of churners, supporting data-driven retention strategies

## Tools & Technologies
Python, Pandas, NumPy, Scikit-learn, Matplotlib

## How to Run
```bash
pip install -r requirements.txt
