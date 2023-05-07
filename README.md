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

In the first approach, a train_test_split function from scikit-learn machine learning library were used to split the data into 25% testing and 75% training sets. After that, LogisticRegression from the same library was used to model and fit the training set data. Then, the testing dta were implemented to the fitted logistic regression model to predict the "loan_status". At the end, the performance of the model was evaluated by calculating the accuracy score and the confusion matrix and printing the classification report.
Using the first approach this model was able to acheive an accuracy score of 0.95 which is an acceptable score. The reuslts of theconfusion matrix showed that 99% of the healthy loans and 90% of the high-risk loans were predicted correctly. 



In the second approach the counts of 1 and 0 were first reported. Results showed out of 77536 entries in this dataset, 75036 had a value of "0" int he "loan_status" column or 75036 entries are healthy loan. Ont he other hand, only 2500 loans are high risk and are marked by "1" in th e"loan_status" column. This clearly show an imbalances in this dataset. Therefore, I have used 



In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
