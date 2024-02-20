## Abstract
This report delivers a detailed examination of Tesla, Inc. (TSLA) stock data through the lens of advanced time series analysis techniques, aiming to forecast the stock's future performance over a 6 to 12-month horizon. A stock is a share of ownership in a corporation, and an investment in TSLA stock represents a stake in Tesla's prospective achievements. The potential for capital gains and dividends comes with the inherent risk of price depreciation, reflecting the volatile nature of the stock market.

The core of this analysis is the application of various time series forecasting methods to TSLA's historical stock data. We begin with elementary models such as the Naïve method, which assumes the most recent stock price as the best predictor for future prices, and the Historical Average method, which forecasts future values based on the historical average of the stock. To gauge the precision of these methods, we employ accuracy metrics including Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and Mean Absolute Percentage Error (MAPE), which collectively offer a quantifiable measure of each method's forecasting reliability for TSLA stock.

Moving beyond foundational approaches, the study incorporates more sophisticated models such as ARIMA and SARIMA, which are designed to capture complex patterns in time series data. The ARIMA model addresses non-seasonal time series data, while SARIMA extends this approach to account for seasonal variations, which can be particularly pertinent for TSLA stock given its historical performance patterns.

The report meticulously evaluates the results of these models, providing an in-depth narrative on the nature of TSLA’s stock behavior and the effectiveness of different time series methodologies. Our aim is to provide a nuanced understanding of TSLA’s price trajectory, empowering investors with the knowledge to make well-informed decisions in a market that is as promising as it is unpredictable.


## Time Series Visualization  

### The time series visualization of Tesla, Inc. (TSLA) stock from January 2019 to 2023 comprises 60 observations, representing monthly closing prices. This visual analysis offers a comprehensive view of the stock’s performance.

Key Observations and Statistics:
•	The dataset consists of 60 observations, capturing TSLA’s stock price movements over approximately five years.
•	The average (mean) closing price of the stock is approximately $174.81.
•	A standard deviation of approximately $110.21 suggests significant variability in TSLA’s stock prices.
•	The lowest recorded stock price is around $12.34.
•	The highest price attained is approximately $381.59.
•	The median price, representing the middle value, is approximately $206.59.


<img width="452" alt="image" src="https://github.com/kireetigudla/kireeti01/assets/122108823/751c3ea2-3317-4cc1-a667-dcadd0006e2e">


<img width="452" alt="image" src="https://github.com/kireetigudla/kireeti01/assets/122108823/0f1d7911-1b1c-4ff8-aa47-293405ceb1bc">

##Time Series Decomposition 

###The time series decomposition of Tesla, Inc. (TSLA) stock data from January 2019 to 2023 provides an insightful breakdown into trend, seasonality, and residuals.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/932626d3-d0d4-42c7-baed-72fbc188b644)

Trend Component:

The trend component of TSLA stock showcases a long-term upward trajectory. It reflects a consistent increase in the stock's value over the analysed period, indicating a positive overall growth trend in Tesla’s market performance.

Seasonality Component:

Seasonality in TSLA stock is observed as a cyclical pattern, with notable fluctuations occurring at specific times of the year. A trend of stock price surges is seen during the summer months (June to August), suggesting higher market activities or favourable market conditions during this period. Conversely, there is a tendency for the stock prices to decline in the winter months (December to February), indicating a seasonal impact on the stock’s valuation.

Residuals Component:

Residuals represent the irregularities or random variations in TSLA’s stock price that are not accounted for by trend or seasonality. These fluctuations could be attributed to various factors, such as unexpected market events, company-specific news, or changes in investor sentiment. Residuals highlight the unpredictable elements affecting the stock price.

##Additive Decomposition Analysis:

###Additive decomposition is utilized to analyse and understand the time series by linearly combining the effects of seasonality, trend, and errors. The selection of additive decomposition is influenced by the residual values being closer to zero, indicating a more accurate representation of the stock data. The residual plots in additive decomposition are critical for evaluating the error metrics and serve as a crucial factor in choosing between different decomposition approaches.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/10d32f9a-2209-43a6-a275-88e9d028f105)

•	Trend Component: Shows a clear long-term upward trend in TSLA's stock price, reflecting consistent growth over time.
•	Seasonal Component: The additive seasonal component does not display a strong, consistent pattern. This suggests that the stock price does not have a significant fixed seasonal variation.
•	Residual Component: The residuals, representing unexplained variations, show fluctuations, indicating market volatility and external factors not captured by the trend and seasonality.

##Multiplicative Decomposition Analysis:

