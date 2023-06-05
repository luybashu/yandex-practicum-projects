# 12. Forecasting Taxi Orders.
In order to optimize its operations at airports and increase profits, a taxi company is seeking to attract more drivers during peak periods. To achieve this, accurate prediction of the number of taxi orders for the next hour is crucial. 

[HTML](12_taxi.html)   [ipynb](12_taxi.ipynb)

### Goal: 
Develop an ML model to predict the number of taxi orders for the next hour.<br>
Target performance metric: **RMSE < 48**.
### Data: 
Historical data on taxi orders at airports.
### Framework:
-	Data overview and preprocessing.
-	Exploratory data analysis: time series analysis (trends and seasonality).
-	Data preprocessing: handling missing values, dealing with outliers.
-	Feature engineering: feature creation.
-	Model selection with cross-validation.
-	Model testing; evaluating model performance.
-	General conclusion.
### Result:
Through time series analysis (trends and seasonality) essential features were created that facilitated the development of relatively precise and fast ML model for prediction of the number of taxi orders for the next hour.<br> 
*Models tested:* `LinearRegression`, `RandomForestRegressor`, `LGBMRegressor`, `CatBoostRegressor`.<br>
*The best-performing model:* `LinearRegression`, **RMSE = 35.5** on the test set.<br> 
It should be noted that the model does not predict well extreme outliers, such as significantly higher or lower numbers of taxi orders. To address this, analyzing residuals, incorporating additional factors (e.g., flight numbers), or considering a smaller test sample size could be beneficial.
### Stack: 
- `Pandas`, `Matplotlib`, `Seaborn`, `NumPy`, `Statsmodels`,` Scikit-learn`
-  *LinearRegression, RandomForestRegressor, CatBoostRegressor, LGBMRegressor*
-  *autocorrelation*
