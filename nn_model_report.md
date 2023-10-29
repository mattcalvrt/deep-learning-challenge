# Credit Risk Classification Report

## Overview of the Analysis

* The purpose of this analysis is to use various techniques to train and evaluate a model based on loan risk. This was done using a CSV dataset of historical lending activity from a peer-to-peer lending services company. 
* The financial data includes information about the loan (size, interest rate), information about the borrower (income, debt to income ratio, number of accounts, derogatory marks, total debt), and loan status (healthy = "0"; high risk of default = "1"). The goal of our analysis is to use this data to build a model that can predict loan risk.
* Loan status serves as our target variable for the model. The remaining columns in the dataset serve as the features. The dataset consisted of 77,536 loans of which 75,036 were classified as healty and 2,500 were at high risk of default.
* To train and evaluate the model we:
    1. Split the data into training and testing sets;
    2. Created a logistic regression model with the original data
    3. Predicted a logistic regression model using resampled data (ie. oversampled the high risk loans)
* To evaulate the model we:
    1. Calculated the accuracy score of the model,
    2. Generated a Confusion Matrix,
    3. Printed the Classification Report

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1 - Logistic regression model using the original data:
  * Balanced Accuracy: .9520
  * Precision: 
      * Healthy Loans: 1.0
      * High Risk Loans: 0.85
  * Recall: 
      * Healthy Loans: 0.99
      * High Risk Loans: 0.91

* Machine Learning Model 2: Logistic regression model using the resampled data
  * Balanced Accuracy: .9937
  * Precision: 
      * Healthy Loans: 1.0
      * High Risk Loans: 0.84
  * Recall: 
      * Healthy Loans: 0.99
      * High Risk Loans: 0.99

## Summary

The model with the resampled data seems to perform best for our purposes. The original dataframe has imbalanced classes (75,036 Healthy Loans vs 2,500 High Risk Loans, so model 1 performs well at predicting healthy loans (majority class); however, it doesn't perform well at predicting high-risk loans. Since we are interested in predicting high risk loans, we resampled the data by oversampling the high risk loans (minority class) in model 2. The logistic regression model using resampled data is less precise, but is better at predicting high risk loans (recall). For risk reduction, identifying as many high risk loans as possible is preferred, even if it results in an increase of false positives. 


