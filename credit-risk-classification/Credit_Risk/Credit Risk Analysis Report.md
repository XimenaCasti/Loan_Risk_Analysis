Credit Risk Analysis Report

## Overview of the Analysis

The goal of this analysis is to evaluate a Machine Learning Module to determine loan risk. I will be using historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

The data used to perform the module, includes the following columns: "loan_size", "interest_rate","borrower_income", "debt_to_income, 	"num_of_accounts", "derogatory_marks", "total_debt" and "loan_status".

I will be predicting if both the 0 (healthy loan) and 1 (high-risk loan).

Stages of the machine learning process: 
1. Split the Data into Training and Testing Sets
2. Create a Logistic Regression Model
    a. Generate a confusion matrix.
    b. Generate a classification report


## Results and Summary 

Confusion Matrix: 
0 = [[18679    80]
1 = [   67   558]]

Explanation of Confusion Matrix: 

True Negative = 18679 instances were correctly predicted as class 0. 
False Positive =  80 instances were wrongly predicted as class 1. 
False Negative = 67 instances were wrongly predicted as class 0. 
True Positive = 558 instances were correctly predicted as class 1.  

Classification report:

precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.89      0.88       625

    accuracy                           0.99     19384
   macro avg       0.94      0.94      0.94     19384
weighted avg       0.99      0.99      0.99     19384



The logistics regression model predicts healthy loan with 100% precision while the high risk loan is predicted with a 87% precision. 
Meaning that when the model predics 1, it is correct 87% of the time. 
Recall: For 0, it indicates a 100% recall, while for 1 the model identifies 89% of the actual instances. 
The Accuracy of the model is 99%.


## Summary

The logistics regression module performs very well identifying high risk loan and low risks loan. However, it would be ideal to run the module with more training data for the class 1 so that we could have a stronger recall for it. The module performs very well on the class 0 which could be associated with the larger data that the module used to predict. 

