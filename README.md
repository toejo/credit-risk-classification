# credit-risk-classification
 
## Overview of the Analysis

This report analyses the effectiveness of two Logistic Regression models in regards to predicting creditworthiness of loan recipients/borrowers. The dataset is a record of historical lending activity from a peer-to-peer lending services company; it includes data such as size of the loan (loan_size), income of the loan recipient (borrower_income), total debt (total_debt), and status of the loan (loan_status).

Creditworthiness is based off of whether a loan recipient is given a loan_status of "1" or "0", where "1" equates to a loan that at a high-risk of defaulting and 0 being healthy loan. Steps taken to achieve the results include: (1) processing the dataset by splitting dividing it into the target variable (loan_status) and the feature variables (the rest of the variables in the dataset in this case), (2) performing a train_test_split on the variables to train the models, (3) running the dataset through the logistic regression model (Logistic Regression Model A), and (4) resampling the dataset using the RandomOverSampler module then running the resampled dataset through logistic regression a second time (Logistic Regression Model B).   

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression Model A:
  * Model A achieved a 95% Balanced Accuracy Score.
  * Model A achieved a 100% Precision score when predicting healthy loans (0), and an 87% Precision score when predicting loans with a high-risk of defaulting (1).
  * Model A achieved a 100% Recall score when identifying healthy loans (0), and a 91% Recall score when identifying loans with a high-risk of defaulting (1).
    
* Logistic Regression Model B:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * Model B achieved a 100% (99.6% if not rounded up) Balanced Accuracy Score.
  * Model B achieved a 100% Precision score for predicting healthy loans (0), and an 87% Precision score when predicting loans with a high-risk of defaulting (1).
  * Model B achieved a 99% Recall score when identifying healthy loans (0), and a 100% Recall score when identifying loans with a high-risk of defaulting (1).

## Summary

The two models achieved comparable results. Both models did well in predicting (Precision score) whether a loan is healthy in status (0) or if a loan is at high risk for defaulting (1). However, Model B did slightly better than Model A in regards to identifying (Recall score) the status of a loan, and its Balanced Accuracy Score is higher as well. Therefore, Model B performed the best.

The difference between Model A and B is that Model B's dataset was rebalanced/resampled through RandomOverSampler which led to an even distribution between data points (resulting to an increase in the sample size of class 1/target variable = 1, from 750 value_counts() in Model A to 52525 value_counts() in Model B). This suggests that having more data points with a loan_status that equals to 1, or at least having a comparable distribution of loan_status data points,  had a positive effect in training the Logistic Regression Model. Therefore, for this particular dataset, predicting `1`'s seem to be more important. 
