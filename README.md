# credit-risk-classification

## Overview of the Analysis

A datset of historical lending activity from peer to peer lending services company was provided to build a model that can identify the creditworthiness of borrowers. This dataset has 77536 rows of data. These data include:

1:loan_size
2:interest_rate
3:borrower_income
4:debt_to_income
5:num_of_accounts
6:derogatory_marks
7:total_debt
8:loan_status

Here to define the creditworthiness of borrowers a value of 0 and 1 was assigned to the "loan_status" column which means that the loan is healthy, or has a high risk of defaulting respectivley. Two approches were used to build a model that predicts "loan_status":
1: Split the data to training and testing sets and use logistic regression to model "loan_status"
2: Check for data imbalances in the "loan_status" column, remove the imbalances by resampling, split the data to training and testing sets, and use logistic regression to model "loan_status"

In the first approach, a train_test_split function from scikit-learn machine learning library were used to split the data into 25% testing and 75% training sets. After that, LogisticRegression from the same library was used to create the model and fit the training set data. Then, the testing data were implemented to the fitted logistic regression model to predict the "loan_status". At the end, the performance of the model was evaluated by calculating the accuracy score and the confusion matrix and printing the classification report.
Using the first approach this model was able to acheive an accuracy score of 0.95 which is an acceptable score. The reuslts of the confusion matrix showed that 99% of the healthy loans and 90% of the high-risk loans were predicted correctly. Below is a summary of the classification report.



Healthy loans had the precision of almost 1 meaning that the counts of high-risk loans which unaccurately were modeled as healthy loans were very low. However, high-risk loans had the precision of only 0.85 meaning that the counts of healty loans which inaccurately were modeled as high-risk loans were not insignificant. 

Healthy loans had the the recall of 0.99 meaning that the logistic regression model was able to find 99% of the healthy loans. The recall score of the high-risk loans were 0.91 meaning that the logistic regression model was able to to find 91% of the high-risk loans.
Ideally, in the finance industry one would like to find a better recall score for the high-risk loans to reduce the risk of giving loans to cutomers that are high risk. Therefore, a second approach was implemented to reduce the risk. 


In the second approach the counts of 1 and 0 were first reported. Results showed out of 77536 entries in this dataset, 75036 had a value of "0" in the "loan_status" column or are healthy loan. On the other hand, only 2500 loans were high risk and were marked by "1" in the "loan_status" column. This clearly shows an imbalances in this dataset. Therefore, first RandomOverSampler function from imbalanced-learn library was used to properly splitting the data into trainign and testing sets and then similar to the first approach a train_test_split function and LogisticRegression was used to creat the model, fit and predict the test results. At the end, the performance of the model was evaluated by calculating the accuracy score and the confusion matrix and printing the classification report.
Using the second approach, this model was able to acheive an accuracy score of 0.99 which is very good accuracy score and a better score than the first approach. The reuslts of the confusion matrix showed that 99% of the healthy loans and 99% of the high-risk loans were predicted correctly. Below is a summary of the classification report.


Healthy loans had the precision of almost 1 meaning that the counts of high-risk loans which unaccurately were modeled as healthy loans were very low. However, high-risk loans had the precision of only 0.84 meaning that the counts of healty loans which inaccurately were modeled as high-risk loans were not insignificant. 

Healthy and high-risk loans had the the recall of 0.99 meaning that the logistic regression model was able to find 99% of the healthy loans and high-risk loans. 
Ideally, in  the  finance industry one would like to find a good recall score for the high-risk loans to reduce the risk of giving loans to cutomers that are high risk. Therefore, a second approach was a better approach and the results of this moel should be used for futre analysis. 


