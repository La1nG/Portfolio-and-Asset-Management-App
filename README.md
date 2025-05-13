-- WIP --

# Portfolio and Asset Management App

Key Features
Multiple Forecasting Models: Implements ARIMA and BSTS for robust predictions

Ensemble: Uses a weighted averaging method based on error metrics to create a ARIMA-BSTS Ensemble Forecast

Model-Based Uncertainty Quantification

Market Regime Detection: Identifies different market states (Bear, Neutral, Bull), determining probabilities of transitioning regime, average regime return, and duration. 

Alternative Data: Incorporates news sentiment, Macroeconomic indicators, and Volume Analysis.

Technical Indicators: Calculates and visualizes a variety of technical indicators, support and resistance levels, and provides a technical summary.

Model Diagnostics: Conducts residual analysis and statistically validates model quality

--------------------------------------------------------------------------------------------------------------------------------------
(WIP) Risk Analysis - Greeks, Market Dependencies (Equity, Market, Bond), SSVI Surface

(WIP) Portfolio Analysis 

(WIP) Valuation

---------------------------------------------------------------------------------------------------------------------------------------

Installation
Prerequisites
R 4.0.0 or higher RStudio (recommended)

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
- Click forecasting tab to view forecast predictions and uncertainty intervals
- View Model diagnostics and Model Validations tabs to analyse the accuracy and viability of the produced forecast/s


Guide

The app implements several state-of-the-art forecasting models:

- ARIMA: Autoregressive Integrated Moving Average

- BSTS: Bayesian Structural Time Series

- XGBoost: Gradient boosting for time series

Ensemble Methods

Multiple models are combined using various ensemble techniques:

- Bayesian Model Averaging: Weights models based on probabilities

- Adaptive Ensemble: Dynamically adjusts weights based on recent performance

Uncertainty Quantification

The app provides two methods for calculating prediction intervals:

- Bootstrap: Resamples historical data to estimate forecast variability

- Bayesian: Leverages parameter uncertainty for probabilistic intervals

Contributing
Contributions and suggestions to this App are welcome and appreciated. Please feel free to submit pull requests or open issues to help improve functionality, let me know about bugs, or enhance documentation.

Disclaimer
This application is intended for educational and research purposes only. 

License
This project is licensed under the MIT License - see the LICENSE file for details.
