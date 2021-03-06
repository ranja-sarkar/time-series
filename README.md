# time-series

***Is your time series a random walk?***

It may be a random walk (stochastic process), and some ways to check are as follows: 
•	The time series shows a strong temporal dependence (autocorrelation) that decays linearly or in a similar pattern. 
•	The time series is non-stationary and making it stationary shows no obviously learnable structure in the data.  
•	Using an observation at the previous time step to learn what will happen in the next time step (persistence model) provides the best source of reliable predictions.

Baseline forecasts with the persistence model quickly indicate whether you can do significantly better. If you can’t, you’re probably dealing with a random walk (or close to it). 
The human mind is hardwired to look for patterns everywhere and we must be vigilant we are not fooling ourselves and wasting time by developing elaborate models for random walk processes.


***Approaches to smoothing a time series*** 

Forecast of (level + trend) is a baseline forecast. Example is Holt's method where there are level smoothing constant (alpha) and trend constant (beta). Seasonal smoothing (Holt Winter's method) considers a seasonal baseline which is a regularly recurring pattern (day, week, month, quarter etc.) and baseline rises and falls at regular intervals. Deviation of each season from the baseline’s long-term (annual) average is used for forecasts (seasonal smoothing constant is delta). 
On the other hand, Exponential Smoothing defines trend as the difference between observed values in consecutive records. 

***ARIMA***

ARIMA handles data with trend, SARIMA data with a seasonal component. The trend, seasonality and noise in a time series are explained by model parameter set (p,d,q), also called the order. The auto-regressive parameter is p; d is difference parameter and q is the moving average parameter. Trend is the long-term change in the mean level of observations. Seasonality is the pattern that’s periodically repeated, and noise is the random variation in the data. A time series is additive when the 'trend' is linear (changes are at linear rate) and 'seasonality' is constant in time. 

Y(t) = Level + Trend + Seasonality + Noise

A stationary time series does not exhibit a trend. 


