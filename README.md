# Stock Price Prediction Application

## Overview

This Streamlit application predicts stock prices using a pre-trained LSTM model. Users can input a stock symbol, select a date range, and choose the number of days to forecast. The app will fetch historical stock data, make predictions, and display the results.

## App Link

Click [here](https://time-series-abe.streamlit.app/) to access the application.

## Features

- **Predict Stock Price**: 
  - Input a stock symbol (e.g., AAPL for Apple).
  - Select a date range for historical data.
  - Choose the number of days for which to forecast stock prices.
  - The app fetches historical data, makes predictions using an LSTM model, and displays both actual and predicted prices.
  - Provides a side-by-side view of the predicted prices and the stock’s logo.
  - Displays a plot comparing actual vs predicted prices.

- **About**:
  - Provides information about the application and its functionality.



## Code Explanation

### Page Configuration
Sets the title of the web page to "Stock Price Prediction Application."

### Model Loading
Loads the pre-trained LSTM model from a `lstm_model.pkl` file using `joblib`.

### Function to Get Stock Image URL
A placeholder function that should return the image URL for a given stock symbol. This function needs to be implemented based on the actual image source.

### Streamlit Application Main Function

1. **Title**: Displays the title of the app.
   
2. **Sidebar Navigation**: 
   - Uses the `streamlit_option_menu` to create a sidebar with options for "Predict Stock Price" and "About."

3. **Predict Stock Price**:
   - **Inputs**: 
     - `ticker`: Enter the stock symbol.
     - `start_date` and `end_date`: Choose the date range for fetching historical data.
     - `forecast_periods`: Slider to select the number of days to forecast.
   - **Data Fetching**: 
     - Retrieves historical stock data using the `yfinance` library.
   - **Data Preparation**:
     - Scales the closing prices and prepares the data for prediction.
   - **Forecasting**:
     - Uses the LSTM model to forecast future stock prices.
     - Inverse scales the predicted prices to their original scale.
   - **Display Results**:
     - Shows a table with predicted prices and dates.
     - Displays the stock logo (if implemented) and the predicted prices in a Plotly chart.
   
4. **About Section**:
   - Provides a brief description of the app's purpose and usage.

## Requirements

- Streamlit
- Pandas
- NumPy
- Plotly
- yFinance
- joblib
- scikit-learn
- datetime
- streamlit_option_menu

Ensure all required packages are installed before running the app.

---

Feel free to customize this README to better fit your project's needs or provide additional details about the app.
