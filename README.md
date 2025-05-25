# 📈 EUR/USD Forex Rate Forecasting Using ANN & ARIMA

A comparative implementation of **Artificial Neural Networks (ANN)** and **Autoregressive Integrated Moving Average (ARIMA)** for predicting EUR/USD hourly exchange rate trends. This project aligns with the research paper [_"A Comparative Analysis of Machine Learning Algorithms for USD/EUR Foreign Exchange Rate Forecasting"_](https://www.irejournals.com/formatedpaper/1706704.pdf) authored by Mubaraq Onipede and team at the National Center for Artificial Intelligence and Robotics, Nigeria.

---

## 🧠 Project Overview

The foreign exchange (Forex) market is notoriously volatile and non-linear. This project investigates two powerful approaches for trend forecasting:

- **ARIMA**: a classical statistical model for identifying and extrapolating linear trends.
- **ANN**: a deep learning model designed to capture complex, non-linear patterns in sequential financial data.

The dataset consists of **hourly EUR/USD exchange rate data** sourced from **MetaTrader 5**, covering **January 2013 – September 2016**.

---

## 🔍 Research Objectives

- Forecast hourly EUR/USD trends using supervised learning.
- Compare ANN and ARIMA based on their predictive performance.
- Explore how technical indicators enhance financial time series forecasting.
- Evaluate models using metrics like **Precision**, **Recall**, and **Accuracy**.

---

## 🧰 Technologies Used

| Tool        | Purpose                          |
|-------------|----------------------------------|
| Python      | Core language                    |
| Pandas, NumPy | Data preprocessing             |
| Scikit-learn | Feature scaling, metrics        |
| Statsmodels | ARIMA modeling                   |
| TensorFlow / Keras | ANN modeling             |
| Matplotlib / Seaborn | Visualizations         |

---


## 🧮 Model Summary

### 📊 ARIMA

- **Purpose**: Linear trend modeling
- **Configuration**: ARIMA(1,1,1)
- **Stationarity**: Verified using Augmented Dickey-Fuller (ADF) Test
- **Limitations**: Failed to capture rapid non-linear trend reversals

### 🤖 ANN

- **Architecture**: Multi-layer Perceptron with 9 dense hidden layers
- **Activation**: ReLU in hidden layers, Sigmoid in output
- **Optimizer**: Adam
- **Regularization**: Early stopping to prevent overfitting
- **Feature Engineering**:
  - RSI
  - Bollinger Bands (Upper, Middle, Lower)
  - Moving Averages (9 & 21)
  - ATR (Average True Range)
  - Custom "Trend" label

---

## 📈 Evaluation Metrics

| Model       | Precision       | Recall          | Accuracy       | Remarks                        |
|-------------|------------------|------------------|----------------|--------------------------------|
| ARIMA       | Moderate          | Low for reversals | ~50%           | Good with linearity            |
| ANN         | Balanced (0.54 avg) | High on majority class | 51–53%      | Better on turning points       |

---

## 📌 Key Insights

- **ANN** is better suited for capturing **non-linear, volatile** price movements.
- **ARIMA** provides reliable forecasting in **stationary linear trends**.
- A **hybrid model** leveraging both approaches could improve real-world performance.

---

## 📚 Reference

Onipede, M., Abiamamela, O., & Olorunsola, J. (2024). _A Comparative Analysis of Machine Learning Algorithms for USD/EUR Foreign Exchange Rate Forecasting_, IRE Journals, Vol 8, Issue 6.  
📄 [Read the Full Paper](https://www.irejournals.com/paper-details/1706704)


## Datasets

For evaluation and improvement, datasets can be provided upon request.

## 🚀 Getting Started

1. Clone this repository  
   ```bash
   git clone https://github.com/yourusername/eurusd-forecasting-ann-arima.git
   cd eurusd-forecasting-ann-arima

