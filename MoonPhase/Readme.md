# Moon Phase with EMA Cross Strategy (TFEX)

This folder is a project to study and develop a TFEX trading strategy based on Moon Phase combined with EMA Crossover technique for entry and exit signals.

---

## Initial Concept

We started from the assumption that:

> If it's a waxing moon, the market tends to move DOWN
> If it's a waning moon, the market tends to move UP

This will be proven through backtesting.

---

## Hypothesis Verification

You can view the backtest results and analysis of this hypothesis in the file:

`prove.ipynb`

Which uses Python to:

- Retrieve TFEX data
- Calculate daily moon phase
- Divide data into waxing and waning periods
- Calculate average returns in each period
- Display the percentage of market movement in each phase

---

## Strategy in Pine Script (for TradingView)

This strategy is written in the file:

`assignment4_ver2.pine`

### Entry Rules

#### Buy (Long Entry)
- When in waning period or after waxing for 15 days
- And an EMA cross up occurs using:
  - Short EMA: 15
  - Long EMA: 50 in 15 mins timeframe

#### Sell (Short Entry)
- When in waxing period
- And an EMA cross down occurs (15 crosses below 50)

### Exit Rules
- Close all orders immediately when Moon Phase changes (from waxing to waning or vice versa)
- Or close position on opposite EMA crossover direction

---

## Example Results

You can view the strategy behavior and trading signals directly from the TradingView chart.

---

## Suggestions for Further Development

- Test with other timeframes such as 1H, 1D
- Add stop loss / take profit
- Use machine learning to discover additional patterns

---

## Author

Sirawitch Chairuangsirikul  

