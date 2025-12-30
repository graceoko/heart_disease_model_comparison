# Comparative Machine Learning Models for Heart Disease Prediction

## Overview
This project explores the use of supervised machine learning to predict the presence of heart disease using a structured healthcare dataset. Rather than focusing solely on building a predictive model, the goal is to compare model performance and evaluate trade-offs that are especially relevant in healthcare analytics, such as balancing overall accuracy with sensitivity to disease detection.

Two classification models—Decision Tree and Naive Bayes—were developed and evaluated using cross-validation. Performance was assessed using accuracy, precision, and recall to illustrate how different algorithms may be better suited for different clinical or analytical priorities.

---

## Dataset
The analysis uses the publicly available **Heart Disease Dataset** from Kaggle, which contains clinical and demographic health indicators for 303 patients.

- **Observations:** 303  
- **Features:** 14 total variables  
- **Target Variable:**  
  - `1` = Presence of heart disease  
  - `0` = No heart disease  

Key features include age, sex, cholesterol levels, fasting blood sugar, ECG results, and other health indicators. The dataset contains no missing values and has a reasonably balanced distribution of outcomes.

---

## Problem Formulation
This project focuses on a binary classification task:

- **Objective:** Predict whether a patient has heart disease based on selected clinical features.

This framing allows for direct comparison of model behavior across evaluation metrics that matter in healthcare contexts, particularly recall (sensitivity) for identifying disease cases.

---

## Feature Selection & Preprocessing
To emphasize interpretability and model comparison, a subset of clinically relevant features was selected:

- `restecg` (resting ECG results)  
- `chol` (serum cholesterol)  
- `fbs` (fasting blood sugar)  

Numerical features were standardized using **StandardScaler**, and `target` was defined as the outcome variable. These choices allowed for a controlled comparison between models while reducing complexity.

---

## Models Evaluated
Two supervised learning models were implemented and evaluated using **5-fold cross-validation**:

- **Decision Tree Classifier**
- **Naive Bayes Classifier**

Model performance was assessed using:
- Accuracy
- Precision (per class)
- Recall (per class)

This multi-metric approach highlights how model performance can vary depending on the metric prioritized.

---

## Results & Key Insights
- The **Decision Tree** model outperformed Naive Bayes across most evaluation metrics:
  - Accuracy: **82.4%**
  - Balanced precision and recall across both classes
- The **Naive Bayes** model achieved lower overall accuracy (**53.2%**) but demonstrated higher recall for the positive class (presence of heart disease).

### Key Insight
Although the Decision Tree performed better overall, Naive Bayes was more sensitive to detecting disease cases. This illustrates an important healthcare analytics trade-off: a model with lower accuracy may still be valuable when minimizing false negatives is a priority.

---

## Why This Matters
In healthcare applications, model selection is rarely about maximizing a single metric. This project demonstrates how comparative evaluation and metric-driven reasoning are critical for aligning machine learning models with real-world clinical or operational goals.

---

## Limitations
- Limited feature set may not capture the full complexity of heart disease risk
- No hyperparameter tuning was performed
- Small dataset size limits generalizability
- Only two algorithms were explored

---

## Future Work
- Expand feature selection and incorporate additional clinical variables
- Apply hyperparameter optimization
- Evaluate additional classification models (e.g., Logistic Regression, SVM, ensemble methods)
- Explore cost-sensitive or recall-optimized approaches

---

## Artifacts
- **Notebook:** End-to-end data exploration, modeling, and evaluation
