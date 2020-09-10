# Steps of AutoML

The training of `mljar-supervised` AutoML is divided into steps. Each step represents the actions that are common in the process of constructing Machine Learning model in the ML pipeline. Below are described steps of AutoML. 

There are used names that are used in the code.

???+ note "Names of steps (`fit_level`)"
    In the documentation there are used exactly the same names as used in the code to describe each of the training level.
    In the code, step can be represented as `fit_level` variable.


## `simple_algorithms`

The first step in `AutoML` training it to check the simplest algorithms:

- `Baseline`,
- `Decision Tree`,
- `Linear`.

There is trained one model for each of the algorithm. By analyzing results of each model we can learn a lot about analyzed dataset:

- `Baseline` will provide the result without complex ML involved. 
    - It returns the most frequent label from the training data for classification tasks.
    - It returns the mean of target from training data for regression tasks.
    - If further results are much better than `Baseline` results, it justify the use of Machine Learning. Take a look at [tutorial with classification of random data](/tutorials/random/).



## `default_algorithms`

## `not_so_random`

## `golden_features`

## `insert_random_feature`

## `features_selection`

## `hill_climbing`

## `ensemble`

## `stack`

## `ensemble_stacked`

