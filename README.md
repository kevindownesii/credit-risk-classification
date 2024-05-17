# credit-risk-classification

* Data Analysis Steps

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
Split the data into training and testing datasets by using train_test_split.

Fit a logistic regression model by using the training data (X_train and y_train).

Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

Generate a confusion matrix.

Print the classification report.

* CREDIT RISK ANALYSIS REPORT

## Overview of the Analysis

* The purpose of this analysis is to use various techniques to train and evaluate a model based on loan risk. Using a dataset of historical lending activity from a peer-to-peer leanding service company, a model was built to determine the creditworthiness of borrowers categorizing them into healthy or high risk. 

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

Overall, the logistic regression model is very effective with predicting healthy loans and reasonably effective in identifying high-risk loans.

