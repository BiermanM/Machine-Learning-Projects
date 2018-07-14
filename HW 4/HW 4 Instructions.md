# HW 4 Instructions

1.	Set up the Auto data 
    1.	Load the ISLR package
    2.	Determine the median value for mpg
    3.	Use the median to create a new column in the data set named mpglevel, which is 1 if mpg > median and otherwise is 0. Make sure this variable is a factor. We will use mpglevel as the target (response) variable for the algorithms. 
    4.	Use the `names()` function to verify that your new column is in Auto

2.	Plots 
    1.	 Set up a 2x2 graph grid and plot the following pairs of plots 
    2.	Plot pair 1: plot `horsepower~mpg` and `weight~mpg`, setting colors according to the factor mpglevel, ex: `col = (Auto$mpglevel)`
    3.	Plot pair 2:  plot `horsepower~mpglevel` and `weight~mpglevel`

3.	Create a train and a test set 
    1.	75% train, 25% test
    2.	Set seed to `1234` to get reproducible results
    3.	Do not include columns `name` and `mpg` in the train and test sets

4.	Build a logistic regression model 
    1.	Build the model on the train set with mpglevel as the response and all other columns as predictors
    2.	Use the `predict()` function on the test set
    3.	Create a table comparing predicted to actual values for mpglevel
    4.	Calculate the mean accuracy

5.	Cluster with kNN (not scaled) 
    1.	Apply the kNN algorithm on the train set using default `k = 1`
    2.	Create a table comparing predicted to actual values for mpglevel

6.	Cluster with kNN (scaled) 
    1.	Create a new scaled train and scaled test set; you can’t scale mpglevel so leave that out of the scaled train and test sets
    2.	Create a vector called `scale_train_labels` for mpglevel
    3.	Create a vector called `scale_test_labels` for mpglevel
    4.	Apply the kNN algorithm on the scaled data again with `k = 1`
    5.	Create a table comparing predicted to actual values for mpglevel

7.	Questions (Place in white portion at the end of the Rmd file) 
    1.	In the plots created in Step 2, describe the relationship you see between mpg and horsepower, and the relationship you see between mpg and weight.
    2.	In the plots created in Step 2, why did we get data points for the first pair of graphs and box plots for the second pair?
    3.	In step 3 when we created the train and test sets, why do we need to remove column `name`?
    4.	In step 3 when we created the train and test sets, why do we need to remove column `mpg`?
    5.	Compare the mean accuracies of the three algorithms.
    6.	Compare and contrast how a logistic regression model makes predictions versus kNN with `k = 1`.
