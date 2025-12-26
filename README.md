# Kalman-SP500

# Financial Econometrics II – Trend Following Project

**Course:** Financial Econometrics II – Master 203  
**Instructor:** G. Monarcha  
**Group Assignment**  

---

## Project Overview

This project implements a **trend-following strategy** on the S&P500 index using a **Kalman filter** to estimate the latent trend and slope of the index.  
The main goals are:

1. Compute the spread between the observed S&P500 log-prices and its trend.
2. Identify abnormal deviations from the trend.
3. Test macroeconomic factors as potential explanatory variables of the spread.
4. Build a trading strategy based on slope signals, expected slope, and spread thresholds.
5. Evaluate the performance and Sharpe ratio of the strategy.

---

## Data

- **File:** `GROUP DATASET.xlsx`  
- **Contents:**
  - Daily S&P500 total return prices
  - Daily macroeconomic factors  

---

## Core Model

The latent trend model is defined as:

\[
\begin{cases}
P_t = T_t + \epsilon_t \\
T_t = T_{t-1} + S_{t-1} + u_t \\
S_t = S_{t-1} + v_t
\end{cases}
\]

- \(P_t\): observed S&P500 level at time \(t\)  
- \(T_t\): latent trend estimated by Kalman filter  
- \(S_t\): stochastic slope of the trend  
- \(\Delta_t = \ln(P_t) - T_t\): spread between log-price and trend  

---

## Project Structure

