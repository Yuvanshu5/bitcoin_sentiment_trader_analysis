Bitcoin Market Sentiment vs Trader Performance Analysis

A data analysis project exploring the relationship between Bitcoin market sentiment (Fear & Greed Index) and trader performance metrics using Python, Pandas, and visualization libraries.

Project Overview

This project analyzes how market sentiment impacts trading behavior and profitability.
By combining historical trader data with the Bitcoin Fear & Greed Index, the analysis uncovers trends in:

Trader profitability under different market sentiments
Position sizing behavior
Sentiment-driven market dynamics
Time-series performance variations

The project also includes automated exploratory data analysis (EDA) reports generated using ydata-profiling.

Dataset Information
1. Fear & Greed Index Dataset

Contains Bitcoin market sentiment classifications such as:

Extreme Fear
Fear
Neutral
Greed
Extreme Greed
Main Columns
date
classification
2. Historical Trader Dataset

Contains historical trader execution and performance information.

Main Columns
account
coin
execution_price
size_tokens
size_usd
side
timestamp_ist
closed_pnl
transaction_hash
order_id
fee
trade_id
date
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
YData Profiling
Project Workflow
1. Data Loading
Import sentiment and trader datasets using Pandas.
2. Data Cleaning
Standardize column names
Convert timestamps into datetime format
Handle missing values
3. Exploratory Data Analysis (EDA)

Generated profiling reports using ydata-profiling:

sentiment_profile.html
trader_profile.html
4. Data Merging

Merged trader data with sentiment data on the date column.

5. Performance Analysis

Analyzed:

Average profit/loss (closed_pnl)
Position size (size_usd)
Sentiment-wise trading behavior
6. Visualization

Created:

Boxplots
Line charts
Bar charts
Key Insights
Trader profitability changes significantly across sentiment categories.
Market greed periods often show larger trade sizes.
Fear-driven markets display higher volatility in profit/loss distributions.
Sentiment can act as a useful contextual indicator for trading analysis.
Visualizations Included
Distribution Analysis
Closed PnL Distribution by Sentiment
Position Size Distribution by Sentiment
Time-Series Analysis
Average Closed PnL Over Time by Market Sentiment
Comparative Analysis
Mean Trade Size by Sentiment
Project Structure
├── bitcoin_sentiment_trader_analysis.ipynb
├── fear_greed_index.csv
├── historical_data.csv
├── sentiment_profile.html
├── trader_profile.html
└── README.md
Installation

Clone the repository:

git clone https://github.com/Yuvanshu5/bitcoin_sentiment_trader_analysis
cd bitcoin-sentiment-analysis

Install dependencies:

pip install pandas numpy matplotlib seaborn ydata-profiling
Usage

Run the Jupyter Notebook:

jupyter notebook bitcoin_sentiment_trader_analysis.ipynb

Or execute the profiling script directly.

Sample Code
merged_df = pd.merge(
    trader_df,
    sentiment_df[['date', 'classification']],
    on='date',
    how='left'
)
Future Improvements
Add predictive machine learning models
Perform correlation analysis
Integrate live crypto market APIs
Add trader clustering and behavior segmentation
Build an interactive dashboard using Streamlit or Power BI
