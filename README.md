# 📈 Volatility Forecasting and Portfolio Optimization for Financial Markets

> **Can better volatility forecasts lead to better portfolio decisions?**

This project investigates whether incorporating advanced statistical and machine learning-based volatility forecasting models into portfolio construction results in superior risk-adjusted investment performance compared to traditional portfolio optimization approaches.

Unlike conventional finance projects that focus solely on price prediction or portfolio optimization, this work bridges **statistical modeling, financial econometrics, machine learning, optimization, explainability, and quantitative risk management** into one end-to-end financial analytics pipeline.

---

# 🎯 Project Objective

The primary objective of this study is to determine whether **improved volatility forecasting translates into improved portfolio performance**.

Instead of treating volatility prediction as an isolated forecasting problem, this project integrates predicted market risk into portfolio optimization and evaluates its impact using realistic rolling-window backtesting.

---

# Research Question

> **Does improving volatility forecasts using statistical and machine learning models lead to significantly better portfolio construction than traditional historical-risk approaches?**

---

# Motivation

Portfolio optimization relies heavily on accurate estimates of future risk.

Traditional methods generally assume that historical volatility represents future risk. Financial markets, however, exhibit:

* Time-varying volatility
* Volatility clustering
* Heavy tails
* Structural breaks
* Non-linear relationships

Machine learning provides the opportunity to capture complex market dynamics that traditional models may overlook.

This project investigates whether these improved forecasts can produce portfolios with superior risk-adjusted returns.

---

# Dataset

## Universe

* S&P 100 Constituents

## Time Period

2014 – 2025

## Frequency

Daily

## Data Sources

* Yahoo Finance
* CBOE VIX Index
* FRED (Risk-Free Rate)

---

# Data Collected

For every stock:

* Open
* High
* Low
* Close
* Adjusted Close
* Volume

Additional Market Variables

* VIX
* S&P 500 Index
* Risk-Free Rate

---

# Project Pipeline

```
Data Collection
        │
        ▼
Data Cleaning
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Future Volatility Target Construction
        │
        ▼
Volatility Forecasting Models
        │
        ▼
Model Evaluation
        │
        ▼
Portfolio Optimization
        │
        ▼
Rolling Backtesting
        │
        ▼
Risk & Performance Evaluation
        │
        ▼
Statistical Validation
        │
        ▼
Model Explainability
```

---

# Exploratory Data Analysis

The project performs detailed statistical analysis including:

* Return distributions
* Rolling volatility
* Correlation analysis
* Sector-wise volatility comparison
* QQ Plots
* Histograms
* Boxplots

Statistical measures:

* Mean
* Median
* Standard Deviation
* Skewness
* Kurtosis
* Jarque-Bera Test

---

# Feature Engineering

## Technical Indicators

* Moving Averages
* Rolling Mean
* Rolling Volatility
* RSI
* MACD
* Bollinger Bands
* ATR
* Momentum
* Rate of Change

---

## Lag Features

* Previous Day Return
* 2-Day Lag
* 5-Day Lag
* 10-Day Lag

---

## Market Features

* S&P500 Return
* Market Volatility
* VIX
* Risk-Free Rate

---

## Calendar Features

* Month
* Quarter
* Day of Week

---

# Target Variable

The prediction target is

> **30-Day Future Realized Volatility**

Instead of predicting stock prices, the models estimate the future market risk over the next 30 trading days.

This aligns more closely with institutional portfolio management and risk management practices.

---

# Forecasting Models

## Baseline Models

* Historical Volatility
* EWMA
* GARCH(1,1)

---

## Machine Learning Models

* Random Forest Regressor
* XGBoost Regressor
* LightGBM *(Optional)*

---

# Hyperparameter Optimization

Time-series aware tuning using:

* TimeSeriesSplit
* Grid Search
* Random Search

to prevent look-ahead bias.

---

# Portfolio Construction

The predicted volatility is incorporated into several portfolio allocation strategies.

## Strategy 1

Equal Weight Portfolio

---

## Strategy 2

Markowitz Mean-Variance Optimization

---

## Strategy 3

Global Minimum Variance Portfolio

---

## Strategy 4

Risk Parity Portfolio

---

## Strategy 5

Machine Learning Assisted Portfolio Optimization *(Proposed Framework)*

---

# Rolling Backtesting

The project employs realistic rolling-window backtesting.

Portfolio weights are rebalanced monthly to simulate institutional investment practice.

This avoids hindsight bias and evaluates models under changing market conditions.

---

# Performance Evaluation

Forecasting Performance

* RMSE
* MAE
* MAPE
* R²
* Directional Accuracy

---

Portfolio Performance

* CAGR
* Annual Return
* Annual Volatility
* Sharpe Ratio
* Sortino Ratio
* Maximum Drawdown
* Calmar Ratio
* Portfolio Turnover
* Value at Risk (VaR)
* Conditional Value at Risk (CVaR)

---

# Statistical Validation

To determine whether observed improvements are statistically significant, the project performs:

* Bootstrap Confidence Intervals
* Diebold-Mariano Test
* Paired Statistical Tests
* White Reality Check *(Optional)*

This ensures conclusions are supported by statistical evidence rather than isolated performance improvements.

---

# Model Explainability

Tree-based models are interpreted using

* Feature Importance
* SHAP Values

to identify the variables that contribute most to future volatility prediction.

This improves transparency and aligns with modern financial model governance practices.

---

# Robustness Analysis

Models are evaluated across different market regimes including:

* COVID-19 Market Crash
* 2022 Bear Market
* Bull Market Periods

to assess stability under varying market conditions.

---

# Repository Structure

```
Portfolio-Optimization/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── external/
│
├── notebooks/
│
├── src/
│   ├── data_collection.py
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── eda.py
│   ├── target_generation.py
│   ├── train_models.py
│   ├── portfolio_optimization.py
│   ├── backtesting.py
│   ├── evaluation.py
│   ├── explainability.py
│   └── statistical_tests.py
│
├── models/
│
├── figures/
│
├── reports/
│
├── dashboard/
│
├── requirements.txt
│
└── README.md
```

---

# Technologies Used

### Programming

* Python

### Data Processing

* pandas
* NumPy

### Visualization

* Matplotlib
* Plotly

### Machine Learning

* scikit-learn
* XGBoost
* LightGBM

### Financial Econometrics

* arch

### Portfolio Optimization

* PyPortfolioOpt
* SciPy

### Explainability

* SHAP

### Statistical Testing

* SciPy
* statsmodels

---

# Key Contributions

* Built an end-to-end quantitative finance pipeline from raw market data to portfolio construction.
* Compared classical econometric volatility models with machine learning approaches.
* Integrated volatility forecasts into multiple portfolio optimization strategies.
* Performed realistic rolling-window backtesting with periodic portfolio rebalancing.
* Evaluated investment strategies using financial performance metrics and statistical significance testing.
* Applied explainable AI techniques to identify the primary drivers of future market volatility.

---

# Future Work

* Deep Learning (LSTM, Transformer)
* Multivariate GARCH Models
* Dynamic Covariance Forecasting
* Black-Litterman Portfolio Optimization
* Reinforcement Learning for Portfolio Allocation
* Regime Switching Models
* Bayesian Portfolio Optimization

---

# Disclaimer

This project is intended for educational and research purposes only and should not be considered financial or investment advice.
