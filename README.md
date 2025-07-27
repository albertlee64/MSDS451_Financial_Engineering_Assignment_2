# MSDS451 Financial Engineering Assignment 2: Portfolio Optimization using Monte Carlo Methods

With change in federal procurement strategies and the emerging trend of "defense tech' companies, I wanted to focus this assignment on 3 companies within the Federal Government Contracting Landscape. Booz Allen Hamilton is a $12B+ professional services federal contractor that has had recent contract cancellation and has had their company reviewed by GSA. Northrop Grumman is a defense manufacturer that recently gained a huge publicity due to it’s B2 stealth bomber. The last company is Palantir whose stock has doubled since the beginning of the year but also has recently gained momentum in leading the federal contracting space in a new category as “defense tech”.

This project explores portfolio optimization using three publicly traded assets (BAH, NOC, PLNTR), simulating long-only and long-short strategies under uncertainty. The model leverages Monte Carlo methods to simulate thousands of portfolios, calculates optimal weights, and compares performance against the S&P 500.

# Data Input

Historical price data from yfinance for BAH, NOC, PLNTR
Risk-free rate assumed at 3%
Max Leverage of 2.0

Asset Summary Statistics:

        Mean Daily Return  Annualized Return  Annualized Volatility
Ticker                                                             
BAH                0.0004             0.1034                 0.2841
NOC                0.0006             0.1419                 0.2451
PLTR               0.0032             0.8145                 0.7298

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

Optimal Portfolio Weights:
Ticker  Long-Only (Max Sharpe)  Long-Only (Min Risk)  Long-Short (Max Sharpe)  Long-Short (Min Risk)
   BAH                  0.0070                0.3506                  -0.0546                 0.3868
   NOC                  0.5107                0.5899                   0.6013                 0.5561
  PLTR                  0.4823                0.0595                   0.4533                 0.0572

# Backtesting

Max Sharpe portfolio applied to historical returns
Compared cumulative performance against the S&P 500

<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/464d544c-6278-4bc3-b6a7-daf86b5bf47d" />

# License

MIT License

