# Algorithms

## Baseline

### Classification

The `Baseline` algorithm is using scikit-learn algorithm: [`DummyClassifier`](https://scikit-learn.org/stable/modules/generated/sklearn.dummy.DummyClassifier.html). It is using strategy `prior` which returns most frequent class as label and class prior for `predict_proba()`.

### Regression

The `Baseline` algorithm is using scikit-learn algorithm: [`DummyRegressor`](https://scikit-learn.org/stable/modules/generated/sklearn.dummy.DummyRegressor.html). It is using strategy `mean` which returns mean of the target from training data.

!!! note "`Baseline` is not tuned"
    There will be only one model for algorithm `Baseline`. This algorithm has no hyperparameters.

## Decision Tree

### Classification 

The `Decision Tree` is using scikit-learn [`DecisionTreeClassifier`](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html).

!!! note "`Decision Tree` hyperparameters for classification"
    The allowed values of hyperparameters:
    ```python
    dt_params = {"criterion": ["gini", "entropy"], 
                 "max_depth": [2, 3, 4]}
    ```
    The default set of hyperparameters:
    ```python
    classification_default_params = {"criterion": "gini", "max_depth": 3}
    ```

### Regression

The `Decision Tree` is using scikit-learn [`DecisionTreeRegressor`](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html).

!!! note "`Decision Tree` hyperparameters for regression"
    The allowed values of hyperparameters:
    ```python
    dt_params = {
        "criterion": ["mse", "friedman_mse"], 
        "max_depth": [2, 3, 4]
    }
    ```
    The default set of hyperparameters:
    ```python
    classification_default_params = {"criterion": "mse", "max_depth": 3}
    ```

For `Decision Tree` a visualization can be created with `dtreeviz` package (not to have `explain_level > 0`).

## Linear

### Classification

The `Linear` is using scikit-learn [`LogisticRegression`](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html).

!!! note "`Linear` hyperparameters for classification"
    Thera are no hyperparameters for `Linear` model. The parameters used in `LogisticRegression` initialization: `max_iter=500, tol=5e-4, n_jobs=-1`.

### Regression

The `Linear` is using scikit-learn [`LinearRegression`](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html).

!!! note "`Linear` hyperparameters for regression"
    Thera are no hyperparameters for `Linear` model. The parameters used in `LinearRegression` initialization: `n_jobs=-1`.

The coefficients are saved in Markdown report if `explain_level > 0`.

## Random Forest

### Classification

The `Random Forest` is using scikit-learn [`RandomForestClassifier`](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html).

!!! note "`Random Forest` hyperparameters for classification"
    The allowed hyperparameters values:
    ```python
    rf_params = {
        "criterion": ["gini", "entropy"],
        "max_features": [0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
        "min_samples_split": [10, 20, 30, 40, 50],
        "max_depth": [4, 6, 8, 10, 12],
    }
    ```
    The default hyperparameters:
    ```python
    classification_default_params = {
        "criterion": "gini",
        "max_features": 0.6,
        "min_samples_split": 30,
        "max_depth": 6,
    }
    ```

### Regression

The `Random Forest` is using scikit-learn [`RandomForestRegressor`](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html).

!!! note "`Random Forest` hyperparameters for regression"
    The allowed hyperparameters values:
    ```python
    regression_rf_params = {
        "criterion": ["mse"],
        "max_features": [0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
        "min_samples_split": [10, 20, 30, 40, 50],
        "max_depth": [4, 6, 8, 10, 12],
    }
    ```
    The default hyperparameters:
    ```python
    regression_default_params = {
        "criterion": "mse",
        "max_features": 0.6,
        "min_samples_split": 30,
        "max_depth": 6,
    }
    ```

## Extra Trees

### Classification

The `Extra Trees` is using scikit-learn [`ExtraTreesClassifier`](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.ExtraTreesClassifier.html).

!!! note "`Extra Trees` hyperparameters for classification"
    The allowed hyperparameters values:
    ```python
    et_params = {
        "criterion": ["gini", "entropy"],
        "max_features": [0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
        "min_samples_split": [10, 20, 30, 40, 50],
        "max_depth": [4, 6, 8, 10, 12],
    }
    ```
    The default hyperparameters:
    ```python
    classification_default_params = {
        "criterion": "gini",
        "max_features": 0.6,
        "min_samples_split": 30,
        "max_depth": 6,
    }
    ```

### Regression

The `Extra Trees` is using scikit-learn [`ExtraTreesRegressor`](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.ExtraTreesRegressor.html).

!!! note "`Extra Trees` hyperparameters for regression"
    The allowed hyperparameters values:
    ```python
    regression_et_params = {
        "criterion": ["mse"],
        "max_features": [0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
        "min_samples_split": [10, 20, 30, 40, 50],
        "max_depth": [4, 6, 8, 10, 12],
    }
    ```
    The default hyperparameters:
    ```python
    regression_default_params = {
        "criterion": "mse",
        "max_features": 0.6,
        "min_samples_split": 30,
        "max_depth": 6,
    }
    ```

## Xgboost

The AutoML is using [`Xgboost`](https://xgboost.readthedocs.io/en/latest/index.html) package.

### Binary Classification

!!! note "`Xgboost` hyperparameters for binary classification"
    The allowed hyperparameters values:
    ```python
    xgb_bin_class_params = {
        "objective": ["binary:logistic"],
        "eval_metric": ["logloss"],
        "eta": [0.05, 0.075, 0.1, 0.15],
        "max_depth": [1, 2, 3, 4, 5, 6, 7, 8, 9],
        "min_child_weight": [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
        "subsample": [0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
        "colsample_bytree": [0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
    }
    ```
    The default hyperparameters:
    ```python
    classification_bin_default_params = {
        "objective": "binary:logistic",
        "eval_metric": "logloss",
        "eta": 0.1,
        "max_depth": 6,
        "min_child_weight": 1,
        "subsample": 1.0,
        "colsample_bytree": 1.0,
    }
    ```

### Multi-class Classification

!!! note "`Xgboost` hyperparameters for multi-class classification"
    The allowed hyperparameters values:
    ```python
    xgb_multi_class_params = {
        "objective": ["multi:softprob"],
        "eval_metric": ["mlogloss"],
        "eta": [0.05, 0.075, 0.1, 0.15],
        "max_depth": [1, 2, 3, 4, 5, 6, 7, 8, 9],
        "min_child_weight": [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
        "subsample": [0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
        "colsample_bytree": [0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
    }
    
    ```
    The default hyperparameters:
    ```python       
    classification_multi_default_params = {
        "objective": "multi:softprob",
        "eval_metric": "mlogloss",
        "eta": 0.1,
        "max_depth": 6,
        "min_child_weight": 1,
        "subsample": 1.0,
        "colsample_bytree": 1.0,
    }
    ```

### Regression

!!! note "`Xgboost` hyperparameters for regression"
    The allowed hyperparameters values:
    ```python
    xgb_regression_params = {
        "objective": ["reg:squarederror"],
        "eval_metric": ["rmse"],
        "eta": [0.05, 0.075, 0.1, 0.15],
        "max_depth": [1, 2, 3, 4],
        "min_child_weight": [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
        "subsample": [0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
        "colsample_bytree": [0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0],
    }
    
    ```
    The default hyperparameters:
    ```python       
    regression_default_params = {
        "objective": "reg:squarederror",
        "eval_metric": "rmse",
        "eta": 0.1,
        "max_depth": 4,
        "min_child_weight": 1,
        "subsample": 1.0,
        "colsample_bytree": 1.0,
    }
    ```

## CatBoost

The AutoML is using [`CatBoost`](https://catboost.ai/) package.

### Classification

!!! note "`CatBoost` hyperparameters for classification"
    The allowed hyperparameters values:
    ```python
    classification_params = {
        "learning_rate": [0.05, 0.1, 0.2],
        "depth": [2, 3, 4, 5, 6],
        "rsm": [0.7, 0.8, 0.9, 1],  # random subspace method
        "subsample": [0.7, 0.8, 0.9, 1],  # random subspace method
        "min_data_in_leaf": [1, 5, 10, 15, 20, 30, 50],
    }
    ```
    The default hyperparameters:
    ```python
    classification_default_params = {
        "learning_rate": 0.1,
        "depth": 6,
        "rsm": 0.9,
        "subsample": 1.0,
        "min_data_in_leaf": 15,
    }
    ```

- for binary classification `loss_function=Logloss`,
- for mutliclass classification `loss_function=MultiClass`.

## Regression

!!! note "`CatBoost` hyperparameters for regression"
    The allowed hyperparameters values:
    ```python
    regression_params = {
        "learning_rate": [0.05, 0.1, 0.2],
        "depth": [2, 3, 4, 5, 6],
        "rsm": [0.7, 0.8, 0.9, 1],  # random subspace method
        "subsample": [0.7, 0.8, 0.9, 1],  # random subspace method
        "min_data_in_leaf": [1, 5, 10, 15, 20, 30, 50],
    }
    ```
    The default hyperparameters:
    ```python       
    regression_default_params = {
        "learning_rate": 0.1,
        "depth": 6,
        "rsm": 0.9,
        "subsample": 1.0,
        "min_data_in_leaf": 15,
    }
    ```

For regression `loss_function=RMSE`.

## LightGBM


The AutoML is using [`LightGBM`](https://lightgbm.readthedocs.io/en/latest/) package.

### Binary Classification

!!! note "`LightGBM` hyperparameters for binary classification"
    The allowed hyperparameters values:
    ```python
    lgbm_bin_params = {
        "objective": ["binary"],
        "metric": ["binary_logloss"],
        "num_leaves": [3, 7, 15, 31],  
        "learning_rate": [0.05, 0.075, 0.1, 0.15],
        "feature_fraction": [0.8, 0.9, 1.0],
        "bagging_fraction": [0.8, 0.9, 1.0],
        "min_data_in_leaf": [5, 10, 15, 20, 30, 50],
    }
    ```
    The default hyperparameters:
    ```python
    classification_bin_default_params = {
        "objective": "binary",
        "metric": "binary_logloss",
        "num_leaves": 31,
        "learning_rate": 0.1,
        "feature_fraction": 0.9,
        "bagging_fraction": 0.9,
        "min_data_in_leaf": 10,
    }
    ```


### Multi-class Classification

!!! note "`LightGBM` hyperparameters for multi-class classification"
    The allowed hyperparameters values:
    ```python
    lgbm_bin_params = {
        "objective": ["multiclass"],
        "metric": ["multi_logloss"],
        "num_leaves": [3, 7, 15, 31], 
        "learning_rate": [0.05, 0.075, 0.1, 0.15],
        "feature_fraction": [0.8, 0.9, 1.0],
        "bagging_fraction": [0.8, 0.9, 1.0],
        "min_data_in_leaf": [5, 10, 15, 20, 30, 50],
    }
    ```
    The default hyperparameters:
    ```python
    classification_multi_default_params = {
        "objective": "multiclass",
        "metric": "multi_logloss",
        "num_leaves": 31,
        "learning_rate": 0.1,
        "feature_fraction": 0.9,
        "bagging_fraction": 0.9,
        "min_data_in_leaf": 10,
    }
    ```

### Regression

!!! note "`LightGBM` hyperparameters for regression"
    The allowed hyperparameters values:
    ```python
    lgbm_bin_params = {
        "objective": ["regression"],
        "metric": ["l2"],
        "num_leaves": [3, 7, 15, 31], 
        "learning_rate": [0.05, 0.075, 0.1, 0.15],
        "feature_fraction": [0.8, 0.9, 1.0],
        "bagging_fraction": [0.8, 0.9, 1.0],
        "min_data_in_leaf": [5, 10, 15, 20, 30, 50],
    }
    ```
    The default hyperparameters:
    ```python
    regression_default_params = {
        "objective": "regression",
        "metric": "l2",
        "num_leaves": 15,
        "learning_rate": 0.1,
        "feature_fraction": 0.9,
        "bagging_fraction": 0.9,
        "min_data_in_leaf": 10,
    }
    ```

## Neural Network

## Nearest Neighbor

## Stacked Algorithm

## Ensemble

