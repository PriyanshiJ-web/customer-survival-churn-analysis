# Customer Survival Analysis & Churn Prediction

An applied machine-learning project exploring **customer retention, survival analysis, churn prediction, and model explainability** using telecommunications customer data.

## Project Overview

Customer churn is the loss of customers over time and is an important business problem for subscription-based companies. This project combines **survival analysis** and **classification modelling** to understand customer retention patterns and identify customers at higher risk of churn.

The analysis covers:

* Exploratory data analysis of customer characteristics and services
* **Kaplan–Meier survival analysis** to study customer retention over time
* **Log-rank tests** to compare survival across customer segments
* **Cox Proportional Hazards regression** to identify factors associated with churn risk
* Customer-level survival and hazard curves
* Customer lifetime value estimation
* **Random Forest** classification for churn prediction
* Hyperparameter tuning and class-imbalance handling
* Model evaluation using **F1 score and ROC-AUC**
* Model interpretation using **Permutation Importance, Partial Dependence and SHAP**

## Key Findings

The analysis indicates that customer retention varies substantially with factors such as:

* Customer tenure
* Contract type
* Internet service
* Payment method
* Monthly charges
* Adoption of additional services

The survival analysis provides a time-based view of customer retention, while the classification model provides a customer-level estimate of churn risk.

## Modelling

### Survival Analysis

The project uses:

**Kaplan–Meier Estimator**
Estimates the probability that a customer remains active beyond a given tenure.

**Log-Rank Test**
Compares survival distributions across customer segments.

**Cox Proportional Hazards Model**
Models the relationship between customer characteristics and churn hazard.

### Churn Prediction

A **Random Forest classifier** is used to predict whether a customer is likely to churn.

The modelling workflow includes:

1. Data preprocessing and feature preparation
2. Train-validation split
3. Class-imbalance handling
4. Hyperparameter tuning using cross-validation
5. Model evaluation using F1 and ROC-AUC
6. Feature-importance and explainability analysis

The referenced implementation reports approximately **0.62 F1** and **0.85 ROC-AUC** on its evaluation setup; these metrics should be independently reproduced and validated before being treated as final results.

## Explainability

The project explores multiple techniques for interpreting model predictions:

* **Permutation Importance** — measures the effect of disrupting individual features.
* **Partial Dependence Plots** — examine how predictions change with selected features.
* **SHAP** — provides feature-level explanations for individual predictions and overall model behaviour.

## Application

The original implementation also includes a Flask-based interface that combines churn prediction with survival analysis and model explanations.

The application structure is retained as part of the project implementation and is intended to be further developed and independently validated.

## Repository Structure

```text
.
├── Images/
├── static/
│   └── images/
├── templates/
├── Exploratory Data Analysis.ipynb
├── Customer Survival Analysis.ipynb
├── Churn Prediction Model.ipynb
├── app.py
├── requirements.txt
├── Procfile
├── LICENSE.md
└── README.md
```

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Lifelines
* SHAP
* Flask
* Jupyter Notebook

## Reference

This repository is an **adaptation/learning implementation based on an existing open-source project** and retains the original project's MIT licensing terms.

Original project:
`archd3sai/Customer-Survival-Analysis-and-Churn-Prediction`

The implementation will be independently studied, validated, and extended as part of the learning process.
