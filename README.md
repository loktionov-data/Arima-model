# ARIMA Forecasting Model  
**Time Series Forecasting of Monthly Airline Passengers**

## Overview  
This project focuses on time series forecasting using **ARIMA models**. It uses the classic "AirPassengers" dataset, representing monthly totals of international airline passengers from 1949 to 1960. The project explores stationarity, builds multiple ARIMA models, visualizes results, and selects the best configuration based on statistical criteria.

---

> ⚠️ This version improves upon previous work by introducing deeper model tuning (based on AIC/BIC), `ARIMA(4,0,3)` and `ARIMA(4,1,3)` variants, and clearer diagnostics.

---

## Project Workflow

1. **Data Preparation**
   - Import and inspect time series.
   - Apply log transform and `cumsum` for better stationarity.
  
2. **Stationarity Testing**
   - Augmented Dickey-Fuller test.
   - Visual inspection using rolling statistics.

3. **Differencing**
   - First-order and cumulative differencing applied.
   - Used to stabilize variance and trend.

4. **ACF & PACF Analysis**
   - Plots used for initial p/q estimation.
   - Though early signs suggested low-order AR/MA terms, deeper search found `ARIMA(4,0,3)` and `ARIMA(4,1,3)` to perform better.

5. **Model Selection**
   - Fit multiple ARIMA models.
   - Use AIC/BIC to compare and choose the optimal configuration.

6. **Forecasting**
   - Forecast future passenger volumes.
   - Visualize actual vs predicted values with confidence intervals.

---

## Visualizations

- Time series plot (original, log-transformed, differenced)
- ADF test summary
- ACF & PACF plots  
- ARIMA forecast vs actual

---

## Model Insights

- The best-performing models based on **AIC/BIC** were:
  - `ARIMA(4,0,3)`
  - `ARIMA(4,1,3)` (after `cumsum`)
- Despite PACF/ACF suggesting lower lags, full model tuning revealed these models to be more accurate.
- These models successfully captured both trend and noise in the data, producing realistic forecasts.

---

## Technologies Used

- **Python** (Jupyter Notebook)  
- **Libraries**:  
  - `pandas`, `numpy` – data handling  
  - `matplotlib`, `seaborn` – visualization  
  - `statsmodels` – ARIMA modeling and statistical tests

---

## Dataset

- **Source**: [AirPassengers dataset](https://datamarket.com/data/set/22u3/monthly-airline-passenger-numbers-in-1000s-jan-49-dec-60)  
- **Description**: Monthly totals of international airline passengers from 1949 to 1960.

---

## Key Takeaways

- ACF/PACF are useful guides but not final arbiters of model choice.
- Full model selection should involve **grid search** and **AIC/BIC comparison**.
- Forecasting performance depends on both good preprocessing and proper model tuning.
