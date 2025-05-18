-- WIP --
Expecting it to be published next week

# Portfolio and Asset Management App

Key Features
Multiple Forecasting Models: Implements ARIMA and BSTS for robust predictions

Ensemble: Uses a weighted averaging method based on error metrics to create a ARIMA-BSTS Ensemble Forecast

Model-Based Uncertainty Quantification

Market Regime Detection: Identifies different market states (Bear, Neutral, Bull), determining probabilities of transitioning regime, average regime return, and duration. 

Alternative Data: Incorporates news sentiment, Macroeconomic indicators, and (WIP) Volume Analysis.

Technical Indicators: Calculates and visualizes a variety of technical indicators, support and resistance levels, and provides a (WIP) technical summary.

Risk Analysis: (WIP) Greeks, Market Dependencies (Equity, Market, Bond), (WIP) SSVI Surface

Portfolio Analysis: This tab focuses on Portfolio Performance Metrics (VaR, ES, Maximum Drawdown), Portfolio Correlation, Return Distribution, and Efficient Frontier Optimisation

Model Diagnostics: Conducts diagnostics to validate model quality


Installation
Prerequisites
R 4.0.0 or higher RStudio (this is recommended for some packages are built in 4.0.0)

Required Packages
The app requires numerous R packages. The main script includes code to check and install any missing dependencies:

rCopyrequired_packages <- c(
  # Core packages
 "shiny", "shinydashboard", "plotly", "forecast", "bsts", "DT", 
  "tidyverse", "lubridate", "quantmod", "Metrics", "bizdays", "TTR", 
  "zoo", "fredr", "torch", "glmnet", "tseries", "caret", "ggplot2", 
  # Additional packages
  "depmixS4", "roll", "mvtnorm", "xgboost", "shinyjs", "progressr",
  "reshape2", "htmlwidgets", "shinyWidgets", "markdown", "scales"
)

Setup:
- Clone or download this repository
- Open the project in RStudio
- Set your FRED API key in the Helpers.R file (for access to economic data)
- Set Alpha Vantage Key in Helpers.R file (for news retrieval and back up data)
- Set Financial modelling prep key in helpers.R file (for further financial data)
- Run the app
  
Usage Guide

Data Selection:
- Enter a stock symbol (e.g., "AAPL")
- Set historical date range
  
Configure Forecast Settings:
- Set forecast horizon
- Select models to include in the analysis
- Pick ensemble method
- Pick Uncertainty Method

  
Run Forecast:
Click "Run Forecast" to generate predictions

Review:
- Click forecasting tab to view forecast predictions
- View Model diagnostics tab to analyse the accuracy of the produced forecast/s


Guide

The app implements two forecasting models:

- ARIMA/X: Autoregressive Integrated Moving Average with Inflation, Volatility, Volume, and Seasonality as selectable external variables

- BSTS: Bayesian Structural Time Series

Ensemble Method:

- Adaptive Ensemble: Dynamically adjusts weights based on error metrics

Uncertainty Quantification: 

- Model-Based Uncertainty Quantification

Confidence Level Guide: 

- 
-
-

Disclaimer
This application is intended for educational and research purposes only. 

License
This project is licensed under the MIT License - see the LICENSE file for details.
