# Telecom Customer Churn Prediction

## Project Overview

Customer churn is a major challenge for telecommunications companies, as losing existing customers can increase acquisition costs and reduce recurring revenue.

This project develops machine learning models to predict customer churn and identify high-risk customers who could be prioritized for retention initiatives.

Beyond classification performance, the project evaluates how predictive modeling can support business decisions through customer risk ranking and targeted retention strategies.

## Business Objectives

- Predict which customers are most likely to churn.
- Compare Logistic Regression and K-Nearest Neighbors (KNN) for churn classification.
- Identify patterns associated with customer churn.
- Evaluate how predictive risk scores can help prioritize customer retention efforts.

## Dataset

The project uses the Telco Customer Churn dataset, containing **7,043 customer records**.

The dataset includes customer information such as:

- Demographic characteristics
- Contract types and tenure
- Internet and additional service subscriptions
- Monthly and total charges
- Payment methods
- Customer churn status

**Target Variable:** `Churn` (Yes/No)

## Methodology

### 1. Data Preprocessing

- Data cleaning and missing-value handling
- Categorical feature encoding
- Numerical feature scaling
- Feature engineering
- Train-test splitting

### 2. Model Development

Two supervised machine learning algorithms were evaluated:

**Logistic Regression**
- Provides an interpretable baseline for churn prediction.
- Estimates customer churn probabilities.
- Supports analysis of features associated with churn.

**K-Nearest Neighbors (KNN)**
- Predicts churn based on similarities between customer profiles.
- Provides a comparison with a distance-based classification approach.

Model development included hyperparameter tuning and 5-fold cross-validation.

### 3. Model Evaluation

Models were evaluated using classification metrics, including:

- ROC-AUC
- Precision
- Recall
- F1-score

Particular attention was given to churn recall because failing to identify customers who are likely to leave can limit the effectiveness of retention initiatives.

## Key Results

| Metric | Result |
|---|---|
| Customers analyzed | 7,043 |
| ROC-AUC | 0.841 |
| Churn recall | 78.3% |
| Churners captured in highest-risk 20% | 50.3% |
| Lift over random targeting | 2.51× |

### Customer Retention Analysis

To evaluate the potential business value of the model, customers were ranked according to their predicted churn risk.

The analysis found that:

- Targeting the **20% of customers with the highest predicted churn risk** would identify approximately **50.3% of actual churners**.
- This represents a **2.51× lift** compared with random customer selection.

These results demonstrate how predictive analytics could help a telecom company prioritize limited retention resources.

The analysis is a targeting simulation; it does not establish that contacting these customers would prevent churn.

## Tools & Technologies

- **Programming:** Python
- **Data Analysis:** Pandas, NumPy
- **Machine Learning:** scikit-learn
- **Visualization:** Matplotlib
- **Development:** Jupyter Notebook

## Repository Structure

```text
Telecom_Churn_prediction/
│
├── Churn-prediction/
│   ├── Telco-Customer-Churn.csv
│   └── Telecom_Churn_Prediction.ipynb
│
└── README.md
```

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/kapawa/Telecom_Churn_prediction.git
   ```

2. Navigate into the project:

   ```bash
   cd Telecom_Churn_prediction
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Open the notebook:

   ```text
   Churn-prediction/Telecom_Churn_Prediction.ipynb
   ```

5. Run the notebook cells in order.

Ensure that the dataset path in the notebook points to the included `Telco-Customer-Churn.csv` file.

## Key Takeaways

This project demonstrates how machine learning can be applied to customer behavior analysis and retention planning.

It combines predictive modeling, model evaluation, and customer risk segmentation to translate classification results into actionable business insights.

## Future Improvements

- Compare additional algorithms, including Random Forest and XGBoost.
- Investigate probability calibration and different classification thresholds.
- Evaluate retention strategies using cost-sensitive analysis.
- Develop an interactive dashboard for customer churn monitoring.