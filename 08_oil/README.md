# 8. Selection of the oil production regionn.
This project uses synthetic data in the oil production sector. An oil-producing company needs to determine the most profitable region.<br>
**Steps for selecting the oil production region:**
-	Collecting characteristics of oil wells in each region: oil quality and volume of reserves;
-	Developing an ML model to predict the reserve volume in new wells;
-	Selecting oil wells with the highest reserve volumes, considering the company's budget and the cost of well development;
-	Determining the region with the maximum total profit from the new oil wells.

[HTML](8_oil.html) [ipynb](8_oil.ipynb)

### Goal: 
Determine the region that will yield the highest profit from oil production. Using an ML model, select the most profitable oil wells and analyze the possible profit and risks for each region applying the Bootstrap technique.<br>
**Conditions**:
-	Linear regression is the only suitable model.
-	Each region undergoes exploration of 500 oil wells, from which the top 200 should be selected for development.
-	The budget allocated for the development of wells is 10 billion rubles.
-	The price of one barrel of oil is 450 rubles (450 000 rubles per 1000 barrels).
-	Only regions with a probability of losses below 2.5% are considered suitable for development.

### Data:
Synthetic “historical” data on oil wells from three different regions, each consisting of 100,000 wells. The recorded measurements include oil quality (based on three different features) and the volume of reserves (in thousand barrels) for each well.

### Framework:
-	Data overview.
-	Exploratory data analysis: analysis of features and their interactions.
-	Model training.
-	Model testing and feature importance.
-	Analysis of profits and risks for each region.
-	Analysis of risks and profits for each region using statistical data analysis tools.
-	General conclusion.

### Result:
EDA revealed significant variations in the characteristics of oil and its reserves across different regions.<br>
Utilizing the *linear regression model*, predictions for oil reserve volumes were made. The average predicted volume closely matched the average actual values within each region. Region 2 demonstrated the highest accuracy in predictions, achieving RMSE=0.9 thousand barrels, while other regions exhibited RMSE values around 40.<br>
Feature `f2` was found to have the strongest impact on the reserve volume of oil in wells.<br>
Despite having a lower overall reserve volume of oil, Region 2 was recommended for the development of new wells due to its more accurate predictions of oil reserve volumes and the lowest probability of losses (only 1%).

#### Stack: 
- `Pandas`, `Matplotlib`, `Seaborn`, `NumPy`, `Scikit-learn`
-  *LinearRegression*
-  *Phik correlation, Bootstrap*
