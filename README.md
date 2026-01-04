# Crypto Volatility Risk Analysis (Python, Pandas)
## Overview

This project analyzes downside risk in major cryptocurrencies using historical price data and time-series risk metrics.
The focus is risk quantification and capital allocation guidance, not price prediction or trading strategies.

The analysis demonstrates how volatility, drawdowns, and loss probabilities can be used to make explainable, decision-oriented risk assessments.

## Objective

To evaluate and compare downside risk across cryptocurrencies by answering:

How unstable are prices over time?

How severe are historical losses from peak levels?

How frequently do large losses occur?

What level of capital exposure is appropriate given the risk profile?

## Assets Analyzed

Bitcoin (BTC) – High volatility, moderate downside risk

Ethereum (ETH) – Very high volatility and severe drawdowns

Tether (USDT) – Stable asset used as a risk baseline

## Data Source

CoinGecko Public API

Daily price data (last 365 days, API free-tier constraint)

## Methodology

### 1. Data Preparation

Retrieved daily closing prices via API

Aligned assets on a common date index

Converted prices into daily and weekly returns

### 2. Volatility Analysis

Computed 7-day and 30-day rolling volatility

Captured time-varying instability rather than static averages

### 3. Drawdown Analysis

Calculated cumulative returns

Measured drawdowns from historical peaks

Identified maximum drawdown per asset

### 4. Loss Probability Estimation

Weekly probability of losses greater than 10%

Monthly probability of losses greater than 20%

Focused on frequency of severe downside events

### 5. Risk Classification & Guidance

Assigned explainable, rule-based risk levels

Translated risk metrics into capital allocation guidance

<img width="1058" height="525" alt="image" src="https://github.com/user-attachments/assets/cd083a86-c461-4dd0-acc6-1b0c92b453ce" />

<img width="1072" height="530" alt="image" src="https://github.com/user-attachments/assets/8d4fb31f-5b4b-4ebb-9e8f-bb10a1fa40b8" />


## Key Insights

Ethereum exhibits the highest risk, with deep drawdowns (~60%) and frequent large losses.

Bitcoin shows significant but lower downside risk compared to Ethereum.

Tether remains effectively risk-free, serving as a capital preservation baseline.

Volatility alone understates risk; drawdowns and loss probabilities provide clearer decision signals.

## Final Risk Summary

| Asset    | Max Drawdown | Weekly Loss Prob (>10%) | Monthly Loss Prob (>20%) | Risk Level | Allocation Guidance            |
| -------- | ------------ | ----------------------- | ------------------------ | ---------- | ------------------------------ |
| Bitcoin  | ~32%         | ~3.8%                   | 0%                       | High       | Moderate exposure with limits  |
| Ethereum | ~60%         | ~17%                    | 25%                      | Very High  | Limit exposure; high-risk only |
| Tether   | ~0%          | 0%                      | 0%                       | Low        | Capital preservation           |


## Tools & Technologies

Python

Pandas

NumPy

Matplotlib

REST API integration (CoinGecko)

## Project Scope & Limitations

No price forecasting or trading strategies

No machine learning models (emphasis on explainability)

Analysis limited to one year due to public API constraints

Results are descriptive, not predictive

## Why This Project

This project demonstrates:

Practical time-series analysis using pandas

Risk-focused thinking rather than speculative modeling

Clear translation of data into business and investment decisions

Explainable logic suitable for real-world analytics and risk roles

## Repository Structure

crypto-volatility-risk-analysis/
│
├── crypto-volatility-risk-analysis.ipynb

├── README.md

├── rolling_volatility.png

|──drawdown.png

## Author
Pratibha Mehta
