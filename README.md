# MSDS451 Financial Engineering Assignment 2: Portfolio Optimization using Monte Carlo Methods

With change in federal procurement strategies and the emerging trend of "defense tech' companies, I wanted to focus this assignment on 3 companies within the Federal Government Contracting Landscape. Booz Allen Hamilton is a $12B+ professional services federal contractor that has had recent contract cancellation and has had their company reviewed by GSA. Northrop Grumman is a defense manufacturer that recently gained a huge publicity due to it’s B2 stealth bomber. The last company is Palantir whose stock has doubled since the beginning of the year but also has recently gained momentum in leading the federal contracting space in a new category as “defense tech”.

This project explores portfolio optimization using three publicly traded assets (BAH, NOC, PLNTR), simulating long-only and long-short strategies under uncertainty. The model leverages Monte Carlo methods to simulate thousands of portfolios, calculates optimal weights, and compares performance against the S&P 500.

# Data Input

Historical price data from yfinance for BAH, NOC, PLNTR
Risk-free rate assumed at 3%
Max Leverage of 2.0


<img width="790" height="490" alt="image" src="https://github.com/user-attachments/assets/f29fe503-fa33-4f2d-b5c3-cfe720158d0a" />


# Portfolio Simulation

1,000+ portfolios generated using random weights
Long-only constraint: weights ≥ 0 and sum to 1
Long-short constraint: ≤ 2.0 (bounded leverage)

# Optimization

Portfolio return (μ) and volatility (σ) calculated for each
Sharpe Ratio = (μ − r_f) / σ
Max Sharpe and Min Risk portfolios identified

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/e048571f-3fcc-412a-9ec9-f3b62504ca1c" />

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/8261f195-36b6-4e7d-84a6-bce7b1af2891" />


# Stochastic Programming

Simulated future return scenarios from multivariate normal
Used to approximate optimal portfolio weights under uncertainty

<img width="468" height="87" alt="image" src="https://github.com/user-attachments/assets/342f3237-94f2-4aef-a204-a9d5ce8807f8" />

# Backtesting

Max Sharpe portfolio applied to historical returns
Compared cumulative performance against the S&P 500

<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/464d544c-6278-4bc3-b6a7-daf86b5bf47d" />

# AI Usage

AI was used to help develop some of the code around the Monte Carlo optimization portfolio model. AI was also used to help with the Stochastic Programming approximation as I was not familiar with it. Lastly, AI was used to help with the back testing to ensure the cumulative returns were being calculated properly.

# License

MIT License

