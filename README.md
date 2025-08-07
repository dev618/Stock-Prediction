# 📈 Tesla Stock Price Prediction using LSTM

This project demonstrates how to build a **Long Short-Term Memory (LSTM)** model using **Keras** to predict Tesla's stock closing prices based on historical data.

---

## 🧠 Project Objective

The main objective is to:

- Load historical Tesla stock price data
- Preprocess and normalize the data
- Create time-series sequences for the LSTM model
- Train the LSTM neural network
- Predict and visualize future stock prices

---

## 📂 Dataset

- Dataset used: `TSLA.csv`
- Source: [Yahoo Finance](https://finance.yahoo.com/)
- Important feature: `Close` price of the stock
- The `Date` column is set as the index for time series analysis

---

## 📌 Key Libraries Used

- `pandas` – Data manipulation
- `numpy` – Numerical operations
- `matplotlib` – Visualization
- `sklearn.preprocessing.MinMaxScaler` – Feature scaling
- `keras` – Deep learning model (LSTM)

---

## 🧪 Model Architecture

- Model: **Sequential**
- Layers:
  - LSTM layer with 50 units
  - Dense layer with 1 output
- Loss function: `Mean Squared Error`
- Optimizer: `Adam`
- Epochs: `100`
- Batch size: `32`

---

## 🔁 Data Preprocessing Steps

1. Load and parse the `Date` column
2. Extract only the `Close` prices
3. Apply **MinMaxScaler** to scale the data between 0 and 1
4. Create sequences of `60` days to predict the `61st` day price
5. Split the dataset into **80% training** and **20% testing**

---

## 🧩 Sequence Function

```python
def create_sequences(data, seq_length):
    X, y = [], []
    for i in range(len(data) - seq_length):
        X.append(data[i:i+seq_length])
        y.append(data[i+seq_length])
    return np.array(X), np.array(y)
