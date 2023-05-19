# Module 12 Credit Risk Classification Report

## Overview of the Analysis

The purpose of this analysis was to develop machine learning models to predict credit risk based on financial information. The dataset provided contained various features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status. The goal was to predict whether a loan is classified as a healthy loan (0) or a high-risk loan (1).

The loan status variable showed an imbalanced distribution with 75,036 instances of healthy loans (0) and 2,500 instances of high-risk loans (1).

The analysis followed the stages of the machine learning process, including data preparation, model development, and evaluation. Two machine learning models were utilized: Logistic Regression with the original data and Logistic Regression with resampled training data.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression with Original Data
  * Balanced Accuracy Score: 0.9443
  * Confusion Matrix: [18679  80, 67 558]
  * Classification Report: 

      |       | Precision | Recall | F1-Score | Support |
      |-------|-----------|--------|----------|---------|
      | 0     | 1.00      | 1.00   | 1.00     | 18759   |
      | 1     | 0.87      | 0.89   | 0.88     | 625     |
      |       |           |        |          |         |
      | Accuracy  |           |        | 0.99     | 0.99    |
      | Macro Avg | 0.94      | 0.94   | 0.94     | 19384   |
      | Weighted Avg | 0.99   | 0.99   | 0.99     | 19384   |




* Machine Learning Model 2:
  * Balanced Accuracy Score: 0.9960
  * Confusion Matrix: [18668  91, 2 623]
  * Classification Report: 

      |       | Precision | Recall | F1-Score | Support |
      |-------|-----------|--------|----------|---------|
      | 0     | 1.00      | 1.00   | 1.00     | 18759   |
      | 1     | 0.87      | 1.00   | 0.93     | 625     |
      |       |           |        |          |         |
      | Accuracy  |           |        | 1.00     | 19384   |
      | Macro Avg | 0.94      | 1.00   | 0.96     | 19384   |
      | Weighted Avg | 1.00   | 1.00   | 1.00     | 19384   |

## Summary

Based on the evaluation of the machine learning models, both models showed strong performance in predicting credit risk. However, the model trained with resampled data outperformed the model using the original data.

The Logistic Regression model trained with resampled data achieved balanced accuracy score of 0.9960, indicating its high accuracy in predicting both healthy loans (0) and high-risk loans (1). It showed higher precision, recall, and F1-score for both classes.

Although the model trained with the original data also performed well, the resampled data model demonstrated superior performance, particularly in terms of recall for high-risk loans. By addressing the class imbalance issue through resampling, the model was able to better capture instances of the minority class.

Given the higher accuracy in identifying high-risk loans, I recommend utiling the Logistic Regression model trained with resampled data for credit risk prediction.
