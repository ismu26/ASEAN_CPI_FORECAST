# ASEAN_CPI_FORECAST
Interactive Shiny app for CPI forecasting using ARIMA and custom VAR models. Features include rolling backtests, synthetic oil path simulation, dynamic predictor selection, and exportable results. Fully data-agnostic and designed for macroeconomic scenario analysis.

# CPI Forecasting Shiny App  
*A dynamic interface for ARIMA and custom VAR modeling with synthetic oil path support*

## Overview
This Shiny application provides an interactive platform for forecasting Consumer Price Index (CPI) using **ARIMA** and **VAR-style regression models**. Users can select a country, model type, forecast horizon, and predictor variables. The app supports **12-month ahead forecasts**, **rolling one-step-ahead backtesting**, and **RMSE/MAE performance evaluation**.

The model framework replicates EViews-style logic and includes examples of:
- Monthly–quarterly data alignment  
- Shock dummy construction  
- MIDAS-inspired lag handling via synthetic oil paths (Almon-like structure)

> ⚠ **No data is included in this repository.** Users must load their own cleaned dataset following the template in `global.R`.

---

## Key Features
- ARIMA & Custom VAR forecasting  
- One-step rolling backtest  
- Synthetic oil path dependent on user-defined shock  
- Visualized forecast & evaluation metrics (MoM & YoY)  
- CSV export via `downloadButton()` after forecast execution  
- Dynamic UI & date range auto-adjustment  
- Automatic fallback logic for model non-convergence

---

## How to Use
1. Load custom dataset into `load_country_data()`
2. Select model type (ARIMA or VAR)
3. Define forecast horizon and predictor set  
4. Optionally input a custom oil shock  
5. Run forecast & review charts and accuracy metrics  
6. Export results to CSV

---

## File Structure
├── app.R / ui.R / server.R
├── global.R # Data loading & preprocessing
├── README.md
