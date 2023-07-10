# Heirarchical Time Series Forecasting of Retail Inventory

As part of Kaggle's M5 forecasting challenge, We are given 3 years of sales data for 10 walmart stores.  These stores are divided among 3 states, California, Wisconsin, and Texas.  Each store's items are broken down further into 3 departments, Hobbies, Food and Household.  The challenge was to create a time series forcast for each item, by all different levels of aggreagtion.  

## The solution

Feature engineering was by far the most difficult part of this challenge, arranging and combining the datasets so that in a dataframe we would have all the different time series indexed.  Once this was done, running the vectors through the models was fairly straight forward, if time consuming.  

## Results

The results were measured through a custom metric that weighted the least squared error for each item.  This is so each item can have the same impact on the overall score.  For example, being off by 100 potatoes isn't that big of a deal, but being off by 100 TV's is.  So we need to weight the value of each into the final evaluation.  

The final normalized weighted root mean squared error was .58
