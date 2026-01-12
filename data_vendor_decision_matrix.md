# Data Vendor Decision Matrix

Choose your data source based on **budget, reliability, and intended use**.

---

## 1. Budget: ₹0 – ₹5,000 / year

| Source | Data | Use Case | Verdict |
|------|-----|---------|--------|
| NSE website | Option chain | Live scan | ❌ Unstable |
| NSE bhavcopy | EOD options | Learning | ⚠️ Limited |
| Investing.com | Events | Calendar | ⚠️ Scraping |

**Recommendation**: Education only. Not suitable for serious backtests.

---

## 2. Budget: ₹5,000 – ₹25,000 / year

| Source | Data | Use Case | Verdict |
|------|-----|---------|--------|
| Upstox API | Live + historical | Paper trading | ✅ Acceptable |
| Angel One API | Live | Execution | ⚠️ Partial |

**Recommendation**: Paper trading + limited backtest.

---

## 3. Budget: ₹25,000 – ₹50,000 / year (Recommended)

| Vendor | Coverage | Strength |
|------|--------|---------|
| Global Datafeeds | Intraday options | Reliable |
| TrueData | Tick + options | High accuracy |

**Recommendation**: Minimum viable professional setup.

---

## 4. Budget: ₹50,000+ / year

| Vendor | Coverage | Strength |
|------|--------|---------|
| Custom feeds | Full stack | Institutional |

**Recommendation**: Required for capital scaling.

---

## Decision Rule

> If you cannot afford quality data, you cannot afford options trading.

End of matrix.

