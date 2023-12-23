# Consumer-Price-Indices-Prediction Model
Training a Time Series ARIMA model to predict Consumer Price Indices using official Kenyan CPI data

Consumer Price Index (CPI) is a measure of weighted aggregate change in retail prices paid by costomers of a given basket of goods and services.

## Uses of Consumer Price Index
- Measure Inflation
- An indicator of Macroeconomic Performance
- Measure Purchasing Power
- Tool in Wage negotiation
- Determinant of supplier price variation

## Benefits of Predicting Consumer Price Indices:
- Controlling inflation
- Accounting and Financial Planning
- Understanding future purchasing power of a Nation's currency
  
## Python libraries used
- Pandas for data manipulation and analysis
- Seaborn andMatplotlib's pyplot for data visualization
- Statsmodels for Time series decomposition and to build ARIMA model
- sklearn to test model accuracy using mean squared error of actual vs predicted indices

## About the Data
The data is from the [Kenya National Bureau of Statistics online Data Tables](https://www.knbs.or.ke/download/employment-earnings-and-consumer-price-indices-2/)
It is a table with monthly Consumer Price Indices from 2018 to 2022 and Annual Averages.

## Steps Taken
1. Importing libraries and loading the data.
2. Understanding the data.
3. Data Cleaning - format, nulls, outliers & data types
4. Time series decomposition and Visualizations - Seasonality, Trend, Noise, Stationarity, Autocorrelation.
5. Modelling - Training, Validating and Improving the prediction model.

## MODEL USED - ARIMA(AutoRegressive Integrated Moving Average)
### Why ARIMA?
- ARIMA’s Autoregressive (AR) component will help remove the trend and seasonality from the data, capturing a linear relationship.
- The time series data is non-stationary, meaning it exhibits trends or seasonality. Differencing from ARIMA’s Integrated (I) component makes it stationary.
-	Autocorrelation was observed in the data, and it requires differencing from ARIMA’s Integrated (I) component to make it stationary.
-	ARIMA’s Moving Average (MA) component captures dependencies between current observations and past forecast errors.

## SUMMARY FINDINGS;
- There's a general increase in consumer price indices over the years.
- The years 2018 and 2020 have a few outliers in the indices.
- For all the 5 years, data in January started at a low index and kept rising as time went by.
- The data follows a consistent upwards or downward slope. - It has trend.
- The data displays a clear periodic pattern which is an increase over time. - It has seasonality.
- The data is not Stationary.

# CONCLUSION
The prediction model isn't 100% accurate.
It has a Mean Squared Error of 0.2132.

The model may be improved by:
1. Using **more historical data** from previous years.
2. **Adding other variables** that may affect Consumer Price Index.
Like Consumer Spending Habits, Money Supply, forex exchange rates.
3. **Considering market conditions** like political instability, war, rapid technological change, financial crisis.
