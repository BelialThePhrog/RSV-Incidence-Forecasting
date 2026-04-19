# Epidemiological Time Series Forecasting: RSV Incidence in Poland 

This repository contains a predictive time-series model designed to forecast Respiratory Syncytial Virus (RSV) incidence rates per 100,000 inhabitants.

## Project Objective
The goal is to provide short-term epidemiological forecasts using public healthcare data (ezdrowie.gov.pl). Accurately predicting the incidence rate allows healthcare providers to optimize pediatric bed allocation ahead of peak infection seasons.

## Technology Stack
* **Language:** Python 3
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning & Modeling:** `scikit-learn` (Linear Regression applied to a first-order difference equation)
* **Visualization:** `matplotlib`

## Methodology
The forecast is built using a first-order difference equation model:
`y_t = a * y_{t-1} + b`

Where:
* `a` captures the dependency on the previous week's incidence rate.
* `b` accounts for the baseline growth/decline rate.
Model parameters were estimated using Linear Regression on historical data.

## Key Insights
The model successfully identifies the cyclical nature of RSV outbreaks and provides actionable predictions for the upcoming weeks. By projecting current trends, the forecast indicates stabilization patterns, which are crucial for epidemiological preparedness.
