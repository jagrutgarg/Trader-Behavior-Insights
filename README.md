# Project Overview

This project analyzes trader behavior by combining:

- Bitcoin Market Sentiment (Fear & Greed Index)

- Historical Trader Data (Hyperliquid)

The objective is to understand how market sentiment influences trader performance, risk-taking behavior, and trading patterns, and to translate those insights into actionable strategy rules.


# Objectives

- Analyze trader performance across Fear vs Greed market regimes

- Identify behavioral segments among traders

- Evaluate differences in leverage, trade frequency, and win rate

- Propose actionable risk-control strategies

- Build a simple predictive model (Bonus)

- Cluster traders into behavioral archetypes (Bonus)

- Create a lightweight Streamlit dashboard (Bonus)

# Dataset Instructions

The datasets are included in this repository in ZIP format:

- fear_greed_index.zip

- historical_data.zip

## How to Run the Notebook

Download both ZIP files from this repository.

Keep them in the same directory as the notebook.

Run the notebook from top to bottom.

The notebook contains automatic:

- Unzipping logic

- Data loading

- Merging

- Feature engineering

No manual extraction is required.


## Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repo-link>
cd Trader-Behavior-Insights
```
### 2. Install Dependencies

```bash
pip install -r requirements.txt
```
### 3. Open and Run the notebook but run all cells sequentially.

## Part A — Data Preparation

- Loaded both datasets

- Documented:

- - Number of rows and columns

- - Missing values

- - Duplicate records

- Converted timestamps to daily level

- Merged datasets by date

- Created key performance metrics:

- - Daily PnL per trader

- - Win rate

- - Average trade size

- - Leverage distribution

- - Number of trades per day

- - Long/Short ratio

## Part B — Analysis

### Key Questions Answered

- Does performance differ between Fear and Greed days?

- Do traders change behavior based on sentiment?

- Can traders be segmented into meaningful behavioral groups?

### Segmentation Implemented

- High vs Low Leverage traders

- Frequent vs Infrequent traders

- Consistent vs Inconsistent traders

### Key Insights

- Leverage usage increases during Greed regimes.

- Drawdowns are amplified during Fear periods.

- High-leverage inconsistent traders contribute disproportionately to downside risk.

- Sentiment significantly influences trade frequency and risk exposure.

All insights are supported by tables and visualizations in the notebook.

## Part C — Actionable Output

Two strategy frameworks were implemented and simulated.

### 🔹 Strategy 1 — Sentiment-Based Leverage Control

#### Rule:

- During Fear:

- - Reduce leverage by 30% for High-Leverage or Inconsistent traders.

- During Greed:

- - Allow leverage expansion only for Consistent traders.

#### Impact:

- Reduced drawdown volatility

- Improved risk stability

- Controlled sentiment-driven overexposure

###🔹 Strategy 2 — Behavioral Risk Tiering

#### Defined a high-risk segment:

- High leverage

- Low consistency

#### Controls Applied:

- 40% leverage reduction

- Risk-tier tagging

- Performance comparison before vs after implementation

Result: Improved downside protection without significantly suppressing average returns.

## Bonus Section
### 1️⃣ Predictive Model

Built an interpretable Logistic Regression model to predict:

Next-day trader profitability

Features used:

- Average leverage

- Trade frequency

- Win rate

- Trade size

- Sentiment value

- Long/Short ratio

Model interpretation includes coefficient analysis.

### 2️⃣ Trader Clustering

Applied KMeans clustering to identify behavioral archetypes:

- Conservative traders

- High-risk traders

- Opportunistic traders

Cluster profiles were analyzed and visualized.

### 3️⃣ Streamlit Dashboard (Optional)

An interactive dashboard (app.py) allows exploration of:

- Sentiment distribution

- Average PnL by regime

- Leverage behavior

- Top traders

## Requirements

pandas

numpy

matplotlib

seaborn

scikit-learn

streamlit

Install using:
```bash
pip install -r requirements.txt
```

## 🧠 Executive Summary

The analysis demonstrates that trader behavior is sentiment-sensitive, particularly in leverage usage and trade frequency.

Key findings:

- Risk expansion during Greed does not proportionally improve profitability.

- High-leverage inconsistent traders drive large drawdowns.

- Sentiment-aware risk controls improve stability without eliminating upside potential.

The proposed strategies are:

- Data-driven

- Operationally implementable

- Suitable for automated risk systems

## 📈 Skills Demonstrated

- Data cleaning and preparation

- Time-series alignment

- Feature engineering

- Behavioral segmentation

- Statistical analysis

- Strategy simulation

- Predictive modeling

- Clustering

- Dashboard development

## 👤 Author

### Jagrut Garg
Data Analysis | Behavioral Analytics | Risk Insights
