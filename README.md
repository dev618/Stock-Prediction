# 📈 StockLSTM – Deep Learning for Tesla Price Forecasting

This project demonstrates how to build a **Long Short-Term Memory (LSTM)** model using **Keras** to predict Tesla's stock closing prices based on historical data.

---

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-LSTM-red?logo=keras)
![NumPy](https://img.shields.io/badge/NumPy-Array%20Processing-blue?logo=numpy)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Manipulation-yellow?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?logo=matplotlib)
![Yahoo Finance](https://img.shields.io/badge/Yahoo%20Finance-Stock%20Data-purple)

---
**Tags:**
[deep-learning](#) [lstm](#) [stock-prediction](#) [time-series-analysis](#) [tensorflow](#) [keras](#) [tesla](#) [tsla](#) [yahoo-finance](#) [machine-learning](#) [python](#) [numpy](#) [pandas](#) [matplotlib](#) [minmaxscaler](#) [price-forecasting](#) [sequential-mod]()



## 🧠 Project Objective

The main objective is to:

- Load historical Tesla stock price data
- Preprocess and normalize the data
- Create time-series sequences for the LSTM model
- Train the LSTM neural network
- Predict and visualize future stock prices

---

## 📂 Dataset

- **Dataset used:** `TSLA.csv`  
- **Source:** [Yahoo Finance](https://finance.yahoo.com/)  
- **Important feature:** `Close` price of the stock  
- The `Date` column is set as the index for time series analysis

---


## 🧪 Model Architecture

- **Model:** Sequential  
- **Layers:**
  - LSTM layer with **50 units**
  - Dense layer with **1 output**
- **Loss function:** Mean Squared Error (MSE)  
- **Optimizer:** Adam  
- **Epochs:** 100  
- **Batch size:** 32  

---

## 🔁 Data Preprocessing Steps

1. Load and parse the `Date` column
2. Extract only the `Close` prices
3. Apply **MinMaxScaler** to scale the data between 0 and 1
4. Create sequences of `60` days to predict the `61st` day price
5. Split the dataset into **80% training** and **20% testing**

---


## 📊 Results
Training Accuracy: Achieved low loss values indicating good learning

Predictions: Accurately predicted trends and closing prices

Visualization: Plotted predicted vs actual prices for clear comparison



