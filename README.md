# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes how trader performance varies across different Bitcoin market sentiment regimes
using historical Hyperliquid trading data and the Bitcoin Fear & Greed Index.

The goal is to uncover:
- How sentiment impacts trader profitability and risk
- Which traders perform well during Fear or Greed regimes
- Contrarian traders who profit when market sentiment is negative
- Traders who remain consistent across different market conditions

---

## Datasets Used
1. **Historical Trader Data (Hyperliquid)**
   - Trade-level execution data including trader identifier, timestamp, and realized PnL

2. **Bitcoin Fear & Greed Index**
   - Daily market sentiment data classified as Extreme Fear, Fear, Neutral, Greed, or Extreme Greed

---

## Methodology
1. Parsed and normalized timestamps from raw trade and sentiment data
2. Aggregated trader performance on a daily basis
3. Merged daily trader PnL with market sentiment
4. Grouped sentiment into three regimes:
   - **Fear** (Extreme Fear + Fear)
   - **Greed** (Greed + Extreme Greed)
   - **Neutral**
5. Computed performance metrics:
   - Total PnL
   - Average daily PnL
   - Win rate
   - Sharpe ratio
   - Maximum drawdown
6. Ranked traders by performance under different sentiment regimes
7. Visualized performance distributions to compare volatility across regimes

---

## Key Insights
- Trader PnL dispersion is highest during **Fear** regimes, indicating elevated risk and opportunity
- **Greed** regimes amplify both gains and losses, suggesting aggressive positioning
- **Neutral** regimes show lower volatility and more stable outcomes
- A subset of traders consistently generates profits during Fear, indicating **contrarian strength**
- Win rate alone is insufficient; combining PnL and Sharpe ratio provides better trader evaluation

---

## Visualizations
- Distribution of daily trader PnL across Fear, Greed, and Neutral regimes
- Ranked lists of top traders by sentiment regime
- Identification of contrarian and consistent traders

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

## Conclusion
Market sentiment plays a critical role in trader performance. Incorporating sentiment-aware
analysis enables better identification of high-performing, contrarian, and consistent traders,
supporting smarter trading strategy decisions.
