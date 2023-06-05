# 9. Gold Recovery Prediction.
This project is based on real data from the gold mining sector, provided by [Zyfra](https://www.zyfra.com/), a company specializing in developing solutions for the efficient operation of industrial enterprises. A gold mining and refining company aims to optimize production by avoiding unprofitable processes. To achieve this, accurate prediction of the recovery coefficients of gold at rougher and cleaning stages is required.

[HTML](9_gold.html) [ipynb](9_gold.ipynb)

### Goal: 
Develop an ML model to predict the recovery coefficients of gold.<br>
Target performance metric: Symmetric Mean Absolute Percentage Error, **sMAPE**.
### Data:
Historical data from the rougher and cleaning stages of the gold recovery process: grain size and ore feed rate, amount of flotation reagents, characteristics of flotation banks, gold and other metal concentrations in ore, after cleaning and in tails. The data is indexed based on the date and time of information reception. Neighbouring parties generally exhibit similar performance patterns.
### Framework:
-	Data overview.
-	Exploratory data analysis: analysis of features and their interactions; analysis of concentration of metals at different stages of recovery process.
-	Data preprocessing: handling missing values, dealing with outliers.
-	Feature engineering: feature selection.
-	Model selection with cross-validation.
-	Model testing and feature importance.
-	General conclusion.
### Result:
Thorough EDA and feature selection were performed.<br>
*Models tested*: `LinearRegression`, `RandomForestRegressor`.<br>
*The best-performing model*: `RandomForestRegressor` (n_estimators = 190, max_depth = 8) for prediction of recovery coefficient from ore (median=87%, sMAPE = 8% on the test set) and `LinearRegression` for prediction of final recovery coefficient (median=68%, sMAPE = 9% on the test set).
Each model demonstrates about 1% lower sMAPE over Dummy models. **Total sMAPE = 9.1%**.<br>
The gold concentration in ore and ore grain size were identified as the primary factors with the strongest impact on the recovery coefficient of gold from ore. Metal concentrations in ore were also found to influence the final gold recovery coefficient, while factors such as the amount of flotation reagents were also identified as potentially significant. Analysis revealed that optimizing recovery parameters, such as the amount of flotation reagents, can lead to the recovery of higher quantities of gold even from ores with lower initial concentrations. 
#### Stack: 
- `Pandas`, `Matplotlib`, `Seaborn`, `NumPy`, `Scikit-learn`
-  *LinearRegression, RandomForestRegressor*
-  *Phik correlation*
