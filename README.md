## Soybean Price Forecasting Using ARIMA

In this project, I forecast the price of Soybeans using the ARIMA (AutoRegressive Integrated Moving Average) model.

The dataset was imported via API from the [FRED (Federal Reserve Economic Data)](https://fred.stlouisfed.org/) website.

### Exploratory Data Analysis (EDA)
I began with exploratory data analysis by plotting a line graph to visualize soybean price trends from **1990 to April 2025**.

### Stationarity Testing
Stationarity is a fundamental assumption of the ARIMA model. To assess this, I:
- Plotted the **rolling mean and standard deviation**
- Performed the **Augmented Dickey-Fuller (ADF) test**

The results indicated that the original series was **not stationary**.

### Differencing and Log Transformation
To achieve stationarity, I applied:
- **Log transformation** to stabilize the variance
- **First-order differencing** to remove trend and seasonality

### Model Order Selection (p, d, q)
To determine the ARIMA model parameters, I plotted:
- **ACF (Autocorrelation Function)**: helps identify the **MA (q)** component
- **PACF (Partial Autocorrelation Function)**: helps identify the **AR (p)** component

These plots help narrow down the parameter space, although they don’t guarantee optimal values. The ACF shows how each lag is correlated with the current value, while PACF shows the correlation of lags after removing the influence of shorter lags.

---

