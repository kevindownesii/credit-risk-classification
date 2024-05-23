# credit-risk-classification

## Data Analysis Steps

For Challenge 20, I was provided a dataset of hisotorical lendgin activity from a peer-to-peer lending service comapany. I was tasked to build a model to train and evalutae based on loan risk the creditworthiness of borroweres. 

Utilizing Pandas, the lending_data.csv file from the Resources folder was converted into a dataframe. 

The labels set (y) from the value “loan_status” which was a binary value of 0 meaning the loan is healthy or 1 meaning the loan has a high risk of defualting. The features (X) DataFrame was created from the remaining columns of loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt, and loan_status. This was accomplished by dropping the loan_status from the dataframe. 

Utilizing the sklearn library by importing train_test_split, the data was split into X_train, X_test, y_train, and y_test. 

Importing LogisticRegression from sklearn, the training data (X_train and y_train) was used to fit a logistic regression model.

The predictions were saved for the testing data labels by using the testing feature data (X_test) and the fitted model.

A confusion matrix, accraucy score, and classification report were created. 

## Confusion Matrix

|              |Predicted0|Predicted1|
|--------------|----------|----------|
| Actual 0     | 18673    | 86       |
| Actual 1     | 23       | 593      |

## Accuracy Score
Accuracy Score : 0.993912505158894

## Classification Report 

|              | precision |  recall  | f1-score | support  |
|--------------|-----------|----------|----------|----------|
|  0 (healthy) | 1.00      | 1.00     |  1.00    | 18759    |
|  1 (highrisk)| 0.87      | 0.95     |  0.91    | 625      |
|--------------|-----------|----------|----------|----------|
|  accuracy    |           |          | 0.99     |  19384   | 
|  marco avg   |  0.94     | 0.97     | 0.95     |  19384   | 
|  weighted avg|  0.99     | 0.99     | 0.99     |  19384   |


### CREDIT RISK ANALYSIS REPORT

## Overview of the Analysis

* The purpose of this analysis is to use various techniques to train and evaluate a model based on loan risk. Using a dataset of historical lending activity from a peer-to-peer leanding service company, a logistic regression model utilzing sklearn was built to determine the creditworthiness of borrowers categorizing them into healthy or high risk. 

* The financial information was historical information on previous borrowers. Data included loan size, borrower income, debt to income ratio, interst rate, numeber of accounts, total debt, and derogatory marks. With this data, the model I built could predict if a potential borrower had a high risk of defaulting on the loan. 

* The variable I was trying to predict was loan status. The values in the loan_status column were as follows:
    *   0 - loan was in good standing
    *   1 - loan was in default


* The stages of machine learning including the following:
    *   Splitting the dataset into two unique variables X and y. Y was the target value which was the loan_status column vuale of 0 or 1. X was the features which was all the other columns. 
    *   After obtaining the variables, the dataset was split into a training group and a test group. 


* The machine learnng model used was Logistic Regression. Logistic Regression is a statistical model used in supervised learning. It is used for binary classification tasks where it can predict the probability that for a given input the value belongs to a specific class. The ouput has two potential outcome represented by 0 or 1. 

## Results

* Machine Learning Model Results:
    * For the Healthy Loans (0), the precision is 1.00, indicating that all the predictions for this label were correct. The recall is 1.00, meaning that all instances of this label were correctly identified.
        The precision for High-Risk Loan (1) is 0.87, indicating that 87% of the predictions for this label were accurate. The recall is 0.89, indicating that 89% of the instances of this label were correctly identified.The overall accuracy of the model is 0.99, indicating that it correctly predicted the loan risk for 99% of the instances.


## Summary

The logistic regression model performs well in predicting the `0` healthy loans with 100% on precision and recall. The model is correctly identifying all healthy loans and does not misclassify any healthy loans as high-risk.

For `1` high-risk loans, the logistic regression model also performs well; however, not as well as the healthy loans. The precision score is 87% which means that only 87% of the loans predicted as high-risk actually turn out to be high-risk. The recall score is 95% informing us tha the model captures 95% of the actual high-risk loans.

Overall, the logistic regression model is very effective with predicting healthy loans and reasonably effective in identifying high-risk loans. However, based on the data set, I would not recommend this model to identify borrowers who are high risk. Out of the 19,384 records only 625 were deemed high risk which comes out to 3.22%. The sample size isn't large enough to get a could determination of creditworthiness for borrowers who are deemed high risk. I would need a larger sample size since the financial industry is highly regulated and has had many lawsuit over discriminatory lending standards. In order to move forwad, I would need a high percentage than 87% in predicting loans to be high risk. 

