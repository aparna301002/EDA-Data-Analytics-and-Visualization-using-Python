# Week 4: Shopify Stock Visualization, Time-Series Analysis & Financial Insights

## Project Overview

This project focuses on visualizing and analyzing Shopify historical stock market data using Python. The cleaned dataset prepared during Week 3 is used to understand historical stock price movements, trading volume, moving averages, daily returns and volatility.

The project applies time-series visualization and statistical analysis to identify market trends, examine price fluctuations and generate meaningful financial insights.

## Objectives

- Visualize historical stock price movements over time.
- Analyze Open, High, Low and Close (OHLC) prices.
- Calculate and visualize 20-day and 50-day Simple Moving Averages.
- Examine the distribution of daily stock returns.
- Analyze trading volume and daily price changes.
- Identify high-volatility trading periods.
- Explore relationships between trading volume, daily returns and price volatility.
- Prepare a financial summary report.

## Dataset

**Dataset Name:** Shopify Stock Data  
**Source:** Preprocessed dataset from Week 3  
**Input File:** `Shopify_Stock_Cleaned.csv`

### Dataset Attributes

| Column | Description |
|---|---|
| date | Trading date |
| open | Opening stock price |
| high | Highest stock price during the trading session |
| low | Lowest stock price during the trading session |
| close | Closing stock price |
| adj_close | Adjusted closing stock price |
| volume | Number of shares traded |

## Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Project Workflow

### 1. Data Loading and Understanding

- Import the cleaned Week 3 dataset.
- Inspect the dataset structure and attributes.
- Convert the date column into a datetime format.
- Sort the observations chronologically.
- Set the date column as the time-series index.
- Check missing values and duplicate dates.

### 2. Financial Metric Calculation

Calculate important financial metrics:

**Daily Price Change**

Daily Price Change = Close − Open

**Daily Return Percentage**

Daily Return (%) = ((Current Adjusted Close − Previous Adjusted Close) / Previous Adjusted Close) × 100

**Daily Price Range**

Daily Range = High − Low

**Price Range Percentage**

Price Range (%) = ((High − Low) / Open) × 100

### 3. Moving Average Analysis

Calculate:

- 20-Day Simple Moving Average (SMA)
- 50-Day Simple Moving Average (SMA)

Moving averages help smooth short-term price fluctuations and identify possible changes in the overall price trend.

### 4. Stock Price Visualization

Create the following visualizations:

- Historical closing price line chart.
- Open, High, Low and Close price comparison.
- Trading volume over time.
- Closing price with 20-day and 50-day moving averages.
- Daily price change line chart.

### 5. Daily Return Analysis

Analyze daily returns using:

- Histogram with KDE curve.
- Box plot of daily returns.
- Mean daily return.
- Return variance.
- Return standard deviation.
- Maximum and minimum daily returns.

### 6. Volatility Analysis

- Calculate daily price range percentage.
- Calculate 20-day rolling standard deviation of daily returns.
- Visualize volatility over time.
- Identify trading days with unusually high price ranges using the 95th percentile.

### 7. Relationship Analysis

Explore relationships between:

- Trading volume and daily returns.
- Stock prices and daily price changes.
- Trading volume and price volatility.

Use scatter plots and a correlation heatmap to understand these relationships.

### 8. Monthly Analysis

Aggregate the data monthly to calculate:

- First opening price of the month.
- Highest price of the month.
- Lowest price of the month.
- Last closing price of the month.
- Total monthly trading volume.
- Average daily return for the month.

## Expected Visualizations

1. Historical Closing Price.
2. OHLC Price Movement.
3. Trading Volume Over Time.
4. Closing Price with 20-Day and 50-Day SMA.
5. Daily Return Distribution.
6. Daily Return Box Plot.
7. Daily Price Change.
8. Daily Price Range Percentage.
9. 20-Day Rolling Volatility.
10. Trading Volume vs Daily Returns.
11. Correlation Heatmap.
12. Monthly Trading Volume.

## Expected Deliverables

- Shopify Stock Analysis Jupyter Notebook.
- Processed Week 4 stock dataset.
- Monthly stock summary.
- Financial summary statistics.
- High-volatility trading days report.
- Financial insights report.

## GitHub Folder Structure

```text
Week-04-Shopify-Stock-Visualization/
│
├── Shopify_Stock_Visualization_Analysis.ipynb
│
├── README.md
│
├── data/
│   └── Shopify_Stock_Cleaned.csv
│
└── reports/
    ├── Shopify_Stock_Week4_Analysis.csv
    ├── Shopify_Monthly_Summary.csv
    ├── Shopify_Financial_Summary.csv
    └── Shopify_High_Volatility_Days.csv
```

## How to Run the Project

1. Open Google Colab.
2. Upload `Shopify_Stock_Visualization_Analysis.ipynb`.
3. Upload the cleaned Week 3 dataset, `Shopify_Stock_Cleaned.csv`.
4. Execute the notebook cells sequentially.
5. Review the generated charts and financial statistics.
6. Export the processed dataset and reports.
7. Prepare the financial insights report based on the actual analysis.

## Conclusion

This project uses Python visualization and time-series analysis techniques to study Shopify historical stock market data. Moving averages help identify price trends, while return distributions and rolling volatility help explain stock price variability. Trading volume analysis and correlation analysis provide additional information about market activity.

The project demonstrates how data analytics and visualization can transform historical stock data into meaningful financial observations.
