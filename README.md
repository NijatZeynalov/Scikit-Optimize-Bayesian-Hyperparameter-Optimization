# Scikit-Optimize: Bayesian Hyperparameter Optimization
 Scikit Optimize implements several methods for sequential model-based optimization.  The library is very easy to use and provides a general toolkit for Bayesian optimization that can be used for hyperparameter tuning. It also provides support for tuning the hyperparameters of machine learning algorithms offered by the scikit-learn library.

Skopt makes this easy for you with their library skopt.space which lets us import Real, Integer, and Categorical to create the probability distributions.

## Space

Skopt makes this easy for you with their library skopt.space which lets us import Real, Integer, and Categorical to create the probability distributions.


__Real__ — This is a search space dimension that can take on any real value. You need to define the lower bound and upper bound and both are inclusive.

_Example: Real(low=0.2, high=0.9, name="min_samples_leaf")_

__Integer__ — This is a search space dimension that can take on integer values.

_Example: Integer(low=3, high=25, name="max_features")_

__Categorical__ — This is a search space dimension that can take on categorical values.

_Example: Categorical(["gini","entropy"],name="criterion")_


# Objective Function

This is a function that will be called by the search procedure. It receives hyperparameter values as input from the search space and returns the loss (the lower the better). This means that during the optimization process, we train the model with selected hyperparameter values and predict the target feature. Then we evaluate the prediction error and give it back to the optimizer.

The optimizer will decide which values to check and iterate over again. You will learn how to create an objective function in the practical example in the notebook.

# Optimizer

This is the function that performs the Bayesian Hyperparameter Optimization process. The optimization function iterates at each model and the search space to optimize and then minimizes the objective function.

There are different optimization functions provided by the scikit-optimize library, such as:

__dummy_minimize__ — Random search by uniform sampling within the given bounds.

__forest_minimize__ — Sequential optimization using decision trees.

__gbrt_minimize__ — Sequential optimization using gradient boosted trees.

__gp_minimize__ — Bayesian optimization using Gaussian Processes.

# Plot Convergence Traces

We can use the plot_convergence method from scikit-optimize to plot one or several convergence traces. We just need to pass the OptimizeResult object (result) in the plot_convergence method. For example, in the below plot a good value is found approximately after 10 iterations, but we need the 30 to find the minimum. 

![alt text](https://scikit-optimize.github.io/stable/_images/sphx_glr_bayesian-optimization_002.png)

# Why we should use Bayesian Optimisation?

Common hyperparameter tuning techniques such as GridSearch and Random Search roam the full space of available parameter values in an isolated way without paying attention to past results. Tuning by means of these techniques can become a time-consuming challenge especially with large parameters spaces. 

__Hyperparameter tuning by means of Bayesian reasoning, or Bayesian Optimisation, can bring down the time spent to get to the optimal set of parameters — and bring better generalisation performance on the test set. It does this by taking into account information on the hyperparameter combinations it has seen thus far when choosing the hyperparameter set to evaluate next.__

In other words, Bayesian Optimization also runs models many times with different sets of hyperparameter values, but it evaluates the past model information to select hyperparameter values to build the newer model. This is said to spend less time to reach the highest accuracy model.




Overall, I think Scikit-Optimize is a pleasure to use, gives you great results, and useful visualizations. Also, it has a lot of options to tweak with strong documentation to guide you through it.

# Resources:

https://towardsdatascience.com/the-beauty-of-bayesian-optimization-explained-in-simple-terms-81f3ee13b10f
