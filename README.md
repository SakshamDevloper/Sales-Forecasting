# Sales-Forecasting

Dataset not included due to size.
Place raw_sales.csv inside data/ folder before running.

# Project Overview

This project focuses on forecasting daily revenue for a retail / e-commerce dataset using the ARIMA (AutoRegressive Integrated Moving Average) time series model.

The objective is to analyze historical transaction-level sales data, aggregate daily revenue, and generate short-term revenue forecasts to support business decision-making such as inventory planning and demand estimation.

# Dataset Description

The dataset contains transactional sales records with the following key fields:

-> Order ID
-> Date
-> SKU
-> Quantity (Qty)
-> Revenue (Amount)
-> Shipping City & State
-> Category

-> For time series modeling, transaction-level data was aggregated into daily total revenue.

# Methodology

-> The forecasting workflow follows a structured time series modeling pipeline:

# 1. Data Preprocessing

-> Converted Date column to datetime
-> Converted Amount to numeric
-> Removed missing values
-> Sorted data chronologically
-> Aggregated transaction data to daily revenue

# 2. Stationarity Check

-> Performed Augmented Dickey-Fuller (ADF) test
-> Applied first-order differencing (d=1) due to non-stationarity

# 3. Model Implementation

-> ARIMA (1,1,1) model selected
-> 80% training data / 20% testing data split
-> Model fitted on training dataset

# 4. Model Evaluation

Model performance was evaluated using:

RMSE : (Root Mean Squared Error)
MAE :(Mean Absolute Error)
MAPE : (Mean Absolute Percentage Error)

# 5. Model Performance

    Metric	     Value

->  RMSE	     118,954.73
->  MAE	         81,513.08
->  MAPE	     12.98%

# Interpretation

A MAPE of 12.98% indicates good forecasting accuracy for retail revenue prediction.