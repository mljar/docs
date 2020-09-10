# Steps of AutoML

The training of `mljar-supervised` AutoML is divided into steps. Each step represents the actions that are common in the process of constructing Machine Learning model in the ML pipeline. Below are described steps of AutoML. 

???+ note "Algorithms used"
    In this section that you are not excluding any algorithms (which can be done by setting `algorithms` argument in `AutoML` constructor). 

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
- `Decision Tree` will provide results for simple tree (up to 4 `max_depth`). The tree will be visualized with [`dtreeviz`](https://github.com/parrt/dtreeviz) package, so you can easily check in the Markdown report what are the rules in the tree. 
- `Linear` will provide simple ML model. You can inspect coefficients to check which features are used.

The models in this step should be trained quickly, so you will get fast intuition about your data and the problem that is solved.

## `default_algorithms`

In this step, the models with default hyper-parameters are trained. 

## `not_so_random`

## `golden_features`

## `insert_random_feature`

## `features_selection`

## `hill_climbing`

## `ensemble`

## `stack`

## `ensemble_stacked`

