# Bitcoin-Price-Prediction-using-ML
# Project Summary: Hourly Bitcoin Price Forecasting Using Regression and Deep Learning

Objective
The purpose of this project is to analyze hourly Bitcoin market data to:
Perform comprehensive data analysis,
Identify the most impactful features through feature selection techniques,
Build regression models to establish baseline performance,
Implement a deep learning model (LSTM) to predict Bitcoin prices for the next 30 days based on historical data.
Steps and Methodology¶
1. Data Preprocessing and Exploration
Missing values were handled using forward-fill (ffill).
The timestamp column was parsed into datetime format and set as the index.
Numerical features were scaled using MinMax normalization to prepare for modeling.
2. Correlation Analysis & Feature Selection
A correlation matrix was generated to identify features with the highest correlation (positive and negative) to the target variable.
The main target selected was BTC_USDT_1h_close (hourly closing price).
Feature selection was guided by correlation strength and R² score performance
Regression Modeling and Comparison¶
Several regression models were trained: Linear Regression, Ridge, Lasso and Random Forest.
Their performances were evaluated and compared using the R² score on a hold-out test set.
4. LSTM-Based Time Series Forecasting
A Long Short-Term Memory (LSTM) neural network was developed using 72-hour input windows.
The model was trained to forecast 720 future time steps (i.e., the next 30 days of hourly BTC prices).
The prediction loop was configured to run silently (verbose=0) to avoid excessive console output.
5. Visualization
The last 300 hours of actual BTC prices were plotted alongside the 30-day forecast.
A clear time-based chart was produced to illustrate the model's predictive performance visually.

# Bitcoin Hourly Close Price
![image](https://github.com/user-attachments/assets/5d799fc9-dad3-471d-b39c-8677e73dff5b)

# Linear Regression:

R2 Score: 0.9999801708098015
Mean Squared Error: 11490.68445796558
Mean Absolute Error: 61.407465946792016

# Ridge Regression:
R2 Score: 0.9999857321929796
Mean Squared Error: 8267.95581349173
Mean Absolute Error: 51.09918937061915

# Next 30 Days Price Prediction using LSTM:
![image](https://github.com/user-attachments/assets/447c0cea-5a5a-4bbd-bca8-131a6ec7ae62)


