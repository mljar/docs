# Modes

| | |**AutoML Modes**| |
|--- |--- |--- |--- |
||**Explain**|**Perform**|**Compete**|
|*Algorithms*| | | |
|Baseline|:fontawesome-solid-check:{: .green } |||
|Linear|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|Decision Tree|:fontawesome-solid-check:{: .green } ||:fontawesome-solid-check:{: .green } |
|Random Forest|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|Extra Trees|||:fontawesome-solid-check:{: .green } |
|XGBoost|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|LightGBM||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green }|
|CatBoost||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|Neural Network|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|Nearest Neighbors|||:fontawesome-solid-check:{: .green } |
|Ensemble|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|Stacking|||:fontawesome-solid-check:{: .green } |
|*Validation*| | ||
||75%/25% train/test split|5-fold CV, Shuffle, Stratify| 10-fold CV, Shuffle, Stratify|
|*Explanations*| | | |
||`explain_level=2`|`explain_level=1`|`explain_level=0`|
|Learning   curves|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|Importance   plots|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } ||
|SHAP   plots|:fontawesome-solid-check:{: .green } |||
|*Steps*||||
|simple_algorithms|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|default_algorithms|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|not_so_random||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|golden_features||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|insert_random_feature||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|feature_selection||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|hill_climbing_1||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|hill_climbing_2||:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|ensemble|:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |:fontawesome-solid-check:{: .green } |
|stack|||:fontawesome-solid-check:{: .green } |
|ensemble_stacked|||:fontawesome-solid-check:{: .green } |
