# Nifty50-options--model
A project to give buying signals for nifty 50 weekly options
## Project Overview
The project aims to help buy call options on the Nifty 50 by analysing processed stock data to predict the one-week maximum price. The model looks at the stock from a purely technical standpoint.  A threshold of 2% is fixed as the minimum for a positive signal. The price movement has been assumed to be a strictly time series model.
## Data Collection and preprocessing
Raw stock data was downloaded from the Nse website. this data only contains, the high, low, open and close of each day and is not enough to predict over a one-week frame. The data is preprocessed using pandas. The predictor variables are the percentage increases from the minimum 7,14,21,28 day intervals before the particular date. The output variable is the percentage increase to a maximum within a 7-day future interval. If this is above 2%, the Y variable is 1, otherwise it is 0. Though data is prepared for 5 years for all trading days, only Thursdays are considered as all one-week NIFTY 50 options mature on Thursdays. 

