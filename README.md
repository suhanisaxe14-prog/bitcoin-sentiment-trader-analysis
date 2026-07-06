# Bitcoin Trader Behavior vs. Market Sentiment Analysis


## Overview
This analysis explores how trader performance and behavior shift across different
market sentiment regimes, using the Bitcoin Fear & Greed Index as the sentiment
signal and a historical trading dataset as the performance signal.

## Approach
1. Parsed and merged historical trade data with the daily Fear & Greed Index by date.
2. Categorized each trade into one of five sentiment classes: Extreme Fear, Fear,
   Neutral, Greed, Extreme Greed.
3. Computed, per sentiment class:
   - Total trades, total volume (USD), average trade size
   - Total and average PnL (including closed-trade-only metrics)
   - Win rate (% of profitable trades)
   - Buy vs. Sell distribution
   - Liquidation rate
   - Average trade size per account across sentiment regimes
4. Visualized win rate, average PnL, trading volume, and buy/sell split across
   sentiment categories in a single 4-panel chart.

## Key Findings
- **Win rate peaks during Extreme Greed** (89.17% on closed trades) and stays
  strong during Fear (87.29%) — both outperforming Neutral markets (82.39%).
- **Average PnL per closed trade** is highest during Extreme Greed (₹130.21),
  suggesting more decisive, higher-conviction trades in strongly bullish sentiment.
- Traders show a **modest sell-side bias during Extreme Greed** (55.1% sell vs.
  44.9% buy) — potentially profit-taking behavior at sentiment extremes.
- Overall, trades placed during emotionally *extreme* markets (Fear or Greed)
  tend to outperform trades placed during Neutral conditions — a counterintuitive
  but consistent pattern across the dataset.

## Files
- `analysis.ipynb` — full notebook with code, outputs, and inline charts
- `analysis.html` — rendered version of the notebook, viewable in any browser
- `summary_by_sentiment.csv` — full trade summary by sentiment class
- `closed_summary_by_sentiment.csv` — closed-trade-only performance summary
- `side_distribution.csv` — buy/sell distribution by sentiment
- `sentiment_analysis_charts.png` — 4-panel summary visualization

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn

## Author
Suhani
