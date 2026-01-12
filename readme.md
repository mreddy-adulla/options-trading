# Bank Nifty Put-Sell System

A **production-grade, systematic options trading framework** for selling Bank Nifty puts using a **scoring-based, risk-first architecture**.

This repository is designed to be:
- Deterministic (rule-based, explainable)
- Scalable (backtest → paper → live)
- Auditable (clear risk & compliance boundaries)

---

## 🎯 Strategy Summary

- Instrument: Bank Nifty weekly options
- Core Trade: Short Put (preferably hedged)
- Edge Sources:
  - Time decay (theta)
  - Volatility risk premium
  - Structural support & OI
- Philosophy: **High probability, controlled drawdowns**

---

## 🧱 System Capabilities

✔ Put-sell scoring model (0–100)  
✔ Fully automated option scanner  
✔ Rule-based entry & exit engine  
✔ 5-year backtesting ready  
✔ Paper trading (Zerodha / Upstox adapters)  
✔ Risk & probability simulation  
✔ Dashboard (PnL, Greeks, Risk)  
✔ AI-ready adaptive scoring (optional)

---

## 📁 Repository Structure

```
bn_put_sell/
├── config/        # Strategy & risk configuration
├── data/          # Market & option data loaders
├── greeks/        # Black–Scholes & IV solvers
├── scoring/       # 0–100 trade scoring engine
├── scanner/       # Put strike scanner
├── strategy/      # Entry / exit logic
├── risk/          # Probability & drawdown models
├── backtest/      # Event-driven backtester
├── papertrade/    # Broker adapters
├── dashboard/     # Streamlit UI
├── ai/            # Adaptive scoring (optional)
└── main.py        # System entry point
```

---

## 🚀 Quick Start

```bash
pip install -r requirements.txt
python main.py
streamlit run dashboard/streamlit_app.py
```

---

## 🧠 Intended Users

- Serious retail traders
- Prop-style individual traders
- Quant-curious discretionary traders

⚠️ This is **not** a beginner strategy.

---

## 📜 Disclaimer

This software is provided for **research and educational purposes only**. Trading options involves substantial risk.

See `COMPLIANCE_AND_RISK.md` before any live deployment.

