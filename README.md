# 📈 Stock Price Movement Prediction

This project builds a machine learning model to predict the **next-day stock price movement** (up or down) for the NSE-listed company **Tata Consumer Products (TATACONSUM.NS)** using historical data from Yahoo Finance (`yfinance`). The prediction is framed as a **binary classification** problem based on technical indicators and price movements.

---

## 🧠 Problem Statement

Can we predict whether the stock price will rise or fall the next day using only price-related features?  
This project attempts to answer that using supervised learning and feature engineering.

---

## 🔍 Features Used

- `Open-Close`: Difference between opening and closing prices
- `High-Low`: Daily trading range
- `SMA_5`, `SMA_10`: Simple Moving Averages over 5 and 10 days
- `Price_Change`: Daily return (percentage)

---

## 🛠 Tools & Libraries

- Python 🐍
- Pandas & NumPy
- yfinance
- scikit-learn (KNN, GridSearchCV)
- Matplotlib for visualization

---

## 🧪 Model Overview

- **Model**: K-Nearest Neighbors (KNN)
- **Label**: `1` if next day's closing price is higher than today, `-1` otherwise
- **Train-Test Split**: 75% / 25%
- **Tuning**: GridSearchCV to find optimal `k` value
- **Metrics**:
  - Training Accuracy: ~67%
  - Test Accuracy: ~51% (indicates underfitting and high market noise)

---

## 📊 Results

Despite feature engineering, the model achieves limited performance. Stock price movements are notoriously noisy and difficult to predict with simple features. The test accuracy (~51%) is only slightly better than random guessing — highlighting the need for:
- Advanced models (e.g. Random Forest, LSTM)
- Better feature sets (e.g. RSI, MACD, Volume analysis)
- Time-series-specific approaches

---

## 📌 Future Improvements

- Add technical indicators using `ta` or `pandas-ta` libraries
- Use Random Forest or Gradient Boosting classifiers
- Try time-series models like ARIMA or LSTM
- Balance the dataset if classes are imbalanced
- Deploy a web app using Streamlit or Flask

---

## 🚀 How to Run

### 1. Clone this repo
```bash
git clone https://github.com/yourusername/stock-price-prediction.git
cd stock-price-prediction
