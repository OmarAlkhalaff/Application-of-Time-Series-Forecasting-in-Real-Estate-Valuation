# Application-of-Time-Series-Forecasting-in-Real-Estate-Valuation

The project involves a real-world dataset, the work is categorized into three main parts

 - Notebook 1: EDA & Feature Engineering.
 - Notebook 2: Static Modeling for Producing Time Series
 - Notebook 2: Mean-Point Time Series Modeling
 
 We will be working with a dataset of tokyo trades published by Ministry of Land, Infrastructure, Transport and Tourism of Japan (MLIT). The dataset is originally reported in japanese languge and was translated by a kaggle contributer. In addition to the trades data, we will be incorporating the housing consumer price index for japan. 
 
 After EDA & feature engineering we will proceed to with two different approaches to model the prices, the approaches in a nutshell: 
 
 - Static Modeling for Producing Time Series: 
   We will produce static models for every quarter of every year. Then predict the price of an instance, using all quarter models. The result is a predicted time series    which will then be forecasted into the future using an LSTM. It should be noted that the timestamps ['Year','Quarter'] are not features in this approach.
   
 - Mean-Point Time Series Modeling: 
  The pipepline is built to take an instance X, and produce a time series that best represent X. The time series is then forecasted using baseline models and an LSTM       model. The catch in this approach is that the time series produced does not come from model predictions (as in the approach in notebook 2), rather it is produced by     sampling from the full dataset based on certain criteria. 
 
  
 The columns we will be working with initially:
![Capture](https://user-images.githubusercontent.com/99807928/187086980-67801c1a-bf41-474b-93fd-d3059ec450ef.PNG)


 The data is collected from the following sources:
  - for Trades data: https://www.kaggle.com/datasets/nishiodens/japan-real-estate-transaction-prices
  - for Housing Consumer Price index: https://fred.stlouisfed.org/series/JPNCPGRHO01IXOBQ
