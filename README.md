# Bitcoin Market Sentiment vs Trader Performance Analysis

## Project Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear & Greed Index) and trader performance using Hyperliquid historical trading data.

The goal is to understand whether market sentiment influences trader profitability, trading behavior, and overall performance.

---

## Dataset Information

### 1. Bitcoin Fear & Greed Index
Contains daily market sentiment labels:

- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

### 2. Hyperliquid Historical Trader Data

Contains:

- Account
- Coin
- Execution Price
- Size USD
- Side (BUY/SELL)
- Closed PnL
- Fee
- Timestamp
- Position Information

Total Records Analyzed:

- 211,224 Trades
- 2,644 Sentiment Records

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Google Colab

---

## Data Processing

### Data Cleaning

- Checked missing values
- Converted timestamps into datetime format
- Extracted trading date
- Merged trader data with sentiment data using date

### Feature Engineering

Created:

- Profit/Loss Indicator
- Sentiment Score Mapping
- Trader Segmentation Groups
- Daily PnL Trends

---

## Analysis Performed

### 1. Market Sentiment Distribution

Analyzed how trades were distributed across:

- Fear
- Extreme Fear
- Neutral
- Greed
- Extreme Greed

---

### 2. Average PnL Analysis

Calculated average trader profitability for each sentiment category.

Result:

| Sentiment | Avg PnL |
|------------|------------|
| Extreme Fear | 34.54 |
| Fear | 54.29 |
| Neutral | 34.31 |
| Greed | 42.74 |
| Extreme Greed | 67.89 |

Observation:

Extreme Greed generated the highest average profitability.

---

### 3. Win Rate Analysis

Calculated percentage of profitable trades.

| Sentiment | Win Rate |
|------------|------------|
| Extreme Fear | 37.06% |
| Fear | 42.08% |
| Neutral | 39.70% |
| Greed | 38.48% |
| Extreme Greed | 46.49% |

Observation:

Extreme Greed showed the highest winning percentage.

---

### 4. Position Size Analysis

Compared average trade sizes across market sentiments.

Observation:

Fear periods showed the largest average position sizes, indicating traders may take larger risks during uncertain market conditions.

---

### 5. Buy vs Sell Behavior

Performed sentiment-wise BUY and SELL analysis using cross-tabulation and heatmaps.

Observation:

Trading activity remained relatively balanced between BUY and SELL orders across sentiments.

---

### 6. Top Trader Analysis

Identified the Top 20 most profitable traders based on cumulative Closed PnL.

Observation:

A small number of traders generated significantly higher profits than the majority.

---

### 7. Statistical Hypothesis Testing

Performed Independent T-Test between Fear and Greed sentiment groups.

Result:

```text
P-value = 0.3231
```

Conclusion:

No statistically significant difference was found between Fear and Greed profitability at a 95% confidence level.

---

### 8. Correlation Analysis

Mapped sentiments to numerical scores:

```text
Extreme Fear = 1
Fear = 2
Neutral = 3
Greed = 4
Extreme Greed = 5
```

Result:

```text
Correlation = 0.00597
```

Conclusion:

Market sentiment alone has almost no direct linear relationship with trader profitability.

---

### 9. Trader Segmentation

Traders were grouped into:

- Top Traders (Top 10%)
- Average Traders
- Bottom Traders (Bottom 10%)

Observation:

Top traders consistently outperformed other groups across nearly all sentiment categories.

Extreme Greed produced exceptionally high returns for Top Traders.

---

### 10. PnL Distribution Analysis

Visualized profit distributions using:

- Box Plots
- Violin Plots

Observation:

Profit distributions contain significant outliers, indicating the presence of highly profitable and highly unprofitable trades.

---

## Key Findings

- Extreme Greed generated the highest profitability.
- Extreme Greed produced the highest win rate.
- Fear sentiment resulted in larger average position sizes.
- Sentiment and profitability showed almost zero correlation.
- Top traders consistently outperformed average and bottom traders.
- Statistical testing showed sentiment alone is not a significant predictor of profitability.

---

## Conclusion

Market sentiment affects trading behavior and profitability patterns, but it is not a strong standalone predictor of trading success.

Trader skill, position sizing, risk management, and execution strategy appear to have a greater impact on profitability than sentiment alone.

---

## Repository Structure

```

primetrade-bitcoin-sentiment-analysis/

├── data/
│ ├── historical_data.csv
│ └── fear_greed_index.csv

├── notebook/
│ └── Primetrade_Assignment.ipynb

├── report/
│ └── Primetrade_Report.pdf

└── README.md

```
