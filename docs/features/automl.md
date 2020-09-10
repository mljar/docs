# Steps of AutoML

The training of `mljar-supervised` AutoML is divided into steps. Each step represents the actions that are common in the process of constructing Machine Learning model in the ML pipeline. Below are described steps of AutoML. 

???+ note "Names of steps (`fit_level`)"
    In the documentation there are used exactly the same names as used in the code to describe each of the training level.
    You can see these names in the terminal during `AutoML` training.


## `simple_algorithms`

The first step in `AutoML` training is to check the simplest algorithms to get quick insights:

- `Baseline`,
- `Decision Tree`,
- `Linear`.

There is trained one model for each of the algorithm. By analyzing results of each model you can learn a lot about analyzed dataset:

- `Baseline` will provide the basline result without complex ML involved. 
    - It returns the most frequent label from the training data for classification tasks.
    - It returns the mean of the target from training data for regression tasks.
    - If further results are much better than `Baseline` results, **it justify the use of Machine Learning**. Take a look at [tutorial with classification of random data](/tutorials/random/).
- `Decision Tree` will provide results for simple tree (with `max_depth` up to 4). The tree will be visualized with [`dtreeviz`](https://github.com/parrt/dtreeviz) package, so you can easily check in the Markdown report what are the rules in the tree. 
- `Linear` will provide simple ML model. You can inspect coefficients to check which features are used.

The models in this step should be quickly trained, so you will get fast intuition about your data and the solved problem.

## `default_algorithms`

In this step, the models are trained with default hyperparameters. Regardless of the data, the hyperparameters are always used the same. In this step, you can compare the results of default models from other datasets and get intuition about your problem complexity.

The following algorithms can be fitted in this step:

- `Random Forest`,
- `Extra Trees`,
- `Xgboost`,
- `LightGBM`,
- `CatBoost`,
- `Neural Network`,
- `Nearest Neighbors`.

This is exactly one model fitted for each algorithm in this step. (Each algorithm has one set of default hyperparameters for each ML task)

## `not_so_random`

## `golden_features`

## `insert_random_feature`

## `features_selection`

## `hill_climbing`

## `ensemble`

## `stack`

## `ensemble_stacked`

