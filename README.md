# credit-risk-classification
Data Analytics Bootcamp: Module 20 Challenge

## Project Description
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Instructions
* Split the Data into Training and Testing Sets
* Create a Logistic Regression Model with the Original Data
* Write a Credit Risk Analysis Report (below)

## References
Code was created referencing class activities. The following source was refernced for randomoversampler as it was not covered in class activities: https://snyk.io/advisor/python/imblearn/functions/imblearn.over_sampling.RandomOverSampler

# Credit Risk Analysis Report

## Overview of the Analysis

The purpose of this analysis is to identify the creditworthiness of loan borrowers. The report analyzes historical lending activity from a peer-to-peer lending services company. The dataset includes loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total date and loan status. The variable being predicted is loan status, 0 being a healthy loan and 1 being a high-risk loan.  The data was first seperated into labels and features. After checking the balance of the lables, the original dataset included 75,036 healthy loans and 2,500 high-risk loans. The data was then split into training and testing datasets by using `train_test_split`. Next, a logistic regression model was created on the original data. A prediction was made using the testing data, an accuracy score was calculated, then a confusion matrix was generated and a classification report was printed. The data was then resampled using `RandomOverSampler`. The `LogisticRegression` classifier was used on the resampled data to fit the model and make predictions. 

## Results

* Machine Learning Model 1:
  * Accuracy: 94% balanced accuracy score 
  * Precision: 100% precise in predicting healthy loans; 87% precise in predicting high-risk loans
  * Recall scores: 100% recall for healthy loans; 89% recall for high-risk loans
* Machine Learning Model 2:
  * Accuracy: 99.6% balanced accuracy score 
  * Precision: 100% precise in predicting healthy loans; 87% precise in predicting high-risk loans
  * Recall scores: 100% recall for healthy loans; 100% recall for high-risk loans

## Summary

* Model 2 seems to perform slightly better than model 1, with 99% accuracy vs 94% accuracy. However, both are 87% prescise in predicting high-risk loans making neither model ideal for the purpose needed. It would be best to have a model that can more accurately predict high-risk loans so that the financial institution's lending is safe-guarded against potential defaults. 