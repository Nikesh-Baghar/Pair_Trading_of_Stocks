#  Portfolio Optimization Using Pair Trading of Stocks

## 1) All the **stock prices** are taken from automotive sector of NSE, India.
   
   **The training data** consist of closing price of stocks from Yahoo Finance for the period 1st July 2021 to 30th June 2024.

   The **evaluation**is done based on the annual returns of the stocks on the test data from 1st July 2024 to 30th June 2025.

## 2) **Correlation coefficients** are computed based on the return values of the close prices.

## 3) To identify the pairs which are **cointegrated**, the coint function defined in the stattools submodule under the statsmodels module of Python is      used.

   The cointegrated pair of **M&M.NS and ASHOKLEY.NS** is used.

## 4) An **ordinary least square (OLS)** regression model is built to get hedge ratio and and the p-value of its t-statistics.

## 5) A dataframe is created which includes **signals for buying and selling** of stocks based on z-score.

## 6) The pair trading portfolio is initiated on 1st July 2024, with an **initial capital of 100000 units** for each asset (i.e., with a total investment    of 200000 units).

   At the end of 30 June 2025 the excess (or deficit) of the total portfolio value over the total initial investment of 200000 units is computed to       arrive at the **profit (or loss).**

   Based on the computed profit (or loss), the **return of the portfolio** is derived. 
