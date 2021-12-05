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