###Multiplicative decomposition, another method for dissecting the time series, involves multiplying the components of seasonality, trend, and error. However, due to the residual values in multiplicative decomposition being closer to one, this method is generally less preferred for TSLA stock data over the additive approach. This indicates that the linear combination of components in additive decomposition provides a more precise depiction of TSLA’s stock behaviour during the given period.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/542f6013-99fc-450b-b6ab-c46e9db000f5)

•	Trend Component: Like the additive model, there's a noticeable upward trend, indicating growth in the stock price over time.
•	Seasonal Component: The multiplicative seasonal component also does not show a distinct seasonal pattern, echoing the findings of the additive decomposition.
•	Residual Component: The residuals in the multiplicative model exhibit variations, suggesting influences on the stock price beyond the trend and seasonal components.
##Comparison and Insights
###
•	Choice of Model: The additive model is typically preferred when the seasonal variations are relatively constant over time, while the multiplicative model is more suitable when seasonal variations change proportionally to the level of the time series. For TSLA stock, the additive model may be more appropriate given the absence of clear proportional seasonality.
•	Seasonality: Both models suggest that TSLA stock does not exhibit strong, consistent seasonal patterns monthly.
•	Trend and Residuals: Both models highlight a significant upward trend and the presence of irregularities or noise in the stock price movement, likely due to market factors, investor sentiment, and other external influences.

##Naive Method

###The Naive Method for forecasting employs a straightforward approach, where the prediction for a future period is based solely on the observed value of the current period. It's a simple strategy that uses the most recent data as the basis for future forecasts, disregarding any underlying seasonality, trends, or intricate patterns in the dataset. In our analysis of the TSLA stock, the Naive Method forecasted a constant value, equivalent to the last observed closing price from the training set.

The forecast using the Naive Method maintained a constant value, mirroring the last observed closing price in the training data. This demonstrates stability in the forecast, despite variations in the actual closing prices.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/6dac8ed7-0498-4268-8370-29ce10897a87)

##Accuracy Metrics
To evaluate the Naive Method’s accuracy, we employed metrics such as RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), and MAPE (Mean Absolute Percentage Error), which are standard for assessing forecasting models:

•	RMSE (Root Mean Squared Error): 104.89. This metric, defined as the square root of the average squared differences between predicted and actual values, assesses the standard deviation of the prediction errors.
•	MAE (Mean Absolute Error): 99.47. This is calculated by averaging the absolute differences between predicted and actual values, indicating the average magnitude of the errors.
•	MAPE (Mean Absolute Percentage Error): Not calculated in our analysis, but typically represents the error as a percentage of the actual value.

##Average Historical method

###The Average Historical Method is a simple forecasting technique that predicts future values based on the average of past observations if this historical average will continue. It ignores seasonal patterns or trends, relying on a constant average over time. For the TSLA stock, the forecasted value using the Historical Average Method was the mean of the historical closing prices.

The forecast using the Historical Average Method produced a constant value, equal to the average of the historical closing prices in the dataset.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/b6247869-be13-463b-bfcf-6580675dedd3)

##Accuracy Metrics

###The accuracy of the Historical Average Method was assessed using the same metrics:

•	RMSE: 68.44. Compared to the Naive Method's RMSE of 104.89, the Historical Average Method shows a lower value, indicating smaller prediction errors on average.
•	MAE: 59.80. This value is lower than the Naive Method's MAE of 99.47, suggesting a closer average prediction to the actual values.
•	MAPE: Not calculated in our analysis, but it would provide a percentage-based comparison of the errors.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/2ebddb67-2dc7-46c6-9370-529d188c8fe8)

##Simple Average Method

###We utilized the Simple Average Method to forecast the TSLA stock's closing prices. This approach predicted a constant value, equal to the average of past observations, for the entire forecast period from 2023 to 2024. Our analysis revealed that this forecast, while simple, did not align well with the actual closing prices, as it maintained a constant value regardless of the stock's actual performance. We used 80% of the data for training and 20% for testing.
In applying the Moving Average forecasting method, the TSLA stock data was smoothed over a 12-month window to predict future values. The visualization portrays the forecast as a flat line projecting the average closing price into the future, which reflects the method's principle of averaging past values without considering potential trends or seasonal variations.


