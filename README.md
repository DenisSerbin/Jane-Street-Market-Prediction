# Jane-Street-Market-Prediction
My first Kaggle competition [Jane Street Market Prediction](https://www.kaggle.com/competitions/jane-street-market-prediction).
With the score of 4433.879 (the winner score was 6476.594) I got the 138th place among 4085 teams).

But the most important part was that I learnt a lot about Data Science, ML and Kaggle itself from other participants. Invaluable experience.

## The competition
Jane Street provided a dataset containing an anonymized (very secretive people!) set of features, representing real stock market data together with several 'resp' values, that represent returns over different time horizons. Each row in the dataset represents a trading opportunity and the goal is to predict an action value: 1 to make the trade and 0 to pass on it.

The competition was evaluated based on the [utility score](https://www.kaggle.com/competitions/jane-street-market-prediction/overview/evaluation), which is essentially the anualized Sharpe Ratio.

## Datasets
The original training dataset is given in two files: 
 - 'train.csv' - the training set, contains historical data and returns,
- 'features.csv' - metadata pertaining to the anonymized features.

Apparently, the files are not avilable anymore on the competition's page :(

## Solution

A multilayer perceptron with six hidden layers takes all 130 anonymized features and outputs a vector of 5 future returns which are then used to calculate the action action value (see [janestreet-model-7.ipynb](janestreet-model-7.ipynb)).
