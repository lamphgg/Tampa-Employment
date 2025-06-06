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

![image](https://github.com/user-attachments/assets/7457a8a4-1b96-4c38-8221-a0c81780edaf)


2. Data Visualization and Decomposition
- Visualizes the employment time series.
- Decomposes it into trend, seasonal, and residual components.
![image](https://github.com/user-attachments/assets/610cbcbd-2616-4133-88b3-f1765589f377)
![image](https://github.com/user-attachments/assets/a61435d2-7501-4b04-9893-a9f78d772119)

3. Linear Trend + Seasonality Model
- Fits a linear model with seasonal and trend components.
- Evaluates model performance using AIC/BIC.
- Forecasts 12 months ahead with 95% prediction intervals.
![image](https://github.com/user-attachments/assets/3f2c422b-376f-494e-b538-9fd302cae2d8)
![image](https://github.com/user-attachments/assets/5fba9a69-8c5c-457f-9e6c-50ac85039ea3)
![image](https://github.com/user-attachments/assets/3acb3c88-1a6e-47b2-9db4-ea35e98a384e)
![image](https://github.com/user-attachments/assets/20bc7730-4b8b-4bd4-bc13-5f61569f1914)

4. Quadratic Trend + Seasonality Model
- Adds a quadratic trend term to capture curvature.
- Forecasts and plots with prediction intervals.
![image](https://github.com/user-attachments/assets/6e304b31-b0e0-4a25-a10b-f828a255dca1)
![image](https://github.com/user-attachments/assets/1e75a578-a7c9-4bb3-a478-7177df26ac5a)

5. Log-Linear (Exponential Growth) Model
- Fits a log-transformed model with seasonal effects.
- Bias-adjusts back-transformed forecasts using the residual variance.
- Visualizes both log and level forecasts.
![image](https://github.com/user-attachments/assets/d2474d22-b504-4f21-93db-f2a92d71f5a8)
![image](https://github.com/user-attachments/assets/67c0f4be-67df-4c39-9eb9-10270d95d44e)
![image](https://github.com/user-attachments/assets/b86e07b8-64f2-4a1b-a505-72bcb78600d5)

6. Model Evaluation
- Plots fitted vs actual values for exponential model in both:
- Log scale
- Original (level) scale
![image](https://github.com/user-attachments/assets/be6d3104-9e6d-4cf6-a750-d71f2a63f82b)
![image](https://github.com/user-attachments/assets/08092e20-98a4-4564-bdb4-36aace318ade)


## Forecasting Techniques Used
- Classical Decomposition
- Time Series Linear Regression (tslm)
- Log-Transformation with Bias Adjustment
- Model Evaluation via AIC/BIC and Visual Diagnostics
