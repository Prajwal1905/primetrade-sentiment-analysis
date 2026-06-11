# Trader Performance vs Bitcoin Market Sentiment

Analysis of 211k+ Hyperliquid trade executions against the Bitcoin Fear & Greed Index
to find how market sentiment relates to trader profitability and behavior.

## Datasets
- `fear_greed_index.csv` — daily Bitcoin Fear & Greed Index (included in repo)
  - Source: https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing
- `historical_data.csv` — Hyperliquid trade history (47MB, not included in repo due to size)
  - Download: https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing
  
## Key Findings
1. **Sentiment extremes beat calm markets** — best avg PnL per trade in Extreme Greed (~$130)
   and Fear (~$113), with 87-89% win rates vs ~$71 on Neutral days.
2. **The profitable side flips with sentiment** — shorts earned 2.5x more than longs during
   Fear ($208 vs $83 per close); longs beat shorts during Greed.
3. **Winners sell euphoria, losers buy it** — top-5 accounts' buy ratio drops to 0.41 in Greed,
   while bottom-5 accounts buy 65% of the time in Greed and sell into Fear.
4. **Traders size 2.5x bigger into Fear** (~$7.8k avg) than Extreme Greed (~$3.1k).
5. **Days after Extreme Fear averaged ~5x more profit** than post-Greed days (small sample: 14 days).

## How to Run
1. Download `historical_data.csv` from the link above into the project folder
2. `pip install pandas matplotlib seaborn jupyter`
3. Open `analysis.ipynb` and Run All

## Tools
Python, pandas, matplotlib, seaborn