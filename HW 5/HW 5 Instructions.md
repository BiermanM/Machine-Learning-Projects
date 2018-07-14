# HW 5 Instructions

1.	Set up the Auto data again, and train and test sets, using your code from Steps 1 and 2 of Homework 4 to create an Auto$mpglevel column, then divide into train and test sets (75/25).

2.	Build a Naïve Bayes model 
    1.	Build the model on the train set
    2.	Use the `predict()` function on the test set
    3.	Create a table comparing predicted to actual values for mpglevel
    4.	Calculate the mean accuracy

3.	SVM linear kernel 
    1.	Use the `tune()` function to perform cross-validation to determine the best value for cost
    2.	Use the parameter(s) from the previous step to build an SVM model with a linear kernel on the train set
    3.	Use the `predict()` function on the test set
    4.	Create a table comparing predicted to actual values for mpglevel
    5.	Calculate the mean accuracy

4.	SVM polynomial kernel 
    1.	Use the `tune()` function to perform cross-validation to determine the best values for cost and degree
    2.	Use the parameter(s) from the previous step to build an SVM model with a polynomial kernel on the train set
    3.	Use the `predict()` function on the test set
    4.	Create a table comparing predicted to actual values for mpglevel
    5.	Calculate the mean accuracy

5.	SVM radial kernel 
    1.	Use the `tune()` function to perform cross-validation to determine the best values for cost and gamma
    2.	Use the parameter(s) from the previous step to build an SVM model with a radial kernel on the train set
    3.	Use the `predict()` function on the test set
    4.	Create a table comparing predicted to actual values for mpglevel
    5.	Calculate the mean accuracy

6.	Questions. 
    1.	Compare the accuracy results for the 4 models
    2.	Discuss the advantages and disadvantages of Naïve Bayes versus SVM
