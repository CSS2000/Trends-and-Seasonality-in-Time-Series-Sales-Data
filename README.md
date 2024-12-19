## Time Series Analysis and Forecasting 
Overview
This project demonstrates various techniques for time series analysis and forecasting, focusing on models such as SARIMA, ARIMA, TBATS, and Facebook Prophet. The models are applied to revenue and sales datasets, exploring their ability to capture trends, seasonality, and noise for accurate predictions.

Prerequisites
The following Python libraries are required:

pandas
numpy
matplotlib
statsmodels
scikit-learn
pmdarima
tbats
fbprophet
Install them using:

pip install pandas numpy matplotlib statsmodels scikit-learn pmdarima tbats prophet
Dataset
Input Data:
Aggregated Revenue Dataset (df_agg):
Total Revenue: Original time series data.
RevenueDiff1: Differenced data to make the series stationary.
Australian Drug Sales (aust_drug_df):
Monthly anti-diabetic drug sales data from 1992 to 2008.
Workflow
1. Data Preparation
Load datasets.
Check for stationarity using differencing (RevenueDiff1).
Split datasets into training and testing sets (last 12 months for testing).
2. SARIMA Modeling
Configure (p, d, q) and (P, D, Q, S) parameters.
Fit the SARIMA model using SARIMAX.
Evaluate using metrics:
Root Mean Squared Error (RMSE)
Mean Absolute Error (MAE)
R² Score
Backtransform forecasts if differencing was applied.
3. ARIMA Model
Use ARIMA from statsmodels with grid search to tune parameters.
Automate parameter selection using auto_arima from pmdarima.
4. TBATS Model
Use TBATS for datasets with complex seasonal patterns.
Train the model and extract key parameters:
alpha, beta
Seasonal harmonics
5. Facebook Prophet
Use Prophet for trend and seasonality-based forecasting.
Train on the dataset and generate future forecasts.
Visualize components such as trend and seasonality.
6. Evaluation
Compare models using:
RMSE
MAE
R² Score
Highlight the better-performing model (e.g., SARIMA for seasonal datasets).
Results
ARIMA:

RMSE: 692.151
MAE: 534.061
SARIMA:

RMSE: 412.061
MAE: 320.800
SARIMA outperformed ARIMA due to its ability to handle seasonal components effectively.

Visualization
Original series vs. forecast.
Autocorrelation (ACF) and Partial Autocorrelation (PACF).
Component analysis (trend, seasonality).
References:
 https://www.analyticsvidhya.com/blog/2021/10/a-comprehensive-guide-to-time-series
analysis/#Converting_Non-Stationary_Into_Stationary
 https://towardsdatascience.com/time-series-analysis-with-facebook-prophet-how-it-works
and-how-to-use-it-f15ecf2c0e3a
 https://www.analyticsvidhya.com/blog/2021/06/statistical-tests-to-check-stationarity-in-time
series-part-1/#:~:text=There%20are%20various%20statistical%20tests,unit%20root%20in
 %20the%20data.
 https://towardsdatascience.com/time-series-forecasting-based-on-the-trend-and-seasonal
components-26b92866e548
 https://www.geeksforgeeks.org/time-series-analysis-using-facebook-prophet/
 https://towardsdatascience.com/time-series-analysis-with-facebook-prophet-how-it-works
and-how-to-use-it-f15ecf2c0e3a
 https://medium.com/analytics-vidhya/time-series-forecasting-using-tbats-model
ce8c429442a9
 https://www.influxdata.com/blog/forecasting-with-fb-prophet-and-influxdb
