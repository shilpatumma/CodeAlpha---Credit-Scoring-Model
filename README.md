# Credit Scoring Model using Machine Learning

## Overview

This project develops a Machine Learning-based Credit Scoring Model to predict an individual's creditworthiness using financial and behavioral attributes. The model classifies customers into three categories: Good, Standard, and Poor credit scores.

The project covers the complete machine learning workflow, including data preprocessing, feature engineering, model training, evaluation, and comparison of multiple classification algorithms.

---

## Problem Statement

Credit scoring plays a crucial role in the financial industry by helping institutions evaluate the risk associated with lending money to customers.

The objective of this project is to build a classification model that can accurately predict a customer's credit score category based on their financial history and credit behavior.

---

## Dataset

The dataset used in this project is publicly available on Kaggle.

**Dataset Source:**
https://www.kaggle.com/datasets/parisrohan/credit-score-classification

### Dataset Features

* Age
* Occupation
* Annual Income
* Monthly In-hand Salary
* Number of Bank Accounts
* Number of Credit Cards
* Interest Rate
* Number of Loans
* Delay from Due Date
* Number of Delayed Payments
* Outstanding Debt
* Credit Utilization Ratio
* Credit History Age
* Monthly Balance
* Payment Behaviour
* Credit Mix
* Payment of Minimum Amount

### Target Variable

Credit_Score

Classes:

* Good
* Standard
* Poor

### Note

The original dataset is not included in this repository due to GitHub file size limitations. Please download the dataset directly from Kaggle and place it in the project directory before running the notebook.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Google Colab
* Jupyter Notebook

---

## Project Workflow

### 1. Data Loading

* Imported the credit score classification dataset.
* Examined data structure and feature types.

### 2. Data Cleaning

* Removed unnecessary columns:

  * ID
  * Customer_ID
  * Name
  * SSN

* Converted numeric values stored as strings into proper numerical format.

* Handled missing values using median imputation.

### 3. Feature Engineering

#### Credit History Conversion

Converted credit history values from:

22 Years and 5 Months

to:

269 Months

#### Debt-to-Income Ratio

Created a new financial feature:

Debt-to-Income Ratio = Outstanding Debt / Annual Income

This feature helps capture the relationship between debt burden and income.

### 4. Data Encoding

Applied Label Encoding to convert categorical variables into numerical values suitable for machine learning algorithms.

### 5. Train-Test Split

* Training Set: 80%
* Testing Set: 20%
* Stratified Sampling applied to preserve class distribution.

### 6. Model Training

Trained and evaluated multiple classification models.

---

## Machine Learning Models

### Logistic Regression

A baseline classification algorithm used for performance comparison.

### Decision Tree Classifier

A tree-based model that learns decision rules from the training data.

### Random Forest Classifier

An ensemble learning technique that combines multiple decision trees to improve prediction accuracy and reduce overfitting.

Hyperparameters:

* n_estimators = 300
* max_depth = 20
* min_samples_leaf = 2
* min_samples_split = 5
* random_state = 42

---

## Evaluation Metrics

The following metrics were used to evaluate model performance:

* Accuracy Score
* Classification Report
* Confusion Matrix
* ROC-AUC Score

---

## Results

The performance of multiple machine learning models was compared:

| Model               | Purpose                   |
| ------------------- | ------------------------- |
| Logistic Regression | Baseline Model            |
| Decision Tree       | Tree-Based Classification |
| Random Forest       | Ensemble Learning Model   |

Among the tested models, Random Forest achieved the best overall performance and was selected as the final model.

---

## Project Structure

```text
credit-scoring-model/
│
├── Credit_Scoring_Model.ipynb
├── README.md
└── requirements.txt
```

---

## Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

---

## Future Enhancements

* Hyperparameter Tuning using GridSearchCV
* Feature Selection Techniques
* Model Deployment using Flask or Django
* Interactive Dashboard using Streamlit
* Explainable AI using SHAP and LIME
* Real-time Credit Risk Prediction System

---

## Key Learning Outcomes

* Data Cleaning and Preprocessing
* Feature Engineering
* Classification Algorithms
* Model Evaluation Techniques
* Machine Learning Workflow
* Credit Risk Analysis

---

## Author

**Shilpa Tumma**

