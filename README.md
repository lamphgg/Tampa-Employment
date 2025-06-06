# Tampa Employment Forecasting in R

This project performs a time series analysis and forecasting on employment data from Tampa using R. It demonstrates how to apply classical linear models, quadratic trend models, and log-linear (exponential growth) models to real-world economic data.

---

## Installation

To get started, install the required R packages:

install.packages("forecast")
install.packages("readxl")
install.packages("lmtest")
install.packages("tseries")

Then, load the libraries

library(forecast),
library(readxl),
library(lmtest),
library(tseries),

## Project Workflow
1. Data Summary
- Loads and summarizes employment data (EMPTPA) from Excel.
- Converts data into a time series object (monthly frequency starting from 2000).

2. Data Visualization and Decomposition
- Visualizes the employment time series.
- Decomposes it into trend, seasonal, and residual components.

3. Linear Trend + Seasonality Model
- Fits a linear model with seasonal and trend components.
- Evaluates model performance using AIC/BIC.
- Forecasts 12 months ahead with 95% prediction intervals.

4. Quadratic Trend + Seasonality Model
- Adds a quadratic trend term to capture curvature.
- Forecasts and plots with prediction intervals.

5. Log-Linear (Exponential Growth) Model
- Fits a log-transformed model with seasonal effects.
- Bias-adjusts back-transformed forecasts using the residual variance.
- Visualizes both log and level forecasts.

6. Model Evaluation
- Plots fitted vs actual values for exponential model in both:
- Log scale
- Original (level) scale

## Forecasting Techniques Used
- Classical Decomposition
- Time Series Linear Regression (tslm)
- Log-Transformation with Bias Adjustment
- Model Evaluation via AIC/BIC and Visual Diagnostics
