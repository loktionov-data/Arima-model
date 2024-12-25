# Arima-model

## Overview
This project explores time series forecasting using the **ARIMA (AutoRegressive Integrated Moving Average)** model on the popular **AirPassengers dataset**. The dataset consists of monthly airline passenger numbers from 1949 to 1960, making it a classic dataset for time series analysis.

## Key Features
1. **Dataset**:
   - **Source**: [Kaggle - AirPassengers Dataset](https://www.kaggle.com/datasets/georgerocha/airpassengers).
   - Contains monthly totals of international airline passengers (in thousands).
   - Covers the time period: **January 1949 – December 1960**.
2.**ARIMA Modeling**:
   - Data preprocessing and visualization.
   - Stationarity testing using the Augmented Dickey-Fuller (ADF) test.
   - Model selection and parameter tuning using auto_arima function from pdmarima library.
   - Forecasting future values using the ARIMA model.
3. **Visualization**:
   - Time series plots of the original data.
   - Predicted vs. actual values visualization.
---

## Technologies Used
- **Python** for data analysis and modeling.
- **Jupyter Notebook** for documenting and organizing the work.
- **Libraries**:
  - `pandas` and `numpy` for data manipulation.
  - `matplotlib`  for visualizations.
  - `statsmodels` and `pmdarima` for ARIMA modeling.
