# TimeSeries_Analysis

# Context

Gold, the yellow shiny metal, has been the fancy of mankind since ages. From making jewelry to being used
as an investment, gold covers a huge spectrum of use cases. Gold, like other metals, is also traded on the
commodities indexes across the world. For better understanding time series in a real-world scenario, we will
work with gold prices collected historically and predict its future value.

# Content

Metals such as gold have been traded for years across the world. Prices of gold are determined and used
for trading the metal on commodity exchanges on a daily basis using a variety of factors. Using this daily
price-level information only, our task is to predict future price of gold

# Data

For the purpose of implementing time series forecasting technique , i will utilize gold pricing from
Quandl. Quandl is a platform for financial, economic, and alternative datasets.
To access publicly shared datasets on Quandl, we can use the pandas-datareader library as well
as quandl (library from Quandl itself). The following snippet shows a quick one-liner to get your hands on gold pricing
information since 1970s.

import quandl
golddf = quandl.get("BUNDESBANK/BBK01WT5511")

The time series is univariate with date and time feature

# ARIMA MODEL 

The ARIMA model (an acronym for Auto-Regressive Integrated Moving Average), essentially creates a linear equation which describes and forecasts your time series data. This equation is generated through three separate parts which can be described as:

AR — auto-regression: equation terms created based on past data points
I — integration or differencing: accounting for overall “trend” in the data
MA — moving average: equation terms of error or noise based on past data points
