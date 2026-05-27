# TFEX with Open Interest

This project was created to study and develop a TFEX trading strategy using the concept of Open Interest that correlates with price behavior.

---

## Initial Concept

In this project, we define an "Open Interest line" as a price level that is divisible by 25, such as: 525, 550, 575.

---

## Study Steps

### 1. Research & Data Analysis

- Analyze the relationship between price behavior and OI (Open Interest Level)
- Measure statistics such as:
  - Frequency of Breakout at OI line
  - Frequency of Reversal occurrences
  - Calculate as percentage to find pattern reliability

> Example:
> Price breaks through OI level then reverses in 32% of all cases (see in research.pine file)

---

### 2. Strategy Development (Pine Script)

- Develop automated trading strategy with Pine Script
- Use OI level as support/resistance for order entry decisions
- Analyze results through Backtest such as:
  - Win rate
  - Max Drawdown
  - Sharpe Ratio

---

### 3. Order Entry

- Identify when reversal or breakout occurs
- Once identified, use strategy as follows:

For reversal trades:
- Find price action candles (bullish/bearish engulfing)
- Or use RSI / volume together
- Risk/Reward ratio 2:1

For breakout trades:
- Don't enter immediately, wait for pullback back to previous resistance
- Set buy/sell at the previous line
- Risk/Reward ratio 2:1