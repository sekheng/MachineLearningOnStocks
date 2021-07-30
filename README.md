# Machine Learning On Stocks

Created as a group project for CZ/CE1115 in order to answer one of the biggest questions on everyone's mind: 

**Is Stocks and Cryptocurrency the best Savings Account?**

In order to learn more about the stock markets with machine learning, we decided to try out 2 ways of to predict the stock market:
- Polynomial Regression Line
- Multivariate Long Short Term Memory(LSTM) Model

## First, how much can we earn on Savings Account?
We take a look at how much we can earn by extrapolating **10000 USD** over 10 days based on an annual interest rate of 0.05% according to POSB savings account. The result isn't that astonishing.

![POSB disappointing interest](/Images/POSB_interest_earned.png "10 days of Interest earned on Savings Account")

So we are going to explore what if we put them into stocks or cryptocurrency.

## Polynomial Regression on Cryotcurrency

Polynomial regression is based on 
> y = x^2 + x + c 

The number of degrees can vary.

Taking **last 3 years (The last day is 18 April 2021) worth** of data of the most popular cryptocurrency: Bitcoin, Litecoin(Ltc), and Ethereum(Eth)

We train and test the formula we have mentioned above

### Bitcoin training and test data

![Training the formula on BTC data](/Images/btc_train.png "BTC Train data")
- Explained Variance: 0.97
- Root Mean Squared Error: 2502.54

![Test on BTC data](/Images/btc_test.png "BTC test data")
- Explained Variance: 0.97
- Root Mean Squared Error: 2133.13

The explained variance is very close to 1 as the higher the number, the more accurate the model. The Root Mean Squared Error is also very close to each other.

The same can be seen in LTC and ETH.

### ETH training and test data

![Training the formula on ETH data](/Images/eth_train.png "ETH Train data")
- Explained Variance: 0.96
- Root Mean Squared Error: 97.86

![Test on ETH data](/Images/eth_test.png "ETH test data")
- Explained Variance: 0.95
- Root Mean Squared Error: 95.04

### LTC training and test data

![Training the formula on LTC data](/Images/ltc_train.png "LTC Train data")
- Explained Variance: 0.84
- Root Mean Squared Error: 19.39

![Test on LTC data](/Images/ltc_test.png "LTC test data")
- Explained Variance: 0.81
- Root Mean Squared Error: 18.9

### Forecasting investment in cryptocurrency
Since the formula can reliably simulate the growth of cryptocurrency, we can now proceeed to predict the next 10 days and put them in comparison against Savings account:

![Forecasting of cryptocurrency](/Images/crypto_predict.png "Predict 10 days of cryptocurrency growth")

We can safely say that investing in cryptocurrency will beat Savings Account anytime!

## Multivariate LSTM on Tesla

LSTM is a model in TensorFlow that can predict stock market to a certain accuracy. When training the model with large amount of data from 2017 to 2020 and include multiple parameter such as 'Open' and 'Close', the model can be surprisingly accurate.




You can refer to [Our Machine Learning Google Colab](/StocksTheBestSavingAccount.ipynb "Our codes on ipynb") that we have done numerous steps to achieve the end result including data collection, and how we split the data into train and test dataset.

## Credits:
- Lee Sek Heng
- Chua Eng Soon
