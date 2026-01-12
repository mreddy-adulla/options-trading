# ARCHITECTURE
## Bank Nifty Put-Sell System

This document explains **how the system is structured**, how data flows, and why each layer exists.

---

## 1. Architectural Principles

- Same logic for backtest, paper, and live
- Loose coupling between modules
- Risk evaluation before execution
- Explainability over black-box optimization

---

## 2. High-Level Flow

```
Market Data
   ↓
Feature Extraction
   ↓
Scoring Engine (0–100)
   ↓
Option Scanner
   ↓
Entry Rules
   ↓
Risk Engine (POE, DD)
   ↓
Exit Engine
   ↓
Execution Layer
   ↓
Metrics & Dashboard
```

---

## 3. Layer Responsibilities

### Data Layer
- Fetches spot, futures, options, VIX
- Normalizes timestamps
- Produces immutable market snapshots

### Scoring Layer
- Converts multi-factor signals into a single quality score
- Modular and interpretable

### Strategy Layer
- Entry & exit rules
- No market data fetching
- No broker calls

### Risk Layer
- Probability of expiry
- Expected move
- Monte Carlo drawdown

### Execution Layer
- Broker abstraction
- Paper and live trading use identical logic

---

## 4. Why This Architecture Works

- Prevents overfitting
- Enables safe iteration
- Allows audit & debugging
- Scales capital without logic changes

---

## 5. Extension Points

- Swap scoring logic
- Add new brokers
- Plug AI models
- Add new indices

---

End of ARCHITECTURE.md

