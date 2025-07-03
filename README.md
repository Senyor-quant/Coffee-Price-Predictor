
# 📈 Coffee Price Predictor: LSTM Model for Arabica Forecasting

## 🌱 Project Overview
This project uses Long Short-Term Memory (LSTM) neural networks to forecast Arabica coffee prices based on weather, climate, and macroeconomic data. Built as part of a data-driven investment analysis at A&F Investments, the model supports intraday trading decisions with a systematic, fully automated pipeline.

## 🔍 Data Sources
- **🌦 Weather Data**: OpenWeather API — temperature, humidity, wind speed, precipitation, soil moisture
- **🌊 Climate Data**: NOAA Oceanic Niño Index — El Niño/La Niña indicators
- **💱 Macroeconomic Data**:
  - BRL/USD exchange rate (apilayer)
  - CFTC Net Futures Positions (COT reports)

All data is automatically scraped, cleaned, and merged into a single modeling-ready dataset.

## 🧠 Model Summary
- LSTM model trained on 30-day input sequences
- Forecasts next-day coffee prices
- Uses 5-fold expanding-window cross-validation
- Hyperparameters optimized via Genetic Algorithm
- Output used for daily trading decisions (go long/short)

## 🛠 Forecasting Pipeline
1. Scrape & merge data (weather, climate, macro)
2. Normalize using Min-Max scaling
3. Generate 30-day sliding windows
4. Train LSTM via backpropagation through time
5. Predict next-day coffee prices
6. Apply trade rules based on forecast deltas

## 📊 Results (Backtest Summary)
- **Total PnL**: €320.68
- **Average PnL/trade**: €0.70
- **Sharpe Ratio**: 0.48
- **Annualized Return**: 2.76%
- **Volatility**: 3.06%
- **Trades Executed**: 459 (over 8 years)

## 📁 Project Structure
```
coffee-price-predictor/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   └── 01-lstm-model.ipynb
├── src/
│   ├── data_loader.py
│   ├── train_model.py
│   └── trading_strategy.py
├── requirements.txt
├── .gitignore
└── README.md
```

## 🚀 Getting Started
1. Clone the repo  
```bash
git clone https://github.com/YOUR_USERNAME/coffee-price-predictor.git
cd coffee-price-predictor
```

2. Install requirements  
```bash
pip install -r requirements.txt
```

3. Run training notebook or `src/train_model.py` to begin modeling.

## 👥 Authors
- Barak Azor
- Mark Schulitschenko
- Andrii Kyrylenko
- Jule Broeders
- Sarah Elshawaf
- Senyo Azasoo

Project for **A&F Investments – May 2025**

## 📄 License
This project is licensed under the [MIT License](LICENSE).