![image](https://github.com/kireetigudla/kireeti01/assets/122108823/4b9474ca-6938-4694-a29f-b20a89701b5c)

##Accuracy Metrics.

###The accuracy of the Simple Average Method was evaluated using RMSE and MAE. The RMSE was 68.44, and the MAE was 59.80. Although these metrics indicated a reasonable level of accuracy, the method's inability to adapt to changes in the stock's performance limits its effectiveness.

##Holt’s Linear Method

###Holt's Linear Trend method was used to estimate the TSLA stock's future values. This method attempted to account for the stock's trend but still resulted in a forecast that did not closely match the actual stock price movements. We maintained an 80/20 split for training and testing the data.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/b83722b3-8b35-4b81-b326-14da03d84587)

##Accuracy Metrics

###For Holt's Linear method, we calculated RMSE and MAE. The RMSE was 88.20, and the MAE was 83.22. Despite accounting for the trend, the method's inability to capture the stock's full complexity resulted in limited forecasting accuracy.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/713cc159-b000-41a5-8b8c-20f85b609672)


##Holt-Winters Method

###The Holt-Winters method, applied to the TSLA stock data, incorporates seasonal components. The forecast generated by this method was more dynamic but did not accurately predict the stock's actual movements. The same data split for training and testing was used.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/3271400d-a667-4ac9-9059-355398c8dd5e)

##Accuracy Metrics.

###The accuracy metrics for Holt-Winters included RMSE and MAE. The RMSE was 234.54, and the MAE was 221.50. The high values of these metrics suggest that the method, despite its complexity, was not well-suited to predict the TSLA stock's behaviour accurately.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/2f3be111-e9e8-487a-9160-1e9baa801330)

##Comparative Analysis

###After comparing the Simple Average, Single Exponential Smoothing, Holt's Linear, and Holt-Winters methods, we found that the Simple Average Method had the lowest RMSE and MAE, indicating better average accuracy. However, its simplistic approach does not capture the dynamic nature of the TSLA stock prices. In contrast, the more sophisticated Holt-Winters method, which accounted for seasonality and trend, showed higher error metrics, suggesting that its complexity did not translate to better predictions for this dataset. The Single Exponential Smoothing and Holt's Linear methods offered a balance between simplicity and complexity but still did not adequately capture the stock's fluctuations. Therefore, while the Simple Average Method showed the lowest errors, it's important to consider the limitations of each method in the context of the data's characteristics.



##Time Series Stationary test and Differencing 


To determine the stationarity of the TSLA stock time series, we applied the Dickey-Fuller test. The test yielded a p-value of at 0.500614, significantly above the 0.05 significance level, indicating that the series is not stationary. Therefore, we proceeded with differencing, finding that the time series achieves stationarity with one order of difference, setting the value of d or I at '1'.

The p-value, at 0.500614, exceeds the significance level of 0.05. This means that the null hypothesis, which assumes the time series is non-stationary, cannot be dismissed. Consequently, the time series requires differencing. The appropriate level of differencing is determined by examining the Auto Correlation Function (ACF) plot, specifically looking for the point where it approaches zero relatively quickly. A time series that exhibits positive autocorrelations for numerous lags may need additional differencing. On the other hand, if the autocorrelation at a single lag is excessively negative, this could indicate the series is over-differenced. To identify the correct order of differencing necessary to achieve stationarity in the time series, the autocorrelation function will be plotted and analysed.



![image](https://github.com/kireetigudla/kireeti01/assets/122108823/8fd08c94-827e-45ba-b1ca-e7c6413bd435)

##ACF and PACF

###The Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) plots were analysed. The ACF plot showed that the lag of 1 is well above the significance line, leading us to set the q or MA value at '1'. 

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/6d8c39d8-eed4-4668-b3ab-ed0e98341ae5)

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/b208aab4-8d57-4ade-a35c-1a701b7cb913)


##ARIMA

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/9764b5ff-5fb4-47fe-8d58-ccdfe4ea7917)

###Our fitting of the ARIMA model to the TSLA stock time series data revealed:
•	Standardized residuals were within the acceptable error range, suggesting the model fit the data well.
•	The Q-Q plot hinted at a largely normal distribution of residuals, despite some noticeable outliers.
•	The histogram of residuals indicated a slight bias towards positive outliers, signifying a rightward skew.
•	The correlogram displayed a quick decay in autocorrelation, implying minor residual correlations.

- AR and MA coefficients indicated a negative correlation for AR (ar. L1 approximately 0.9923) and a positive one for MA (ma. L1 approximately -0.97456).
- The residual errors were close to zero, but the variation increased over time, hinting at missing components.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/b0b8dcca-0dcb-4e34-ab78-55b4f0ac1d0d)

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/22b78bf9-feb1-4cf8-b1c7-b43db53c59fa)

###While the ARIMA (0,1,0) model appeared to provide a reasonable forecast, its lack of a seasonal component could be a potential shortfall for the TSLA dataset.

##Accuracy Metrics.

![image](https://github.com/kireetigudla/kireeti01/assets/122108823/f49374ec-0644-4775-b2dc-8bc18ca1033b)



![image](https://github.com/kireetigudla/kireeti01/assets/122108823/338b8ad2-c8cb-4f35-a0af-4117a2ebb8d5)











