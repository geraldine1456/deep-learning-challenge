# Credit Risk Analysis Report

## Overview of the Analysis

In this analysis, we aimed to evaluate the creditworthiness of borrowers using a logistic regression classifier. The dataset used (`lending_data.csv`) contains historical lending activity, including borrower features such as income, debt, and loan amount, along with the `loan_status` target column indicating whether a loan was healthy (0) or high-risk (1).

We sought to predict the `loan_status` variable to assist a peer-to-peer lending company in assessing risk. The machine learning process included:

- Data preprocessing and splitting into features (`X`) and labels (`y`)
- Train-test split using `train_test_split` with `stratify`
- Model training with `LogisticRegression`
- Evaluation using a confusion matrix and classification report

## Results

* **Machine Learning Model 1: Logistic Regression**
    * **Accuracy Score:** 0.99
    * **Precision Score (Healthy Loans - 0):** 1.00
    * **Recall Score (Healthy Loans - 0):** 1.00
    * **F1 Score (Healthy Loans - 0):** 1.00
    * **Precision Score (High-Risk Loans - 1):** 0.87
    * **Recall Score (High-Risk Loans - 1):** 0.95
    * **F1 Score (High-Risk Loans - 1):** 0.91

## Summary

The logistic regression model demonstrates excellent overall performance, especially for predicting healthy loans (0) with perfect precision, recall, and F1-score. It also effectively detects high-risk loans (1), with a strong recall of 0.95 and an F1-score of 0.91.

This indicates that the model is reliable for identifying risky borrowers — which is often the more critical task for lenders. As a result, we **recommend this model for use**. For further improvement, especially in reducing false positives, advanced classifiers or data resampling techniques may be considered.