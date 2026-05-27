# TFEX Trading Strategy (S501!) with Trend + Momentum + Sideway Strategy

## Objective

Create a TFEX trading system that selects strategy suitable for market conditions by using Trend analysis technique first, then choosing order entry at smaller Timeframe appropriately.

---

## Step 1: Trend Analysis on H4 Timeframe

Use 3 EMA lines to indicate trend:
- EMA(9)
- EMA(21)
- EMA(55)

### How to Read Trend:

| EMA Arrangement Condition | Meaning |
|--------------------------|---------|
| EMA(9) > EMA(21) > EMA(55) | Uptrend |
| EMA(9) < EMA(21) < EMA(55) | Downtrend |
| Mixed or close together | Sideway / No clear trend |

---

## Step 2: Enter Trade on M15 Timeframe According to Identified Trend

### Case 2.1: When there is Trend (Uptrend or Downtrend)

**Strategy: EMA Crossover (9, 21) on M15**

- Trade when H1 chart shows trend signal (from 3-line EMA)
- Wait for EMA(9) to cross EMA(21) on M15 TF to enter order according to trend

### Example:
- H1 is uptrend → Enter Buy on M15 when EMA9 crosses EMA21 up
- H1 is downtrend → Enter Sell on M15 when EMA9 crosses EMA21 down

---

### Case 2.2: When it's Sideway

**Strategy: Bollinger Band + RSI**

Use range trading when there's no clear trend.

#### Trade Entry Conditions:
- **Sell** → When price touches Upper Bollinger Band and RSI > 70
- **Buy** → When price touches Lower Bollinger Band and RSI < 30
- **SL**: 5% of portfolio at the middle line

#### Timeframe Used: M15

---

This system is designed to suit the TFEX market with high volatility and can be used for both morning and afternoon sessions.
