# LSTM Trading Bot

A machine learning project that uses Long Short-Term Memory (LSTM) neural networks to predict stock market movements.

## Project Overview

This trading bot analyzes historical stock price data and makes predictions about future price movements. It uses LSTM (a type of recurrent neural network) to learn patterns from historical data and technical indicators to make predictions.

## Technologies Used

- **Python**: The primary programming language
- **TensorFlow/Keras**: For building and training the neural network model
- **Pandas**: For data manipulation and analysis
- **NumPy**: For numerical operations
- **Matplotlib**: For data visualization
- **yfinance**: For downloading historical stock price data
- **pandas_ta**: For calculating technical indicators
- **scikit-learn**: For data preprocessing

## Features

1. **Data Collection**: Downloads historical stock price data (in this case, Apple Inc.) using the yfinance library.

2. **Technical Analysis**: Calculates several technical indicators:
   - Relative Strength Index (RSI)
   - Exponential Moving Averages (EMA) of different periods (9, 21, 50)
   - Bollinger Bands
   - Stochastic Oscillator
   - Average True Range (ATR)
   - On-Balance Volume (OBV)
   - Volume Weighted Average Price (VWAP)

3. **Data Preprocessing**:
   - Normalizes data using MinMaxScaler
   - Organizes data into time sequences (using past 30 days to predict next movement)
   - Splits data into training and testing sets (90% training, 10% testing)

4. **LSTM Model**:
   - Uses a neural network with LSTM layers
   - Compiled with Adam optimizer and Mean Squared Error loss function
   - Trained over 50 epochs with batch size of 10

5. **Performance Evaluation**:
   - Measures performance using Mean Absolute Error
   - Visualizes predictions vs actual values
   - Calculates prediction accuracy for binary (up/down) predictions

## How to Use

1. Make sure you have Python installed
2. Install required libraries:
   ```
   pip install tensorflow pandas numpy matplotlib yfinance pandas_ta scikit-learn keras
   ```
3. Run the Jupyter notebook `trading_bot.ipynb`
4. You can modify the stock ticker (currently set to 'AAPL') and date range to analyze different stocks or time periods

## Notes

- This is a research project and not financial advice
- The model's performance depends on market conditions and the quality of historical data
- You can improve prediction accuracy by tuning parameters or adding more features

## Future Improvements

- Add more technical indicators
- Implement a trading strategy based on predictions
- Add backtesting functionality
- Optimize hyperparameters
- Extend to multiple stocks