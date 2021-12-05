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






Overall, I think Scikit-Optimize is a pleasure to use, gives you great results, and useful visualizations. Also, it has a lot of options to tweak with strong documentation to guide you through it.
