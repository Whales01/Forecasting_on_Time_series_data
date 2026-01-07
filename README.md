# Goldman Sachs Time Series Forecasting - Financial Market Analysis
# Overview

This project implements a high-performance time series forecasting pipeline designed to model the price dynamics of Goldman Sachs (GS). The primary objective is to move beyond "black-box" predictions by identifying models that are both statistically predictive and economically meaningful.
A core focus of this research is assessing the sensitivity of equity prices to macroeconomic shifts, specifically the impact of benchmark interest rates. Research indicates that a 100-basis-point change in real Treasury yields is typically associated with a 7% change in forward P/E multiples, making interest rate exogenous variables critical for robust financial modeling.

The work was developed as part of a time series assessment and emphasizes model diagnostics, interpretability, and forecast performance.

# Model Methods & Evaluation
The pipeline compares classical econometric frameworks with modern additive models to identify the optimal balance between interpretability and forecast accuracy.

Statistical Foundation (ARIMA): Utilized as a baseline to capture linear dependencies and ensure stationarity through iterative differencing.

Seasonal Dynamics (SARIMAX): Implemented to account for cyclicality and, crucially, to integrate interest rates as exogenous regressors. SARIMAX is particularly effective in trend-consistent environments when external economic signals are present.

Additive Modeling (Meta Prophet): Employed to decompose the time series into non-linear trends, holidays, and multi-period seasonality. This model is ideal for capturing "irregular" patterns and shifts in business cycles.

Time Series Decomposition: Used to isolate the underlying trend from seasonal noise and residuals, providing a "clean" view of the long-term price trajectory.

# 📊 Evaluation & Performance Metrics
Models are evaluated using a multi-metric framework to ensure they generalize well to unseen market conditions:

Mean Absolute Error (MAE): Used to measure the average magnitude of errors in the same units as the stock price.

Mean Squared Error (MSE): Adopted to penalize larger outliers, which is essential given the high-volatility nature of financial markets.

Economic Significance: Beyond metrics, models are evaluated on their ability to reflect real-world drivers, such as the correlation between 10-year Treasury yields and asset returns.

# Visual Insights
The notebook generates comprehensive visualizations to aid in decision-making:

Time Series Forecast Plots: Interactive overlays of predicted vs. actual prices to visualize "look-ahead" performance.

Prophet Component Analysis: Visual breakdown of daily, weekly, and yearly seasonality. This identifies specific periods where Goldman Sachs' stock historically exhibits recurring strength or weakness.

Trend Saturation: Highlighting "changepoints" where the underlying price momentum shifted due to macro-shocks.
The code eventually visualise the result of timeseries plots and the seasonality components of the prophet trend.
