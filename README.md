# Analyzing Trader Behavior and Market Sentiment

## **Summary of Tasks**
Analyzed historical trading data, sentiment data (Fear-Greed index), and applied:
* Exploratory Data Analysis (EDA)
* Trader profiling and ranking
* Sentiment-wise trader performance
* Correlation and statistical testing
* Clustering with KMeans
* Regression modeling with Random Forest

## Key Analyses and Observations

### 1. **Trader Behavior vs Market Sentiment**

* Boxplots show:
  * PnL is higher in Greed and lower in Fear periods.
  * Trading volume spikes during Greed.
  * Fees paid are also higher in Greed phases (suggesting higher activity).

### 2. **Top & Bottom Traders**
* Identified:
  * Top 10 overall traders by total PnL.
  * Bottom 10 overall traders by total PnL.
  * Top/Bottom 5 traders per sentiment (Fear, Neutral, Greed).
* Traders consistently ranked across all sentiments indicate resilience and skill, while those with large PnL swings are sentiment-sensitive.

### 3. **Trader-Sentiment Correlation**
* Pearson correlation:
  * Fear-Greed Value ↔ PnL correlation is positive, indicating higher sentiment leads to higher PnL.
  * Sentiment drives trader profitability, statistically verified.

### 4. **T-Test Results**
* p-value < 0.05:
  * Statistically significant difference in trader PnL between Fear and Greed.
  * Implication: Traders perform differently depending on market sentiment.

### 5. **Clustering (KMeans)**
* Traders grouped into 3 clusters based on:
  * Avg. PnL
  * Volume
  * Fee
  * Active Days
* Each cluster showed distinct behavior:
  * Cluster 0: Consistent high performers.
  * Cluster 1: Average consistent traders.
  * Cluster 2: Low or erratic performers.

### 6. **Trader Preference: Fear vs Greed**

* Some traders excelled in Fear, indicating contrarian or risk-seeking behavior.
* Others thrived in Greed, suggesting momentum or trend-following strategies.
* Useful for tailoring market roles based on individual edge.

### 7. **Random Forest Regression**
* Feature: Fear-Greed Index
* Target: Total PnL
* Best R² ≈ moderate on train/test sets.
* Indicates: Sentiment alone isn't a strong predictor of PnL — other features likely needed (e.g., entry/exit timing, strategy, leverage).
  
## Insights

### 1. Market Sentiment = Trader Participation
* During "Greed", more unique traders are active.
* Fearful markets may filter out weak hands — likely only experienced or risk-tolerant traders remain.

### 2. Fee-to-Volume Ratio
* Some losing traders paid disproportionate fees, indicating overtrading or poor risk-reward setups.

### 3. Trader Style Evolution
* Many top traders shift performance across sentiments (shown in Fear_minus_Greed pivot table).
* These traders may adapt their strategy based on market mood — potential future mentors or leads for strategy optimization.

## Inferences & Decision-Making
1. Segment traders using KMeans clusters for personalize features, UI, or margin levels.
2. Promote Greed-phase campaigns for higher engagement.
3. Monitor high-fee/low-pnl traders to provide training or limits to avoid churn.
4. Use sentiment-PnL relationship to design predictive alerts.
5. Top fear-phase performers are potential hedging specialists.

## Final Take:
This project demonstrates real-world trading analytics using Python, EDA, clustering, and ML.
