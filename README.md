# Electricity Price Volatility Analysis: IEX Power Market (DAM vs RTM)
Used regression analysis to real Indian power market data to derive an interesting pricing pattern — demand for DAM is inelastic to price while demand for RTM is elastic to price.

## Overview
This project analyzes daily trading data from the Indian Energy Exchange (IEX) to study how traded electricity volume responds to price in the Day-Ahead Market (DAM) and Real-Time Market (RTM). The dataset covers daily observations from January 2024 to September 2025 (623 days).

## Data
The dataset includes, for each day:
- Date
- Traded volume (DAM & RTM)
- Average, minimum, and maximum clearing price (DAM & RTM)

## Methodology
1. Cleaned and parsed date fields
2. Visualized price and volume trends over time for both DAM and RTM
3. Plotted volume vs. price scatterplots for each market
4. Ran OLS regression (Volume ~ Price) separately for DAM and RTM to estimate how sensitive traded volume is to price changes in each market

## Key Findings
- **DAM:** No significant relationship between price and volume (R² = 0.001, p = 0.405). Volume in the day-ahead market does not respond meaningfully to price.
- **RTM:** Significant relationship (R² = 0.261, p < 0.001, β = 12.14). Real-time market volume is meaningfully sensitive to price.

## Interpretation
DAM volumes are likely driven by pre-scheduled generation and demand commitments made a day in advance, making them relatively inelastic to price. RTM, on the other hand, captures more responsive, near-real-time trading behavior, where participants adjust volume based on current price signals, explaining the stronger price sensitivity observed.

## Tools Used
Python, pandas, numpy, matplotlib, seaborn, statsmodels (OLS regression)
