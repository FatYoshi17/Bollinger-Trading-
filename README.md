# Transformer-Based Trading Strategy (MATLAB)

A hybrid algorithmic trading system that integrates Bollinger Bands with a Transformer-based time-series model to predict 5-day forward returns.

This project combines technical analysis with deep learning to build a volatility-aware, risk-controlled trading strategy.

---

## 📌 Strategy Overview

The system consists of:

- **Volatility Regime Detection** using Bollinger Bands
- **Transformer Encoder Model** for multi-step return forecasting
- **Hybrid Signal Logic** (mean-reversion + model confirmation)
- **Transaction-cost-aware backtesting engine**

---

## 🧠 Feature Engineering

The following predictive features were engineered:

- %B (position within Bollinger Bands)
- Bandwidth
- RSI (Relative Strength Index)
- ROC (Rate of Change)
- Normalized distance to upper/lower bands
- Daily returns

All inputs were standardized using training-set statistics to prevent data leakage.

---

## 🤖 Model Architecture

- Sequence length: 30 days
- Transformer encoder with multi-head self-attention
- Feed-forward network + residual connections
- Global average pooling for regression output
- Chronological train/test split (no look-ahead bias)
- GPU-accelerated training (MATLAB R2025a)

Target: **5-day forward return prediction**

---

## 📊 Backtesting Setup

- Initial Capital: $100,000
- Position Size: 20% of capital per trade
- Transaction Cost: 0.1%
- Long-only mean-reversion regime logic
- Benchmark: Buy & Hold

---

## 📈 Results (Test Period)

| Metric | Strategy | Benchmark |
|--------|----------|------------|
| Annualized Return | 6.91% | 23.18% |
| Sharpe Ratio | **1.78** | 0.96 |
| Max Drawdown | **-3.35%** | Higher |

✔ Superior risk-adjusted performance  
✔ Low drawdown  
✔ Stable equity curve  

The strategy prioritizes capital preservation and volatility control over aggressive trend capture.

---

## 📂 Project Structure
transformer-trading-strategy/
│
├── data/
├── src/
├── results/
│ ├── equity_curve.png
│ ├── signals_plot.png
│ └── training_curve.png
├── README.md
└── .gitignore

---

## ⚙️ Tech Stack

- MATLAB R2025a
- Deep Learning Toolbox
- GPU acceleration
- Financial time-series modeling

---

## 🚀 Future Improvements

- Walk-forward retraining
- Long-short extension
- Dynamic position sizing
- Multi-asset portfolio testing
- Python/PyTorch implementation

---

## 📌 Disclaimer

This project is for research and educational purposes only.  
It does not constitute financial advice.
