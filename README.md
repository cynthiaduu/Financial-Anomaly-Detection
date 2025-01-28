# Financial Anomaly Detection

Project overview: stock price anomaly detection and forecasting

Specifically, I followed 3 stocks: NVIDIA, Apple, and Microsoft across July 2024 to the end of September 2024. To do this, I first dove into what points fall into the traditional, statistical definition of an outlier. However, I had to consider if the points were actually outliers or just a reflection of changing market behavior.

To dive deeper into this, I analyzed stock volatility using a Hidden Markov Model. A Hidden Markov Model is great to identify market regimes + trends, and characterizes periods into 3 states. State 0 indicates low volatility and stable returns, State 1 indicates higher volatility and higher returns, while State 2 indicates high volatility and bearish activity / negative returns. 

Next, I conducted STL Decomposition and ARIMA forecasting. STL decomposition decomposes the time series into trend, seasonal, and residual components. ARIMA forecasting is used for time series forecasting, and uses past observations and making the time series stationary to do so.

After performing STL decomposition, I extracted the trend component of the stock price and applied ARIMA to forecast the stock prices for October based on historical patterns. Then I combined the forecasted trend with the seasonal component from STL to account for yearly market trends to predict overall stock price 

The forecast could be improved by incorporating external factors such as macroeconomic indicators, news sentiment, or industry-specific events, which are not captured by the current model. Additionally, experimenting with advanced machine learning models like LSTMs or hybrid approaches that combine ARIMA with deep learning could enhance the accuracy of predictions and anomaly detection.
