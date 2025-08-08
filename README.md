#  Portfolio Optimization Using Pair Trading of Stocks

The work proposes a cointegration-based pair trading approach for stock portfolio design that can be used to earn profit by the investors in the stock market. The
innovative trading strategy provides the investors with reliable signals for triggering the short, long, or no action needed for carrying out transactions in the portfolio
for one year from during the portfolio test period. The pair-trading models are trained and evaluated on real-world stock market data and the results are presented to
demonstrate the effectiveness of the model.



### 1) All the **stock prices** are taken from automotive sector of NSE, India.
   
   **The training data** consist of closing price of stocks from Yahoo Finance for the period 1st July 2021 to 30th June 2024.

   The **evaluation**is done based on the annual returns of the stocks on the test data from 1st July 2024 to 30th June 2025.



### 2) **Correlation coefficients** are computed based on the return values of the close prices.

<img width="3200" height="2000" alt="Assets Return Correlation Matrix" src="https://github.com/user-attachments/assets/e0b73f0b-d999-46be-84a2-07acc05a44af" />



### 3) To identify the pairs which are **cointegrated**, the coint function defined in the stattools submodule under the statsmodels module of Python is used.

   The cointegrated pair of **M&M.NS and ASHOKLEY.NS** is used.

   <img width="4000" height="2800" alt="Assets Cointegration Matrix p-values Between Pairs" src="https://github.com/user-attachments/assets/d0ab8e58-8dc9-4d77-a833-078c3a8e05fb" />

   <img width="5200" height="2400" alt="Close prices" src="https://github.com/user-attachments/assets/5649bafd-fc2e-457c-8d75-8d1463f8235f" />



### 4) An **ordinary least square (OLS)** regression model is built to get hedge ratio and and the p-value of its t-statistics.
      The hedge ratio comes out to be 0.0549

   <img width="1430" height="656" alt="OLS_Regression" src="https://github.com/user-attachments/assets/6599796d-e2c3-4e0e-a31d-7fdd6c57a892" />

   <img width="5200" height="2400" alt="Residual Plot" src="https://github.com/user-attachments/assets/87b299ff-d92b-42cd-9f67-7cc19c51956f" />



### 5) A dataframe is created which includes **signals for buying and selling** of stocks based on z-score.

   <img width="4000" height="1600" alt="z-score behaviour" src="https://github.com/user-attachments/assets/f0900f34-ef8c-4b8a-9991-e2cf993a4b53" />


   <img width="6800" height="2000" alt="Signals" src="https://github.com/user-attachments/assets/888091d4-cafa-427f-9b96-7e624e4a519e" />



### 6) The pair trading portfolio is initiated on 1st July 2024, with an **initial capital of 100000 units** for each asset (i.e., with a total investment of 200000 units).

   At the end of 30 June 2025 the excess (or deficit) of the total portfolio value over the total initial investment of 200000 units is computed to       arrive at the **profit (or loss).**

   Based on the computed profit (or loss), the **return of the portfolio** is derived. 

### 7) 14.08% is the Return On Investment (ROI) for the selected pair of stocks.

  <img width="1517" height="546" alt="image" src="https://github.com/user-attachments/assets/9c029f92-660b-46c5-b9e0-bc274a63692f" />


