# LSTM Stock Predictor

![deep-learning.jpg](Images/deep-learning.jpg)

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. I am being asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

In this assignment, I will be using deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

Requirements:

1. [Prepare the data for training and testing](#prepare-the-data-for-training-and-testing)
2. [Build and train custom LSTM RNNs](#build-and-train-custom-lstm-rnns)
3. [Evaluate the performance of each model](#evaluate-the-performance-of-each-model)

- - -

### Files

[Closing Prices Starter Notebook](Starter_Code/lstm_stock_predictor_closing.ipynb)

[FNG Starter Notebook](Starter_Code/lstm_stock_predictor_fng.ipynb)

- - -

## Explaining the process (Following Instructions)

### 1. Preparing the data for training and testing

I used the starter code as a guide to create a Jupyter Notebook for each RNN. The starter code contains a function to create the window of time for the data in each dataset.

For the Fear and Greed or "Fear of Missing Out" (FOMO) model, I used the FNG values to try and predict the closing price. A function is provided in the notebook to get me started.

For the closing price model, I used the previous closing prices to try and predict the next closing price. A function is provided in the notebook to get me started.

Each model will need to use 70% of the data for training and 30% of the data for testing.

I then applied a MinMaxScaler to the X and y values to scale the data for the model.

Finally, I reshaped the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (*example:* `X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1))`)

### 2. Building and training custom LSTM RNNs

In each Jupyter Notebook, I created the same custom LSTM RNN architecture. In FOMO notebook I fitted the data using the FNG values. In the second notebook, I fitted the data using only closing prices. Finally, I used the same parameters and training steps for each model so as to compare each model accurately.

### 3. Evaluating the performance of each model

Evaluating each model and comparing the performance using the above analysis to answer the following:

> Which model has a lower loss?

# 

> Which model tracks the actual values better over time?

#
> Which window size works best for the model?

# 
- - -

### Resources

[Keras Sequential Model Guide](https://keras.io/getting-started/sequential-model-guide/)

[Illustrated Guide to LSTMs](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21)

[Stanford's RNN Cheatsheet](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-recurrent-neural-networks)

- - -

- - -

© 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
