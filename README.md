# Supervised_learning_logistic_regression_model

## Overview of the Analysis

This is an application which trains a model using supervised machine learning to classify/predict the creditworthyness of borrowers

The dataset includes financial information such as loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt and analyzes these metrics to classify/predict a borrower's loan_status (A value of 0 means the loan is healthy, while a value of 1 means the loan has a high risk of defaulting)

The total set of data includes 77,536 loans, which were previously classified into 75,036 healthy loans and 2,500 high risk loans.  We use this loan data to train a model to be able to classify additional data which we may get in the future which doesn't have loan classifications already in order to make a prediction as to the classification of future borrowers using the same metrics.

We use a logistic regression model to model the classifications and compare that to a logisitic regression model with a random oversampling tecnnique to determine the best predictor of creditworthyness for our use case.

The use of a random oversampling methodology is an attempt at addressing the imbalance in the sampling data as there are a lot more healthy loans than there are high-risk loans.


## Results



* Logisitic Regression Learning Model:
  * Accuracy = 95.2%
  * Precision = 0 -> 100%   1 -> 85%
  * Recall =    0 -> 99%    1 -> 91%



* Logisitic Regression Learning Model with RandomOversampling:
  * Accuracy =  99.3%
  * Precision = 0 -> 100%   1 -> 84%
  * Recall =    0 -> 99%    1 -> 99%

## Summary

The logisitic regression model with oversampling did a better job in predicting as it has a 99.3% balanced accuracy score as compared to 95.2% without oversampling.  This makes sense as the Logistic Regression Learning Model had a lot more healthy loan data in its' training set.

When we added in RandomOversampling, it taught the model to put more weight into the high-risk loans and so it would do a better job at identifying the high risk loans.  This can be seen by observing that the recall in high-risk loans increased from 91% to 99% which means the model did a better job at identifying true positives, and had less false negatives when it came to predicting high-risk loans.

For this analysis, it was more important that the model would be able to accurately predict/classify high risk loans.  To that end, the Logistic Regression model w/ oversampling did a better job overall as we can see an 8 point jump in the recall, at the cost of 1 point in the precision.  overall accuracy incraesed to 99.3% as well.