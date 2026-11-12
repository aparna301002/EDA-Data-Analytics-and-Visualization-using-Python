# Week 10 – House Sales Visualization, Spatial Analytics and Real-Estate Insights

## Project Overview

This project focuses on analyzing and visualizing house sales data to understand property valuation patterns, geographical price variations, and real-estate market trends using Python.

The analysis uses the cleaned King County House Sales Dataset prepared during Week 9. Different visualization techniques are applied to examine the relationship between property characteristics and house prices, compare property grades, analyze waterfront properties, and identify high-value and relatively affordable geographical clusters.

The project also generates a real-estate investment insights report based on the observed dataset.

## Dataset Information

**Dataset Name:** King County House Sales Dataset

**Input Dataset:** `house_sales_cleaned.csv`

**Source:** Week 9 – House Sales Data Cleaning and Feature Engineering

### Important Dataset Attributes

| Column | Description |
|---|---|
| price | Selling price of the property |
| sqft_living | Interior living area in square feet |
| sqft_lot | Total lot area in square feet |
| grade | Overall construction and design grade |
| waterfront | Indicates whether the property has a waterfront view |
| lat | Property latitude |
| long | Property longitude |
| price_per_sqft | Calculated price per square foot |
| sale_year | Year of property sale, if available |

## Problem Statement

Real-estate property prices vary according to several factors, including living area, construction quality, waterfront availability, and geographical location.

Understanding these factors is important for evaluating property values and identifying potential market opportunities.

This project uses exploratory data analysis and visualization techniques to examine house price variations and geographical patterns in the housing market.

## Objectives

1. Analyze the relationship between living area and house prices.
2. Compare average and median prices across property grades.
3. Evaluate price differences between waterfront and non-waterfront properties.
4. Visualize geographical house price distributions using latitude and longitude.
5. Identify high-value and relatively affordable geographical clusters.
6. Analyze price per square foot across property grades.
7. Examine yearly house price trends when sale-year information is available.
8. Generate a real-estate investment insights report.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Data Preparation

The cleaned dataset generated in Week 9 was used for this analysis.

The following preparation steps were performed:

- Loaded the cleaned house sales dataset.
- Inspected dataset dimensions and column information.
- Checked missing values.
- Converted important analytical columns into numeric data types.
- Removed records with missing essential visualization fields.
- Excluded invalid records with non-positive house prices or living areas.
- Calculated price per square foot.
- Created waterfront property labels for comparison.

## Exploratory Data Analysis and Visualization

### 1. Living Area vs House Price

A scatter plot with a regression trend line was created to examine the relationship between property living area and selling price.

**Analysis:**
- Examined whether larger living areas are associated with higher prices.
- Calculated the correlation coefficient.
- Observed the overall relationship between property size and valuation.

### 2. Property Grade Analysis

House prices were grouped according to property grade.

**Analysis:**
- Calculated property counts.
- Compared average and median prices.
- Visualized average house prices using a bar chart.
- Used box plots to compare price distributions across grades.

### 3. Waterfront Property Analysis

Waterfront and non-waterfront properties were compared.

**Analysis:**
- Calculated average and median selling prices.
- Compared the number of properties in each category.
- Visualized price distributions using box plots.
- Compared average prices using bar charts.

### 4. Geographical House Price Visualization

Latitude and longitude coordinates were used to visualize geographical price variations.

**Visualization:**
- Each point represents a property.
- Point colours represent selling prices.
- A colour bar indicates house price ranges.

This visualization helps identify geographical areas where higher or lower property prices are concentrated.

### 5. High-Value Geographical Clusters

Properties were grouped into geographical grid cells using rounded latitude and longitude coordinates.

The following metrics were calculated:

- Property count
- Median house price
- Average house price
- Median price per square foot

Clusters with at least 10 properties were considered for the geographical comparison.

The top 10 clusters based on median house price were identified as high-value clusters.

### 6. Relatively Affordable Geographical Clusters

The geographical clusters were sorted by median house price in ascending order.

The 20 clusters with the lowest median house prices were identified for comparison.

These clusters represent relatively affordable areas within the dataset and are not necessarily investment recommendations.

### 7. Price per Square Foot Analysis

Price per square foot was calculated using:

`Price per Square Foot = House Price / Living Area`

The analysis compared property valuation across different grades using summary statistics and box plots.

### 8. Yearly House Price Trends

Where the `sale_year` column was available, yearly house price summaries were generated.

The analysis included:

- Number of properties sold each year
- Average selling price
- Median selling price
- Yearly median price trend visualization

## Real-Estate Investment Insights

A report was generated using the analysis results.

It includes:

- Total valid property records.
- Average and median house prices.
- Average living area.
- Average price per square foot.
- Highest and lowest recorded house prices.
- Correlation between living area and price.
- Highest average-priced property grade.
- Waterfront price comparison.
- Highest-median-price geographical cluster.
- High-value and relatively affordable geographical cluster comparisons.

These insights describe historical patterns in the dataset. They do not guarantee future property appreciation or investment returns.

## Reports Generated

The following reports were exported as CSV files:

| File Name | Description |
|---|---|
| `overall_market_summary.csv` | Overall housing market statistics |
| `grade_price_summary.csv` | House price analysis by property grade |
| `waterfront_price_summary.csv` | Waterfront and non-waterfront comparison |
| `geographical_cluster_summary.csv` | Geographical price cluster analysis |
| `price_per_sqft_summary.csv` | Price per square foot analysis |
| `real_estate_investment_insights.csv` | High-value and affordable cluster insights |
| `yearly_price_summary.csv` | Yearly house price summary, if available |
| `house_sales_week10_analysis.csv` | Dataset used for Week 10 analysis |

## GitHub Folder Structure

```text
Week-10-House-Sales-Visualization/
│
├── House_Sales_Visualization_Spatial_Analytics.ipynb
├── README.md
│
├── data/
│   └── house_sales_cleaned.csv
│
└── reports/
    ├── overall_market_summary.csv
    ├── grade_price_summary.csv
    ├── waterfront_price_summary.csv
    ├── geographical_cluster_summary.csv
    ├── price_per_sqft_summary.csv
    ├── real_estate_investment_insights.csv
    ├── yearly_price_summary.csv
    └── house_sales_week10_analysis.csv
```

*Note: Include `yearly_price_summary.csv` only if the notebook generated it. Add only files that were actually created.*

## Expected Learning Outcomes

After completing this project, the following skills are developed:

- Applying exploratory data analysis to real-estate datasets.
- Creating scatter plots and regression trend lines.
- Comparing categorical property characteristics using bar charts and box plots.
- Performing geographical analysis using latitude and longitude.
- Identifying high-value and relatively affordable geographical clusters.
- Calculating property valuation metrics.
- Generating data-driven real-estate market insights.
- Exporting analytical results for reporting and further analysis.

## Conclusion

Week 10 completes the visualization and geographical analysis of the King County House Sales Dataset.

By combining property characteristics, selling prices, geographical coordinates, and derived valuation metrics, the project provides a better understanding of real-estate market patterns.

The analysis demonstrates how Python-based exploratory data analysis and visualization can support property comparison and historical market evaluation.
