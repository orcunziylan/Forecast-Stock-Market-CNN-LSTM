# Stock Market Forecasting using CNN and LSTM

This project demonstrates the use of Convolutional Neural Networks (CNN) and Long Short-Term Memory (LSTM) networks for forecasting stock market prices. The historical candlestick data of a stock is used to train a deep-learning model that predicts the next day's opening price relative to the previous day's closing price.

## Project Overview

The goal of this project is to forecast stock market prices using a combination of CNN and LSTM networks. The project involves the following steps:

1. **Data Collection**: Historical candlestick data for a given stock is downloaded using the `yfinance` library. This data includes the open, high, low, and close prices of the stock.

2. **Data Preprocessing**: The downloaded data is preprocessed to create input-output pairs for training. For each week, a set of daily candlestick data is used as input, and the opening price of the next day is used as the target output.

3. **Candlestick Plotting**: The daily candlestick data is plotted using the `mpl_finance` library and saved as images. Each week's data is plotted as a candlestick figure to visualize the stock's price movement.

4. **Model Architecture**: The project uses a CNN-LSTM hybrid model. The CNN extracts features from the plotted candlestick images, and the LSTM processes the extracted features to make predictions.

5. **Training and Evaluation**: The model is trained using the training dataset and evaluated on the validation dataset. The mean squared error (MSE) is used as the loss function for training.

6. **Model Checkpointing and Early Stopping**: The model's training progress is monitored using early stopping to prevent overfitting. The best model checkpoint is saved based on validation loss.

## Dependencies

The project code requires the following libraries:

- `yfinance`: To download historical stock market data.
- `mpl_finance`: To plot candlestick figures.
- `pytorch_lightning`: A lightweight PyTorch wrapper for training and evaluation.
