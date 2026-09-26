# Monte Carlo Portfolio Risk & Asset Allocation Model

An interactive Python-based Monte Carlo framework for analysing multi-asset portfolio risk, strategic asset allocation and downside outcomes.

## Overview

This project uses Monte Carlo simulation to analyse potential portfolio outcomes across a diversified set of asset classes.

Historical market data is used to estimate asset returns and covariance relationships. Cholesky decomposition is then applied to generate correlated return scenarios, allowing the simulation to preserve estimated cross-asset relationships.

The framework is designed for portfolio risk and scenario analysis rather than predicting future market returns.

## Asset Universe

The model uses five liquid ETFs representing different asset classes and geographic exposures:

- **SPY** – S&P 500 / US large-cap equities
- **QQQ** – Nasdaq-100 / US technology and growth equities
- **IEUR** – European equities
- **TLT** – Long-duration US Treasury bonds
- **GLD** – Gold

## Key Features

- Interactive portfolio construction
- Up to 50,000 Monte Carlo simulations
- Adjustable investment horizons
- Correlated multi-asset return simulation
- Cholesky decomposition
- Growth, Balanced and Defensive portfolio strategies
- Custom asset allocation
- Normal and stressed market scenarios
- Annualised volatility
- Sharpe ratio
- Probability of loss
- 95% Value at Risk (VaR)
- 95% Expected Shortfall
- Portfolio outcome distributions
- Simulated portfolio paths
- Risk-return comparison
- Cross-asset correlation analysis

## Portfolio Strategies

The model compares three strategic asset allocations:

| Asset | Growth | Balanced | Defensive |
|---|---:|---:|---:|
| SPY | 40% | 30% | 20% |
| QQQ | 30% | 15% | 5% |
| IEUR | 15% | 20% | 15% |
| TLT | 5% | 20% | 40% |
| GLD | 10% | 15% | 20% |

All portfolios are evaluated using the same simulated market scenarios, allowing differences in outcomes to be driven by asset allocation rather than different random draws.

## Methodology

Historical daily log returns are used to estimate the mean return vector and covariance matrix.

Cholesky decomposition transforms independently generated random shocks into correlated shocks based on the estimated covariance structure.

The resulting simulated portfolio outcomes are evaluated using return, volatility and downside-risk measures including VaR and Expected Shortfall.

A hypothetical stressed scenario increases volatility and reduces expected returns to examine portfolio sensitivity under less favourable market conditions.

## Model Limitations

This framework is intended for portfolio risk and scenario analysis rather than market forecasting.

Important limitations include:

- Historical returns and covariance may not represent future market conditions.
- Historical mean returns are noisy estimates of forward-looking expected returns.
- Asset correlations can change significantly during periods of market stress.
- Simulated returns do not fully capture fat tails, volatility clustering or extreme market discontinuities.
- Portfolio rebalancing, transaction costs and taxes are simplified or excluded.
- The stressed scenario represents a hypothetical sensitivity analysis rather than a forecast of a specific market crisis.

## Technologies

- Python
- NumPy
- pandas
- Matplotlib
- yfinance
- ipywidgets

## Running the Model

Open `Monte_Carlo_Portfolio_Risk_Model.ipynb` in Google Colab or Jupyter Notebook and run all cells from top to bottom.

The interactive dashboard can then be used to modify portfolio allocation, investment horizon, number of simulations and market scenario.
