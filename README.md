# Trader Performance vs Market Sentiment Analysis

## Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear & Greed Index) and trader performance on Hyperliquid. The objective is to identify behavioral patterns across different market sentiment regimes and derive actionable trading strategies.

---

## Dataset Description

### 1. Bitcoin Fear & Greed Index

Columns:

* Date
* Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)
* Sentiment Value

### 2. Hyperliquid Historical Trader Data

Key fields:

* Account
* Symbol
* Execution Price
* Side
* Size USD
* Closed PnL
* Fee
* Timestamp

---

## Methodology

### Data Preparation

1. Loaded both datasets using Pandas.
2. Checked for missing values and duplicate records.
3. Converted timestamps into a daily date format.
4. Merged trader activity with Fear & Greed sentiment using the trading date.

### Feature Engineering

The following metrics were created:

* Daily Profit & Loss (PnL)
* Trade Count
* Average Trade Size
* Win Rate
* Trader Activity Level
* Sentiment Classification
* Trader Performance Segments

### Analysis Performed

#### Performance Analysis

* Average PnL by sentiment regime
* Total profitability by sentiment regime
* Win rate comparison across sentiment categories

#### Behavioral Analysis

* Trading frequency during Fear vs Greed periods
* Average trade size by sentiment
* Risk-taking behavior comparison

#### Trader Segmentation

Traders were segmented into:

* High Activity Traders
* Medium Activity Traders
* Low Activity Traders

Additional clustering was performed to identify behavioral archetypes.

---

## Key Insights

### Insight 1: Extreme Greed Produced the Highest Profitability

Average trader profitability was highest during Extreme Greed periods. Traders generally captured stronger market trends and generated larger positive PnL values.

### Insight 2: Market Sentiment Influences Trading Behavior

Trade frequency and average position sizes changed significantly across sentiment regimes. Traders tended to take larger positions during Greed periods and became more defensive during Fear periods.

### Insight 3: High Activity Traders Outperformed Others

Highly active traders consistently generated higher cumulative profits and demonstrated better performance stability than low-activity participants.

### Insight 4: Win Rates Vary Across Sentiment Regimes

Winning percentages were generally stronger during Greed periods, indicating that bullish market conditions provided more favorable trading opportunities.

### Insight 5: Distinct Trader Archetypes Exist

Clustering analysis revealed groups of:

* High-frequency profitable traders
* Low-frequency conservative traders
* High-risk inconsistent traders

These groups respond differently to market sentiment.

---

## Strategy Recommendations

### Strategy 1: Sentiment-Aware Position Sizing

Increase exposure during Greed and Extreme Greed periods while maintaining predefined risk limits.

**Rule:** Increase position size by 10–20% during strong bullish sentiment.

### Strategy 2: Defensive Risk Management During Fear

Reduce leverage and position size during Fear and Extreme Fear periods.

**Rule:** Lower exposure when sentiment falls below the Fear threshold.

### Strategy 3: Follow High-Performing Trader Cohorts

Monitor the behavior of consistently profitable high-activity traders and use their activity as a confirmation signal.

### Strategy 4: Dynamic Risk Allocation

Allocate more capital to trend-following strategies during Greed periods and shift toward capital preservation during Fear periods.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* SciPy

---

## How to Run

1. Clone the repository

```bash
git clone <repository-url>
cd trader-sentiment-analysis
```

2. Install dependencies

```bash
pip install pandas numpy matplotlib scikit-learn scipy
```

3. Place datasets inside the project directory

```text
historical_data.csv
fear_greed_index.csv
```

4. Run the notebook

```bash
jupyter notebook
```

Open:

```text
ASSGNMENT.ipynb
```

and execute all cells.

---

## Conclusion

The analysis demonstrates that market sentiment has a measurable impact on trader profitability and behavior. Greed-driven markets tend to generate stronger trader performance, while Fear regimes encourage defensive behavior. Incorporating sentiment into risk management and position sizing can improve decision-making and trading outcomes.
