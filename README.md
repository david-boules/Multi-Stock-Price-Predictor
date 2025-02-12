# Multi-Stock Price Prediction 📈💹📉

## **📌 Project Overview**
This project aims to build a **deep learning-based multi-stock price prediction model** that forecasts future stock prices for a selected portfolio of stocks. The model leverages **historical stock price data**, **technical indicators**, and **deep learning techniques**. The project includes **Exploratory Data Analysis (EDA), feature engineering, model training, backtesting, and deployment**.

---

## **📌 Objectives**
- Collect **historical stock data** from Yahoo Finance.
- Perform **Exploratory Data Analysis (EDA)** to understand trends, correlations, and seasonality.
- Engineer **technical indicators** for better predictive power.
- Develop a **deep learning model** (LSTM, GRU, or Transformer) for stock price prediction.
- Evaluate model performance using **metrics like MAE, RMSE, and R-squared**.
  ***Optional:***
- Simulate **trading strategies** based on the model’s predictions.
- Deploy the model via **a Streamlit web app** for real-time predictions.

---

## **📌 Project Structure**
```
├── data/                      # Raw and processed datasets
├── notebooks/                 # Jupyter notebooks for analysis & model training
├── models/                    # Saved trained models
├── README.md                  # Project documentation
├── CONTRIBUTING.md            # Contributing guidelines
├── requirements.txt           # Dependencies
├── config.yaml                # Configurations for the project
└── .gitignore                 # Ignore unnecessary files
```

---

## **📌 Data Collection & Preprocessing**
### **1. Data Sourcing**
- Select a diverse portfolio of stocks (e.g., FAANG: Facebook, Apple, Amazon, Netflix, Google) and collect **historical stock price data** using **Yahoo Finance API**.
- Fetch **OHLCV (Open, High, Low, Close, Volume) data**.
- Set the data time range and ensure a **consistent frequency** (daily closing prices).

### **2. Data Cleaning**
- Handle **missing values** using forward fill (not backward fill since this causes data leakage)
- Remove **outliers** that could distort model training.
- Convert **date columns** into a proper datetime format.

---

## **📌 Exploratory Data Analysis (EDA)**
### **1. Time Series Visualization**
- Plot **historical stock prices**.
- Compute **moving averages (50-day, 200-day SMA)**.

### **2. Stationarity Check**
- Perform **Augmented Dickey-Fuller (ADF) test**.
- Apply **differencing** if needed.

### **3. Volatility & Risk Analysis**
- Compute **daily returns**.
- Identify stocks with the **highest and lowest volatility**.

### **4. Correlation Analysis**
- Generate a **heatmap** to check correlations between stocks.
- Identify stocks that move together or in opposite directions

### **5. Seasonality & Market Trends**
- Identify **seasonal patterns** (e.g. monthly price trends).
- Account for **major market events** (e.g., COVID-19 crash)

---

## **📌 Feature Engineering**
### **1. Technical Indicators**
- **Moving Averages**: SMA (50-day, 200-day), EMA (20-day)
- **Momentum Indicators**: RSI (Relative Strength Index), MACD (Moving Average Convergence Divergence)
- **Volatility Indicators**: Bollinger Bands
- **Volume-Based Features**: On-Balance Volume (OBV)

### **2. Time Series Sequence Preparation**
- Convert stock data into **sequential time series format**.
- Choose an **appropriate window size** (e.g., last **60 days of data** to predict the next day).

---

## **📌 Model Development**
### **1. Data Splitting & Normalization**
- Split data into **training (70%), validation (15%), and test sets (15%)**.
- Apply **MinMax scaling** or **Standardization** for better model convergence.

### **2. Model Selection**
Compare **deep learning architectures**:
- **LSTM (Long Short-Term Memory)** – Best for long-term dependencies.
- **GRU (Gated Recurrent Units)** – Computationally efficient.
- **Transformer-Based Models** – Advanced attention-based forecasting.

### **3. Model Training**
- Train models with **varied hyperparameters** (e.g., epochs, batch size, learning rate)
- Train models with **early stopping** to prevent overfitting.

### **4. Model Evaluation**
- Evaluate models using:
  - **Mean Absolute Error (MAE)**
  - **Root Mean Square Error (RMSE)**
  - **R-squared Score**
- Compare deep learning models against **traditional models (ARIMA, XGBoost)**.

---

## Optional Section:

## **📌 Backtesting & Strategy Simulation**
### **1. Backtesting Predictions**
- Use past predictions to simulate **trading decisions**.
- Compare performance with:
  - **Buy & Hold Strategy**
  - **Model-Driven Trading Strategy**.
- Compute profitability metrics:
  - **Cumulative Returns**
  - **Sharpe Ratio**.

---

## **📌 Model Deployment**
### **1. Deploying a Web App (Streamlit)**
- Build an **interactive UI** for stock price predictions.
- Allow users to **input stock tickers** and **forecast future prices**.
- Display **trend visualizations** and **model insights**.

### **2. Real-Time Prediction Integration**
- Fetch **live stock prices** from Yahoo Finance.
- Update **real-time predictions** dynamically.

---

## **📌 Timeline & Milestones**
| **Phase** | **Tasks** | **Duration** |
|---|---|---|
| **Phase 1** | Data Collection & Cleaning |
| **Phase 2** | EDA & Time Series Analysis |
| **Phase 3** | Feature Engineering |
| **Phase 4** | Model Development & Training |
Optional Section:
| **Phase 5** | Backtesting & Evaluation |
| **Phase 6** | Model Deployment (Streamlit) |
| **Phase 7** | Report & Documentation |

---

## **📌 Resources**
- Kaggle's Time Series for Machine Learning Course: https://www.kaggle.com/learn/time-series
- Stock Price Prediction Walktrhough: https://www.projectpro.io/article/stock-price-prediction-using-machine-learning-project/571

## **📌 Contributing**
Feel free to fork this repository, submit issues, and make pull requests.
