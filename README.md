# 📈 Hybrid Financial Forecasting Engine  
### Machine Learning + LSTM + Monte Carlo Simulation for Directional Market Prediction

---

## 🚀 Project Overview

This project builds a **Hybrid Financial Forecasting Engine** that combines:

- 📊 Machine Learning (XGBoost)
- 🧠 Deep Learning (LSTM Neural Network)
- 🎲 Monte Carlo Simulation
- 📉 Technical Indicator Engineering

The system generates a **probabilistic directional forecast (UP / DOWN)** for financial instruments using both statistical modeling and stochastic simulation.

Instead of relying on a single model, this engine blends multiple methodologies to improve robustness and market adaptability.

---

## 🎯 Objective

To create a hybrid forecasting framework that:

- Predicts short-term directional probability  
- Incorporates market regime detection  
- Models volatility and uncertainty  
- Simulates future price distributions  
- Provides visual, decision-support outputs  

---

## 🧠 Model Architecture

### 1️⃣ Feature Engineering

Engineered technical features including:

- RSI (Relative Strength Index)
- EMA(20) & EMA(50)
- EMA slope (momentum proxy)
- Rolling volatility (20-period standard deviation)
- 3-period and 7-period returns
- Market regime classification (EMA crossover logic)

---

### 2️⃣ XGBoost Classifier

- 300 estimators  
- Max depth: 6  
- Learning rate: 0.03  
- RobustScaler normalization  
- Binary classification (Up / Down threshold-based)

**Output:** Probability of upward price movement

---

### 3️⃣ LSTM Neural Network

- Sequence length: 20  
- LSTM (64 units)  
- Sigmoid output layer  
- MinMax scaling  
- Binary cross-entropy loss  

Captures sequential dependencies and temporal structure in price data.

---

### 4️⃣ Monte Carlo Simulation

- 3,000 simulations  
- Geometric Brownian Motion framework  
- Drift and volatility estimated from recent returns  

Generates:

- Simulated future price paths  
- 5%–95% probability cone  
- Final price distribution histogram  

---

### 5️⃣ Final Hybrid Probability

Final directional probability is calculated as:

```
ML Probability = (0.6 × XGBoost) + (0.4 × LSTM)

Final Probability = 
(0.5 × ML Probability) + (0.5 × Monte Carlo Up Probability)
```

This creates a blended probabilistic forecast using:

- Supervised machine learning  
- Deep learning sequence modeling  
- Stochastic financial simulation  

---

## 📊 Visual Outputs

The engine generates:

- ✅ Final Direction Probability Bar Chart  
- ✅ Monte Carlo Simulation Paths  
- ✅ Probability Cone (5%–95% range)  
- ✅ Final Price Distribution Histogram  

These visualizations improve interpretability and decision support.

---

## 🛠️ Tech Stack

- Python  
- NumPy  
- Pandas  
- yFinance  
- XGBoost  
- TensorFlow / Keras  
- Scikit-learn  
- Plotly  

---

## 📥 User Inputs

The engine accepts:

- Ticker (e.g., RELIANCE.NS)  
- Timeframe (1m, 5m, 15m, 1h, 1d, 1wk)  
- Forecast horizon (number of future bars)  

---

## 📌 Sample Output

Example configuration:

```
Ticker: RELIANCE.NS  
Timeframe: 15m  
Horizon: 120
```

Final Directional Probability:

```
UP   : 25.08%
DOWN : 74.92%
```

---

## 💡 Key Financial Insights

- Integrates technical indicators with ML classification  
- Adapts to short-term volatility shifts  
- Models uncertainty through distribution-based simulation  
- Provides probabilistic (not deterministic) forecasts  
- Suitable for quantitative research and financial modeling experimentation  

---

## ⚠️ Disclaimer

This project is developed for educational and research purposes only.  
It does not constitute financial advice and should not be used directly for live trading decisions.

---

## 📈 Why This Project Matters

This project demonstrates:

- Financial domain understanding  
- Advanced feature engineering  
- Machine learning modeling  
- Deep learning for time-series forecasting  
- Risk modeling using Monte Carlo methods  
- Data visualization and interpretability  
- Hybrid quantitative modeling architecture  

It reflects practical quantitative finance and financial data analytics capability.
