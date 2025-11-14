# Sales-trend-forecasting
# Sales Trend Forecasting & Event Fusion Engine - Example

This repository contains a self-contained example program that demonstrates how to build a sales forecasting pipeline that fuses external events (holidays, promotions, weather), quantifies uncertainty, and identifies influential factors.

> **Note:** This is a demonstration project with a synthetic data generator included. Replace the synthetic data with your real dataset (CSV) by modifying the data loading section in `main.py`.

## What the program does

- Generates synthetic daily sales data plus event features (holidays, promotions, weather).
- Creates lag, rolling, and cyclical features.
- Trains:
  - A point forecast model (Gradient Boosting Regressor).
  - Two quantile regressors (lower and upper) to produce prediction intervals (10th and 90th percentiles).
- Evaluates model performance (MAE, RMSE, coverage of prediction intervals).
- Produces a 28-day future forecast using a simple recursive approach.
- Outputs feature importances to identify which signals drive predictions.
- Saves models and CSV outputs into `./output`.

## Requirements

- Python 3.8+
- The following Python packages:
  - numpy
  - pandas
  - scikit-learn
  - matplotlib
  - joblib

You can install dependencies with pip:

```bash
pip install numpy pandas scikit-learn matplotlib joblib
