# credit-risk-classification
UC Davis Module 20 Challenge

Machine learning methods are used to analyze a dataset consisting of past lending transactions of a peer-to-peer lending firm. The aim is to construct a model capable of assessing the creditworthiness of potential borrowers. 

## Overview of the Analysis

The analysis aims to develop and assess the efficacy of a data model that forecasts the creditworthiness of prospective borrowers in peer-to-peer lending platforms. 

The financial data included: 
  - size of loan
  - interest rate
  - borrower's income
  - debt to income ratio
  - number of accounts borrower held
  - derogatory marks against the borrower
  - total debt
  - loan status

The dataset comprised 77,536 data points and was divided into training and testing sets. The training set was utilized to construct an initial logistic regression model from scikit-learn. The primary objective was to predict whether loans to borrowers in the testing dataset would be categorized as either low or high-risk. 

Initially, the model was drawn from the dataset containing the low- and high-risk datapoints and to address the imbalanced nature of the data, the training dataset was resampled. The RandomOverSampler module was utilized for this purpose. The resampling process generated a total of 56,721 datapoints for both low and high-risk loans to balance the data. 

A revised logistic regression model used the newly balanced training data and was used to predict whether loans given to borrowers in the testing set would be considered low- or high-risk. 

## Results

* Machine Learning Model 1:
  - Precision: average of 92.5% (the model was 100% precise in predicting low-risk loans and was only 85% precise in predicting high-risk loans)
  - Accuracy: 99%
  - Recall: average of 95% (the model was 99% precise in predicting low-risk loans and was only 91% precise in predicting high-risk loans)

* Machine Learning Model 2:
  - Precision: average of 92% (the model was 100% precise in predicting low-risk loans and was only 84% precise in predicting high-risk loans)
  - Accuracy: 99%
  - Recall: average of 99% (the model was 99% precise in predicting low-risk loans and was only 91% precise in predicting high-risk loans)

## Summary

At times, the system may identify a loan as bad when it is actually a good loan. In a balanced dataset, the recall for bad loans performs better than in an imbalanced scenario. This indicates the model successfully captures 99% of the bad loans in the test data. However, with an 84% precision, it means that around 84% of the loans flagged as bad are accurate, while the remaining could be good loans. Therefore, it would be advantageous to involve human assessment to verify the categorization of loans marked as bad, ensuring their accurate classification.

