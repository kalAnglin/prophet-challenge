# Prophet-Challenge

## Overview
- To fulfill the responsibility as a growth analyst at Mercado Libre of analyzing the company's financials and search trends to determine if there is a way to predict how to make the company grow.

## Purpose
- To determine the accurary of a Prophet Time Series Model in terms of predicing future growth for Mercado Libre company by comparing the predictions to data exploration centered around finding patterns in the hourly google search traffic, determining whether there is correlation between the search traffic and seasonaliity, and relating the search traffic to stock price patterns.
  
## Business Advantage [^1]
- Time series models offer several advantages related to determining patterns and forecasting future trends. Because businesses rely on repetitive behavior as the basis for revenue, time series models can assist with predicting how future trends may develop ensure good financial health, explore new markets, and restock inventory.
  
## Landscape
- Time series models play a role in different sectors of business and innovation, including Healthcare, Agriculture, Finance, Cybersecurity, and Retail.

## Results
- By calculating the total search traffic for the month, and comparing it with the value to the monthly median across all months, it became evident the Google search traffic increase during the month of May, the month MercadoLibre released its financial results.
- By tracking the patterns of interest in the company and it's platform based on hours, days, and weeks, it became evident the search trends start to increase around 9am, with Monday & Tuesday being the days with the most traffic, and an increase in trends right before the certain weeks throughtout the year which correspond with holiday seasons.
- BBy concating the stock and trends dataframe, slicing the dataframe to just the first of 2020, it was confirmed that new customers and revenue increased for the e-commerce platform after the intial shock to the global financial markets during March of 2020. Also the spike in search trends and stock price at the beginning of May does indicate that people increased their search activity in anticpation of the release of quarterly financial results.
- By creating a new column to represent "Lagged Search Trends", a better representation was provided of how the search trends correlate to the stock closing price given changes to search trends affect the following week's stock prices
- By calculating the standard deviation of the closing stock price over a 4 period rolling windows (equating to 4 hours) it was deduced that the higher volalitiliy in the first half of 2020 was common given the tendency for high volatility days to be followed more high volatility days.
- In regards to predictability, the creation of a correlation matrix made it evident that there is slight correlation between search trends and stock volatility. This correlation is negative, meaning as search trends increases, stock volatility will decreases. The matrix also showed a very small, positive correlation betweeen search trends and hour stock return, meaning as increases in search trends resulted in small increases in houly returns, however given how close the correlation is to 0, a definitive prediction cannot be confirmed.
- The creation of a time series model to forecast near-term popularity of MercadoLibe based on hours proved difficult. The model was better at forecasting data based on days, providing a forecast trend  that showed a dip in search traffic through the 80 day (2000hrs) prediction period. Plotting the components of the forecast confirmed that on Tuesdays from 10am - 1pm and 10pm - 12am, MercadoLibre is the most popular per the search trends. The plot of the components also showed Mid-October as the lowest point for search traffic in the calendar, which corresponds with the celebration Hispanic Heritage Month from September 15 <sup>th</sup> to October 15 <sup>th</sup>.

** Recommendations
 Explore a time series forecast during the part of the year that doesn't coincide with the Hispanice Heritage month to determine if the trends can be explained without the presence of a seasonal holiday.

 [^1]: https://builtin.com/data-science/time-series-model
