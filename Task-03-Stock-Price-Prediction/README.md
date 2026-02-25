### 📈 Stock Price Prediction (Next-Day Forecast)
#### Project Overview

This project focuses on predicting the next day’s closing price of a stock using historical market data. The model uses machine learning techniques to learn patterns from past stock behavior and estimate future prices.
The dataset is collected directly from Yahoo Finance using the yfinance Python library.

#### Objective

Fetch historical stock data using an API
Perform time series data handling
Use Open, High, Low, and Volume as input features
Predict the next day’s closing price
Compare actual vs predicted prices using visualization

#### Dataset

Source: Yahoo Finance
Library: yfinance
Stock Used: Apple (AAPL)
Time Period: 2020 – 2025

Features:
Open
High
Low
Volume

Target:
Next Day Closing Price

#### Technologies Used

Python
Pandas
NumPy
Matplotlib
Scikit-learn
yfinance

#### Machine Learning Model
Linear Regression

Steps:

Download historical stock data
Create a target column (Next_Close) using shift
Split data into training and testing sets
Train the model
Predict closing prices
Evaluate model performance

#### Time Series Handling
Since stock data is time-dependent:
Data order is preserved
shuffle=False is used during train-test split
Next day prediction is created using:
Next_Close = Close.shift(-1)

#### Results
Actual vs Predicted Prices

The predicted values closely follow the actual trend, showing that the model captures short-term price movement patterns.

#### Next-Day Prediction

The trained model is used to predict the next trading day’s closing price based on the most recent available data.