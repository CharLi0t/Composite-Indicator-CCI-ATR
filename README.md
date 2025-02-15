# Composite Indicator (CCI + ATR)

The **Composite Indicator (CCI + ATR)** combines the **Commodity Channel Index (CCI)** with the **Average True Range (ATR)**, providing traders with a dynamic tool for identifying entry and exit points based on momentum and volatility. This indicator is particularly useful for markets like cryptocurrencies, which often exhibit sharp sell-offs and gradual upward trends.

---

## Key Features

### 1. Momentum Analysis with CCI
The CCI calculates price momentum by comparing the current price level to its average over a specific period. The indicator generates signals when CCI crosses predefined thresholds.

- **Buy Signal**: Triggered when CCI crosses above the lower threshold (e.g., -100).
- **Sell Signal**: Triggered when CCI crosses below the upper threshold (e.g., +100).

### 2. Volatility Filtering with ATR
The ATR measures market volatility, ensuring signals occur only during significant price movements.

- Separate multipliers for buy and sell signals allow tailored filtering based on market behavior.

### 3. Stop Loss Calculation
Dynamic stop loss levels are calculated using the ATR multiplier to adapt to market volatility, offering better risk management.

---

## How It Works

### CCI Calculation
The CCI is calculated using the typical price `((High + Low + Close) / 3)` and a user-defined length. It detects momentum changes by measuring deviations from the average price.

### ATR Calculation
The ATR determines the average price range over a specified period, identifying the market’s volatility. The ATR SMA acts as a baseline to filter signals.

### Buy Signal
A buy signal is triggered when:
- CCI crosses above the lower threshold (e.g., -100).
- ATR exceeds its SMA multiplied by the buy multiplier (e.g., 1.0).

### Sell Signal
A sell signal is triggered when:
- CCI crosses below the upper threshold (e.g., +100).
- ATR exceeds its SMA multiplied by the sell multiplier (e.g., 0.95).

### Stop Loss Integration
- **Long positions**: Stop loss = Low – (ATR * ATR Multiplier)
- **Short positions**: Stop loss = High + (ATR * ATR Multiplier)

---

## Advantages
- Combines momentum (CCI) and volatility (ATR) for precise signal generation.
- Customizable thresholds and multipliers for different market conditions.
- Dynamic stop loss ensures better risk management in volatile markets.

---

## Suggested Parameter Settings

### CCI Length
- **Default**: 20
- **Adjustments**:
  - **10–15**: Shorter timeframes (e.g., 5-15 minutes).
  - **20**: General use for 1-hour timeframes.
  - **30–50**: Longer timeframes (e.g., 4-hour or daily charts).

### CCI Threshold
- **Default**: 100
- **Adjustments**:
  - **50–75**: For more frequent signals in ranging markets.
  - **100**: Balanced for most trading conditions.
  - **150–200**: For strong trends to reduce noise.

### ATR Length
- **Default**: 14
- **Adjustments**:
  - **10–14**: For assets with moderate volatility.
  - **20**: For assets with lower volatility.

### ATR Buy Multiplier
- **Default**: 1.0
- **Adjustments**:
  - **0.9–1.0**: For gradual uptrends in crypto markets.
  - **1.1–1.2**: For stronger trend filtering.

### ATR Sell Multiplier
- **Default**: 0.95
- **Adjustments**:
  - **0.8–0.95**: For sharp sell-offs.
  - **1.0–1.1**: For stable downward trends.

### ATR Multiplier (Stop Loss)
- **Default**: 1.5
- **Adjustments**:
  - **1.0–1.2**: For shorter timeframes or less volatile markets.
  - **2.0–2.5**: For highly volatile markets like cryptocurrencies.

---

## Example Use Cases

### Scalping (5-15 minute charts)
- **CCI Length**: 10
- **CCI Threshold**: 75
- **ATR Buy Multiplier**: 0.9
- **ATR Sell Multiplier**: 0.8

### Day Trading (1-hour charts)
- **CCI Length**: 20
- **CCI Threshold**: 100
- **ATR Buy Multiplier**: 1.0
- **ATR Sell Multiplier**: 0.95

### Swing Trading (4-hour or daily charts)
- **CCI Length**: 30
- **CCI Threshold**: 150
- **ATR Buy Multiplier**: 1.2
- **ATR Sell Multiplier**: 1.0

---

## Final Thoughts
The **Composite Indicator (CCI + ATR)** is a versatile tool designed to enhance trading decisions by combining momentum analysis with volatility filtering. Whether scalping or swing trading, this indicator provides actionable insights and robust risk management to navigate complex markets effectively.
