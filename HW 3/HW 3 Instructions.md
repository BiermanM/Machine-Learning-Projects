# HW 3 Instructions

1.	Start with a new Rstudio Rmd file, add headings for Homework 3, your name and a brief description of the purpose of the script. Clearly label each step. Each step should have one or more R code chunks. For step 1, load library mlbench, installing if needed (at the console).  You have to load the data frame into memory with `data(BreastCancer)` Now run `str()` and `head()` on BreastCancer and `summary()` on just the Class column. Use R instructions to calculate the percent in each class, and print them with an appropriate heading using `paste()`. Answer the questions in step 1:
  1.	How many instances are there?
  2.	What is your target column?
  3.	How many predictors are there? What type of data are the predictors?
  4.	What percentage of the observations are malignant?

2.	Cell.size and Cell.shape are in one of 10 levels. Build a logistic regression model called `glm0`, where Class is predicted by Cell.size and Cell.shape. Do you get any error or warning messages? Google the message and try to decide what happened. Run `summary()` on `glm0` to confirm that it did build a model. Write a comment about why you think you got this warning message and what you could possibly do about it.  

3.	Notice in the `summary()` of `glm0` that most of the levels of Cell.size and Cell.shape became predictors and that they had very low p-values. We won’t be able to build a good logistic regression model this way.  It might be better to just have 2 levels for each variable. In this step, add two new columns to BreastCancer as listed below.  Run `summary()` on Cell.size and Cell.shape as well as the new columns. Comment on the distribution of the new columns. Do you think what we did is a good idea? Why or why not?
  1.	Cell.small which is a binary factor that is 1 if `Cell.size == 1` and 0 otherwise
  2.	Cell.regular which is a binary factor that is 1 if `Cell.shape == 1` and 0 otherwise	

4.	Create conditional density plots using the original Cell.size and Cell.shape. First `attach()` the data to reduce typing. Then use `par(mfrow = c(1,2))` to set up a 1x2 grid for two `cdplot()` graphs with `Class~Cell.size` and `Class~Cell.shape`. Observing the plots, write a sentence or two comparing size and malignant, and shape and malignant. Do you think our cutoff points for `size == 1` and `shape == 1` were justified now that you see this graph? Why or why not?

5.	Create plots (not cdplots) with our new columns. Again, use `par(mfrow = c(1,2))` to set up a 1x2 grid for two `cdplot()` graphs with `Class~Cell.small` and `Class~Cell.regular`. Now create two `cdplot()` graphs for the new columns. Now compute the following and provide a summary in the text portion of this answer. Also indicate based on these results if you think small and regular will be good predictors.
  1.	Calculate the percentage of small observations that are malignant
  2.	Calculate the percentage of not-small observations that are malignant
  3.	Calculate the percentage of regular observations that are malignant
  4.	Calculate the percentage of non-regular observations that are malignant

6.	Randomly divide BreastCancer into two data sets: train (80% of the data) and test (20%). Make sure you first set the seed to `1234` so you get the same results as others.

7.	Build a logistic regression classifier to estimate the probability of Class given Cell.small and Cell.regular. Run `summary()` on your model. Answer the following:
  1.	Which predictor(s) seem to be good predictors. Justify your answer.
  2.	Comment on the Null deviance versus the Residual deviance.
  3.	Comment on the AIC score. 

8.	Test the model on the test data and compute accuracy. What percent accuracy did you get?

9.	Your coefficients from the model are in units of logits.  Extract the coefficient of small with `glm1$coefficients[]`. Answer the following questions:
  1.	What is the coefficient?
  2.	How do you interpret this value?
  3.	Find the estimated probability of malignancy if Cell.small is true using `exp()`.
  4.	Find the probability of malignancy if Cell.small is true over the whole BreastCancer data set and compare results. Are they close? Why or why not?

10.	Build two more models, each just using Cell.small and Cell.regular and use `anova(glm_small, glm_regular, glm1)` to compare all 3 models, using whatever names you used for your models. Analyze the results of the `anova()`. Also, compare the 3 AIC scores of the models. Feel free to use the internet to help you interpret AIC scores. 
