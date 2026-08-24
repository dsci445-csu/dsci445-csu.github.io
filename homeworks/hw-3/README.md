# hw-3

Homework 3 in DSCI445: Statistical Machine Learning @ CSU

## Assignment


1. In this exercise you will create some simulated data and will fit simple linear regression models to it. Make sure to use `set.seed(445)` prior to starting part (a) to ensure reproducible results.

    (a) Using the `rnorm()` function, create a vector $x$ containing $100$ observations drawn from a $N(0, 1)$ distribution. This represents the feature, $X$.
    
    (b) Using the `rnorm()` function, create a vector `eps` containing $100$ observations drawn from a $N(0, 0.25)$ distribution, i.e. a Normal distribution with mean zero and variance $0.25$.
    
    (c) Using `x` and `eps`, generate a vector `y` according to the model
        $$
        Y = -1 + 0.5 X + \epsilon.
        $$
        What is the length of the vector `y`? What are the values of $\beta_0$ and $\beta_1$ in this linear model?
        
    (d) Create a scatterplot displaying the relationship between `x` and `y`. Comment on what you observe.
    
    (e) Fit a least squares linear model to predict `y` from `x`. Comment on the model obtained. How do $\hat{\beta}_0$ and $\hat{\beta}_1$ compare to $\beta_0$ and $\beta_1$?
    
    (f) Display the least squares line on the scatterplot obtained in (d) in blue. Draw the population regression line on the plot in red. (See `geom_abline()` for how to add a line based on intercept and slope.)
    
    (g) Now fit a polynomial regression model that predicts `y` using `x` and $\texttt{x}^2$. Is there evidence that the quadratic term improves the model fit? Explain your answer.
    
    (h) Repeat (a)-(f) after modifying the data generation process in such a way that there is *less* noise in the data. The model should remain the same. You can accomplish this by changing the variance of the normal distribution used to generate the error term $\epsilon$ in (b). Describe your results.
    
    (i) Repeat (a)-(f) after modifying the data generation process in such a way that there is *more* noise in the data. The model should remain the same. You can accomplish this by changing the variance of the normal distribution used to generate the error term $\epsilon$ in (b). Describe your results.
    
    (j) What are the confidence intervals for $\beta_0$ and $\beta_1$ based on the original data set, the noisier data set, and the less noisy data sets? Comment on your results.
        
2. When the number of features $p$ is large, there tends to be a deterioration in the perforance of KNN and other *local* approaches that perform prediction using only observations that are *near* the test observation for which a prediction must be made. This phenomenon is known as the *curse of dimensionality*, and it ties into the fact that non-parametric approaches often perform poorly when $p$ is large. We will now investigate this curse.

    (a) Suppose that we have a set of observations, each with measurements on $p = 1$ feature, $X$. We assume that $X$ is uniformly (evenly) distributed on $[0,1]$. Associated with each observation is a response value. Suppose that we wish to predict a test observation's response using only observations that are within $10\%$ of the range of $X$ closest to that test observation. For instance, in order to predict the response for a test observation with $X = 0.6$ we will use observations in the range $[0.55, 0.65]$. On average, what fraction of the available observations will we use to make this prediction?
    
    (b) Now suppose that we have a set of observations, each with measurements on $p = 2$ features, $X_1$ and $X_2$. We assume $(X_1, X_2)$ are uniformly distributed on $[0,1]\times[0,1]$. we wish to predict a test observation's response using only observations that are within $10\%$ of the range of $X_1$ *and* within $10\%$ of the range of $X_2$ closest to that test observation. For instance, in order to predict the response for a test observation with $X_1 = 0.6$ and $X_2 = 0.35$ we will use observations in the range $[0.55, 0.65]$ for $X_1$ and in the range $[0.3, 0.4]$ for $X_2$. On average, what fraction of the available observations will we use to make this prediction?
    
    (c) Now suppose that we have a set of observations, each with measurements on $p = 100$ features. Again, the observations are uniformly distributed on each feature, and again each feature ranges from $0$ to $1$. we wish to predict a test observation's response using only observations that are within $10\%$ of each feature's range that is closest to that test observation. What fraction of the available observations will we use to make this prediction?
    
    (d) Using your answers to (a)--(c), argue that a drawback of KNN when $p$ is large is that there are very few training observations *near* any given test observation.
    
    (e) Now suppose that we wish to make a prediction for a test observation by creating a $p$-dimensional hypercube centered around the test observation that contains, on average, $10\%$ of the training observations. For $p = 1, 2,$ and $100$, what is the length of each side of the hypercube? Comment on your answer.
    
        [Hint: A hypercube is a generalization of a cube to an arbitrary number of dimensions. When $p = 1$, a hypercube is simple a line segment. When $p = 2$ it is a square, and when $p = 100$ it is a $100$-dimensional cube.]
        

Turn in in a pdf of your homework to canvas using the provided Rmd file as a template. Your Rmd file on the server will also be used in grading, so be sure they are identical.

**Be sure you have shared your server project with the instructor and grader. You only need to do this once per semester.**

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

