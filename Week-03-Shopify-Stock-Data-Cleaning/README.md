# Week 3: Shopify Stock Data Understanding, Cleaning & Exploratory Analysis

## 1. Project Overview

This project focuses on understanding, cleaning, and performing Exploratory Data Analysis (EDA) on Shopify stock market data.

Financial market data requires proper handling of time-series dates, missing values, incorrect stock prices, and unusual trading activity. These factors are important for accurately evaluating stock performance and market behavior.

This project uses Python to clean stock price attributes, organize trading dates, calculate daily price changes and returns, analyze trading volume, identify anomalous trading days, and summarize stock return distributions.

## 2. Objectives

- Format and index time-series date attributes correctly.
- Load and clean stock price attributes (Open, High, Low, Close, Adjusted Close, Volume).
- Calculate daily price change.
- Calculate daily return percentage.
- Evaluate stock trading volume trends.
- Identify anomalous trading days.
- Summarize stock return distributions using mean, variance, and standard deviation.

## 3. Dataset Information

**Dataset Name:** Shopify Stock Data (2025)

**Input File:** `Shopify_Stock_2025.csv`

**Cleaned Output File:** `Shopify_Stock_Cleaned.csv`

### Dataset Attributes

| Column | Description |
|---|---|
| date | Stock trading date with timezone information |
| open | Opening stock price |
| high | Highest stock price during the trading day |
| low | Lowest stock price during the trading day |
| close | Closing stock price |
| adj_close | Adjusted closing stock price |
| volume | Total number of shares traded |

## 4. Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 5. Data Understanding and Cleaning

### 5.1 Dataset Inspection

- Load the Shopify stock dataset using Pandas.
- Display the first and last five records.
- Check the number of rows and columns.
- Inspect column names and data types.
- Generate descriptive statistical summaries.

### 5.2 Date Formatting

- Convert the date column into datetime format.
- Handle invalid date values.
- Sort records chronologically.
- Set the date column as the DataFrame index.

### 5.3 Numerical Data Conversion

Convert the following attributes into appropriate numerical formats:

- open
- high
- low
- close
- adj_close
- volume

### 5.4 Missing Value and Duplicate Handling

- Identify missing values.
- Calculate missing-value percentages.
- Handle incomplete records.
- Identify duplicate records.
- Inspect duplicate trading dates.

### 5.5 Stock Price Validation

- Identify zero or negative stock prices.
- Check for negative trading volume.
- Validate High, Low, Open, and Close price relationships.
- Investigate invalid or inconsistent records.

## 6. Financial Metric Calculations

### 6.1 Daily Price Change

Daily Price Change measures the difference between the closing price and opening price.

**Formula:**

Daily Price Change = Close - Open

Interpretation:
- Positive value: Stock closed above its opening price.
- Negative value: Stock closed below its opening price.
- Zero: Stock opened and closed at the same price.

### 6.2 Daily Return Percentage

Daily Return Percentage measures the percentage change in adjusted closing price compared with the previous trading day's adjusted closing price.

**Formula:**

Daily Return (%) = ((Current Adjusted Close - Previous Adjusted Close) / Previous Adjusted Close) × 100

This metric helps evaluate daily stock performance.

### 6.3 Daily Trading Range

Daily Trading Range measures the difference between the highest and lowest prices during a trading day.

**Formula:**

Daily Range = High - Low

### 6.4 Range Percentage

**Formula:**

Range Percentage = ((High - Low) / Open) × 100

This metric helps understand intraday price movement relative to the opening price.

## 7. Trading Volume Analysis

- Calculate average trading volume.
- Identify maximum and minimum trading volume.
- Calculate total trading volume.
- Generate descriptive statistics.
- Visualize trading volume distribution using a histogram and KDE plot.

## 8. Anomalous Trading Day Detection

The Interquartile Range (IQR) method is used to identify unusually high or low trading-volume observations.

**Formulas:**

IQR = Q3 - Q1

Upper Bound = Q3 + 1.5 × IQR

Lower Bound = Q1 - 1.5 × IQR

Potential anomalous trading days are identified and examined for unusual trading activity.

## 9. Statistical Analysis of Daily Returns

Calculate the following statistical measures:

| Statistical Measure | Description |
|---|---|
| Mean | Average daily return |
| Variance | Measures the dispersion of daily returns |
| Standard Deviation | Measures the spread of daily returns |
| Minimum | Lowest daily return |
| Maximum | Highest daily return |
| Median | Middle value of daily returns |

These measures help evaluate the distribution and variability of stock returns.

## 10. Data Visualization

The following visualizations are generated:

1. Trading volume distribution histogram.
2. Trading volume box plot.
3. Daily price change line plot.
4. Daily return percentage line plot.
5. Daily return distribution histogram with KDE.
6. Monthly trading volume bar chart.

## 11. Project Folder Structure

```text
Week-03-Shopify-Stock-Data-Cleaning/
│
├── Shopify_Stock_Data_Analysis.ipynb
├── README.md
│
├── data/
│   ├── Shopify_Stock_2025.csv
│   └── Shopify_Stock_Cleaned.csv
│
└── reports/
    ├── stock_summary.csv
    ├── monthly_volume_summary.csv
    ├── anomalous_trading_days.csv
    └── return_statistics.csv
```

## 12. How to Run the Project

1. Open the Google Colab notebook.
2. Upload the original Shopify stock CSV dataset.
3. Execute the notebook cells sequentially.
4. Inspect the dataset and perform data cleaning.
5. Calculate daily price changes and returns.
6. Analyze trading volume and identify potential anomalies.
7. Calculate return statistics.
8. Generate the visualizations.
9. Export the cleaned dataset and summary reports.

### Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

## 13. Expected Deliverables

- Shopify stock data understanding and cleaning notebook.
- Cleaned Shopify stock dataset.
- Daily price change calculation.
- Daily return percentage calculation.
- Trading volume analysis.
- Anomalous trading day identification.
- Daily return statistical analysis.
- Monthly trading volume summary.
- Stock summary report.
- Exported CSV files.

## 14. Important Considerations

- Stock market data contains trading days rather than every calendar day.
- Weekends and exchange holidays should not automatically be treated as missing records.
- Daily returns should use the previous available trading day's adjusted closing price.
- Missing stock prices should not be filled with arbitrary values.
- Statistical outliers are not necessarily incorrect records.
- Unusual trading volume should be investigated before classifying it as an error.
- Verify the dataset's actual date range before describing it as 2025-only.

## 15. Conclusion

This project demonstrates the use of Python for understanding, cleaning, and analyzing financial time-series data.

By organizing trading dates, validating stock price attributes, calculating daily price changes and returns, analyzing trading volume, and examining return statistics, the project prepares a structured dataset for further visualization and financial insights in Week 4.

## Author

Aparna M

## Project

14-Week Practical Project – EDA: Data Analytics and Visualization Using Python
