# HW 6 Instructions

## Problem 1: Default data

1.	Set up the data
    1.	Load the ISLR library and attach the Default data set.
    2.	Run the `dim()` and `names()` functions on Default
    3.	Use function `set.seed(2017)` so your results are reproducible.
    4.	Divide the data into 80% for training and the rest for a test set.

2.	Logistic regression model
    1.	Create a logistic regression model on the training data where default is predicted by all other variables
    2.	Run a summary of the model
    3.	Predict Yes/No on the test data
    4.	Compute the accuracy

3.	Decision tree model
    1.	Create a decision tree model on the training data
    2.	Run a summary of the model
    3.	Make predictions for the test set
    4.	Compute the accuracy

4.	Display the tree
    1.	Print the tree with labels
    2.	Display the tree in nested decision form by just using the tree name 

## Problem 2: Heart data

1.	Set up the data
    1.	Download the heart data to your machine from Piazza.
    2.	Load the data into R and attach it
    3.	Remove the `X` column
    4.	Set up train and test sets with 80% for training again using seed `2017`

2.	Logistic regression model
    1.	Create a logistic regression model on the training data where AHD is predicted by all other variables
    2.	Run a summary of the model
    3.	Predict Yes/No on the test data
    4.	Compute the accuracy

3.	Decision Tree Model
    1.	Create a decision tree model on the training data
    2.	Run a summary of the model
    3.	Make predictions for the test set
    4.	Compute the accuracy

4.	Display the tree
    1.	Print the tree with labels
    2.	Display the tree in nested decision form by just using the tree name 

5.	Cross validation
    1.	Create a new tree from the `cv.tree()` function
    2.	Look at the `$dev` and `$size` variables by displaying the tree using its name
    3.	Plot in a 1x2 format:
        1.	`$size` and `$dev`
        2.	`$k` and `$dev`

6.	Prune the tree
    1.	Create a new pruned tree using `best = n` where `n` is the optimal size indicated in step 5
    2.	Plot the new pruned tree with labels

7.	Predict
    1.	Using the pruned tree, make predictions on the test set
    2.	Compute the accuracy

## Questions

### Problem 1

1. In the logistic regression model, which variables were important and which were not?

2. What was the accuracy of the logistic regression model and the decision tree model?

3. In the tree, why might you have a branch where both branches are No?

4. Write a simple if/else statement that summarizes the Yes/No values in the decision tree.

5. Is it a good idea to prune this tree? Why or why not?

### Problem 2

1. Which variables were important (2 or 3 **) in the logistic regression model?

2. Which variables were used to create the decision tree?

3. Compare the accuracy of the logistic regression model and the decision tree.

4. What was the accuracy on the pruned tree?

5. Which model (logistic regression, decision tree) might be more meaningful to a doctor, and why.
