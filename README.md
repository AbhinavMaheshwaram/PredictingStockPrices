# Stock Price Prediction Project Documentation

## Overview
This document outlines the process and methodology used to create a stock price prediction model using historical stock data and machine learning techniques.

## Project Goals
The primary goal of this project is to predict future stock prices based on historical data. This prediction can assist investors in making informed decisions about buying or selling stocks.

## Tools and Libraries Used
- Python programming language
- Libraries:
  - numpy
  - pandas
  - matplotlib
  - yfinance
  - scikit-learn
  - keras

## Data Collection
- Data source: Yahoo Finance
- Stock: Google (GOOG)
- Timeframe: January 19, 2014, to December 30, 2023

## Preprocessing
1. Importing necessary libraries.
2. Downloading stock data using the `yfinance` library.
3. Resetting the index of the data.
4. Calculating moving averages for 100 and 200 days.
5. Handling null values using `dropna` function.
6. Splitting data into training and test sets (80/20 ratio).
7. Scaling data using `MinMaxScaler` to normalize between 0 and 1.

## Model Building
1. Utilizing LSTM (Long Short-Term Memory) neural network for sequence prediction.
2. Constructing the model architecture with multiple LSTM layers and dropout regularization to prevent overfitting.
3. Compiling the model with Adam optimizer and mean squared error loss function.
4. Training the model with the training data for 50 epochs.

## Model Evaluation
1. Generating predictions for the test data.
2. Scaling back the predicted and actual prices to their original scales.
3. Visualizing the predicted and actual prices using matplotlib.

## Save the Model
1. Saving the trained model using the `.save()` function in Keras.

## Conclusion
- The LSTM model shows promising results in predicting stock prices based on historical data.
- Further optimization and fine-tuning may enhance the model's performance.
- The saved model can be deployed for real-time predictions or further analysis.
