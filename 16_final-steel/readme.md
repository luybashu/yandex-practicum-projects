# 16. Final Project. Alloy Temperature Prediction.
A steel mill needs to optimize production costs by reducing electricity consumption during the steel processing stage. By accurately predicting the alloy temperature at the end of processing, more efficient process protocols can be developed.

[HTML](link) [ipynb](link)
### Goal: 
Develop an ML model to predict the final temperature of the alloy.<br>
Target performance metric: **MAE < 6.8**.
### Data: 
Historical data obtained from various sources during different steps of alloy processing: temperature measurements; heating data; supply of bulk and wire alloy additions; gas purge information. 
### Result:
Thorough EDA, feature selection, and engineering enabled the development of an ML model with low temperature prediction error.<br> 
*Models tested*: `ElasticNet`, `LGBMRegressor`, `CatBoostRegressor`.<br>
*The best-performing model*: `CatBoostRegressor` (n_estimators = 132, learning_rate = 0.1, l2_leaf_reg = 3, depth = 4), **MAE = 5.2** on the test set.<br>
The factors found to have the strongest impact on the final temperature were the total active power for alloy heating and the initial temperature of the alloy. The duration of the period without heating and the steel "grade" showed relatively less importance, while the amount of gas used for purge had the least effect.<br>
The customer was provided with insights into the existing data issues, along with recommendations based on the model results. 
Potential avenues for model improvement were suggested.
### Stack:<br>
- `Pandas`, `Matplotlib`, `Seaborn`, `NumPy`, `Scikit-learn`
- *ElasticNet, LGBMRegressor, CatBoostRegressor*
- *Pipline, Phik correlation, KNN*
