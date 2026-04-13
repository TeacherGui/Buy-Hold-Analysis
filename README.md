# Buy-Hold-Analysis
Analysis of a variable income asset portfolio aiming to scrutinize the profitability, risk, and diversification of the assets.

**Objectives**
1. Profitability Analysis: What is the profitability of the assets/portfolio compared to the Ibovespa, taking dividends into account?
2. Historical Risk Analysis (Drawdown): How much did the assets devalue in the past and how long did they take to recover?
3. Diversification Analysis: Is there a correlation between asset prices? Which one?

**Methodology**
Collection → Processing → Analysis → Visualization

1. Collection: Portfolio data input via importation and editing of a simple spreadsheet with "Ticker", "Quantity", and "Average Price" columns; use of the Pandas library to load this data into the code's memory; automated enrichment via the yfinance API for the extraction of historical time series of adjusted prices (Adj Close) over a five to ten-year window; ensuring the database already incorporates dividends, interest on equity, and corporate events for the calculation of real profitability.

3. Processing: Time-series alignment to synchronize assets and benchmarks, handling holidays and non-trading days; calculation of the daily equity value by multiplying the adjusted price of each asset by its respective quantity in custody; application of base-100 normalization on the total equity curve and on the benchmarks (Ibovespa, IPCA and SELIC) to allow for visual comparison of percentage growth from a common starting point; conversion of prices into daily percentage changes, or log-returns, to serve as input for statistical risk and correlation calculations.

4. Analysis: Comparison of the portfolio's accumulated profitability against reference indices to measure real gain and excess return (Alpha); calculation of Maximum Drawdown to identify the largest historical percentage decline and the recovery time for each asset and the consolidated portfolio; application of the Pearson correlation coefficient on returns to validate if the diversification among assets is statistically effective or if they exhibit high linear dependence on each other.
 
5. Visualization: Consolidation of results into visual artifacts such as line charts for accumulated performance and heatmaps for the correlation matrix; structuring of statistical summary tables that transform processed data into visual support for long-term strategic investment decision-making.
