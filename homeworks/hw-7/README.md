# hw-7

Homework 7 in DSCI445: Statistical Machine Learning @ CSU

## Assignment

**Note:** Here is a useful list of functions for the methods in this chapter:

- Recipe steps `step_dummy(all_nominal_predictors())`, `step_normalize(all_predictors())`, and `step_pca(all_predictors(), threshold = tune())` create PCA components.
- Recipe steps `step_dummy(all_nominal_predictors())`, `step_normalize(all_predictors())`, and `step_pls(all_predictors(), threshold = tune())` create PLS components.

Be sure to `set.seed(445)`.

1. In this exercise we will predict the number of applications received using the other variables in the `College` data set (in the `ISLR` package).

    a) Split the data into training (60%) and "test" (40%) set randomly.
    
    b) Fit a PCR model on the training set with $M$ chosen using 10-fold CV (on the training set only). Report the test error obtained, along with the value of $M$ selected by CV.
    
    c) Fit a PLS model on the training set with $M$ chosen using 10-fold CV (on the training set only). Report the test error obtained, along with the value of $M$ selected by CV.
    
    d) Comment on the results obtained. How acurately can we predict the number of college applications received? Is there much difference among the test errors resulting from these approaches? Please also compare to your results from problem 2. in Homework 6.
    
2. We will now try to predict per capita crime rate in the `Boston` data set from the `ISLR` package.

    a. Try out some of the regression methods explored in this chapter such as best subset, the lasso, ridge regression, and PCR. Present and discuss results for the approaches that you consider.
    
    b. Propose a model or a set of models that seem to perform well on this data set and justify your answer. Make sure that you are evaluating performance using validation error, cross-validation error, or some other reasonable alternative (not just training error).
    
    c. Does your chosen model involve all of the features in the data set? Why or why not?

Turn in in a pdf of your homework to canvas using the provided Rmd file as a template. Your Rmd file on the server will also be used in grading, so be sure they are identical.

**Be sure to share your server project with the instructor and grader. You only need to do this once per semester.**

1. Open your `homeworks` project on liberator.stat.colostate.edu
2. Click the drop down on the project (top right side) > Share Project...
    
    <div class="figure">
    <img src="share_project.png" alt="plot of chunk unnamed-chunk-1" width="25%" />
    <p class="caption">plot of chunk unnamed-chunk-1</p>
    </div>
  
3. Click the drop down and add "dsci445instructors" to your project.

    <div class="figure">
    <img src="share_dropdown.png" alt="plot of chunk unnamed-chunk-2" width="25%" />
    <p class="caption">plot of chunk unnamed-chunk-2</p>
    </div>

This is how you **receive points** for reproducibility on your homework!

