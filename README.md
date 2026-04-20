# 📈 Stock Market Forecasting of MAANG Companies using LSTM

## 📌 Project Overview

This project focuses on forecasting stock prices of **MAANG companies** (Meta, Apple, Amazon, Netflix, Google) using deep learning techniques, specifically **LSTM (Long Short-Term Memory) neural networks**.

The workflow includes real-time data collection, exploratory analysis, technical indicator engineering, time-series modeling, and future price prediction.

---

## 🚀 Key Features

* Real-time stock data extraction using `yfinance`
* Technical analysis with moving averages (MA20, MA40)
* Interactive visualizations (candlestick + trend charts)
* Deep learning model using **LSTM neural networks**
* Multi-step sequence generation for time-series forecasting
* Model evaluation using RMSE, MAE, and MAPE
* Live-like prediction pipeline for next-day stock price

---

## 📊 Dataset

* **Source:** Yahoo Finance (`yfinance`)
* **Companies:**

  * Google (GOOG)
  * Amazon (AMZN)
  * Apple (AAPL)
  * Meta (META)
  * Netflix (NFLX)
* **Time Range:** Historical data from 2020 onwards (configurable)
* **Features:**

  * Open, High, Low, Close (OHLC)
  * Volume
  * Derived indicators (Moving Averages)

---

## 🧠 Model Architecture

The forecasting model is built using LSTM layers:

* Input sequence window (100 timesteps)
* LSTM Layer (64 units, return sequences)
* Dropout (0.2)
* LSTM Layer (64 units)
* Dropout (0.2)
* Dense Output Layer (1 unit)

**Loss Function:** Mean Squared Error
**Optimizer:** Adam

---

## 🔄 Workflow

### 1. Data Collection

* Fetch stock data using `yfinance`
* Combine multiple MAANG company datasets

### 2. Feature Engineering

* Compute MA20 and MA40 moving averages
* Normalize data using MinMaxScaler

### 3. Sequence Creation

* Convert time-series data into supervised learning format
* Create sliding windows for LSTM input

### 4. Model Training

* Train LSTM model on historical stock data
* Validate using train/test split

### 5. Prediction

* Predict next-day stock prices
* Compare predicted vs actual values

---

## 📉 Evaluation Metrics

* Root Mean Squared Error (RMSE)
* Mean Absolute Error (MAE)
* Mean Absolute Percentage Error (MAPE)

---

## 📊 Visualizations

* Candlestick charts for stock trends
* Moving average trend overlays
* Actual vs Predicted price graphs
* Real-time price fetch simulation

---

## 🛠️ Tech Stack

* Python 🐍
* Pandas & NumPy
* Matplotlib & Plotly
* Scikit-learn
* TensorFlow / Keras
* yFinance API

---

## 🔍 Key Insights

* LSTM effectively captures short-term stock movement patterns
* MAANG stocks show strong volatility with clear trend cycles
* Moving averages help smooth noise but do not fully capture sudden market shifts
* Model performance is sensitive to sequence length and market volatility

---

## 📌 Future Improvements

* Add sentiment analysis from news/Twitter
* Use Transformer-based time-series models
* Deploy as a web dashboard (Streamlit/Dash)
* Add portfolio optimization module

This project is for **educational and research purposes only**.
