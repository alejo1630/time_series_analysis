# Time_series_analysis

This Python notebook provides a comprehensive analysis of time series data using different machine learning models. 

## 🔰 What is it about?

The dataset used contains monthly milk production from January 1962 to December 1975. The analysis includes exploratory data analysis, feature engineering, and forecasting using **XGBoost**, **LSTM**, and **Darts** models. It also compares the performance of these models based on RMSE metric.

These are the main insights:

*Forecasting 12 months*

<img src = "https://raw.githubusercontent.com/alejo1630/time_series_analysis/main/Images/Prediction.png" width = "1000">

All three models capture the overall trend accurately, including the rise in production from January to May and the decline thereafter. XGBoost provides smoother predictions with less variance, often underestimating troughs and overestimating peaks. LSTM captures the seasonal pattern more closely but with slight lag, while Darts, although following the trend well, tends to overestimate both peaks and troughs. Overall, XGBoost offers stable predictions, LSTM balances trend and variance well, and Darts is highly sensitive to changes, making each model suitable for different forecasting needs.

*Forecasting performance based on RMSE for more months (12-74)*

<img src = "https://raw.githubusercontent.com/alejo1630/time_series_analysis/main/Images/RMSE.png" width = "1000">

Darts consistently shows the lowest and most stable RMSE across all horizons, indicating robust performance irrespective of the prediction length. XGBoost starts with low RMSE for shorter horizons but its error increases significantly beyond 36 months, reflecting a decrease in accuracy for long-term predictions. LSTM, on the other hand, shows a steady increase in RMSE with the prediction horizon, indicating that its accuracy degrades more gradually over time compared to XGBoost. This suggests that while Darts excels in consistent performance, XGBoost is better suited for short-term predictions, and LSTM offers a balanced approach but is less effective for long-term forecasting.

