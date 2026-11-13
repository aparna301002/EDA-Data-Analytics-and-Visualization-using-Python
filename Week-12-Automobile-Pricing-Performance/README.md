# Week 12 – Automobile Pricing and Performance Trade-off Analysis

## Project Overview

This project focuses on analyzing automobile pricing, engine performance, and fuel efficiency using Python.

The analysis uses the cleaned Automobile Dataset prepared during Week 11. It examines how automobile prices vary across manufacturers and how technical specifications such as engine size, horsepower, curb weight, and fuel efficiency are related to vehicle pricing.

The project also explores performance trade-offs between engine power and fuel economy, classifies automobiles based on price ranges, and generates analytical reports to support automobile comparisons.

## Dataset Information

**Dataset Name:** Automobile Dataset

**Input Dataset:** `automobile_cleaned.csv`

**Source:** Week 11 – Automobile Data Cleaning and Feature Engineering

### Important Dataset Attributes

| Column | Description |
|---|---|
| make | Automobile manufacturer |
| price | Automobile selling price |
| horsepower | Engine power |
| engine_size | Engine displacement |
| curb_weight | Vehicle weight |
| city_mpg | City fuel efficiency |
| highway_mpg | Highway fuel efficiency |
| power_to_weight | Horsepower relative to vehicle weight |
| combined_mpg | Average of city and highway MPG |
| fuel_type | Fuel type of the automobile |

## Problem Statement

Automobile buyers consider several factors when selecting a vehicle, including price, engine performance, fuel efficiency, and manufacturer.

Vehicles with higher horsepower or larger engines may have different pricing and fuel-efficiency characteristics compared with vehicles designed for better fuel economy.

Understanding these relationships helps evaluate automobile specifications and identify performance trade-offs.

This project applies exploratory data analysis and visualization techniques to examine automobile pricing, performance, and fuel-efficiency patterns.

## Objectives

1. Analyze automobile prices across different manufacturers.
2. Examine the relationship between engine size and automobile price.
3. Analyze the relationship between horsepower and price.
4. Compare city, highway, and combined fuel efficiency.
5. Evaluate fuel efficiency across manufacturers.
6. Examine the relationship between curb weight and fuel efficiency.
7. Analyze power-to-weight ratio.
8. Identify automobile performance and fuel-efficiency trade-offs.
9. Classify automobiles based on price distribution.
10. Generate automobile pricing and performance reports.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Data Preparation

The cleaned dataset generated during Week 11 was used for this analysis.

The following preparation steps were performed:

- Loaded the cleaned automobile dataset.
- Inspected dataset dimensions and column information.
- Checked missing values.
- Converted important numerical columns into appropriate data types.
- Removed records with missing essential analytical attributes.
- Excluded invalid non-positive values for price, horsepower, engine size, vehicle weight, and fuel-efficiency measurements.
- Recalculated power-to-weight ratio and combined MPG to maintain consistency.

## Exploratory Data Analysis

### 1. Automobile Price Analysis

The distribution of automobile prices was examined using descriptive statistics and histograms.

The following measures were calculated:

- Average price
- Median price
- Minimum price
- Maximum price

A histogram was created to understand the distribution of automobile prices.

### 2. Manufacturer-wise Price Analysis

Automobile prices were grouped by manufacturer.

The following metrics were calculated:

- Number of vehicles
- Average price
- Median price
- Minimum price
- Maximum price

A bar chart was created to compare average automobile prices across manufacturers.

The highest and lowest average-priced manufacturers were also identified.

### 3. Engine Size vs Price Analysis

A scatter plot with a regression trend line was created to examine the relationship between engine size and automobile price.

The correlation coefficient was calculated to understand the strength and direction of the relationship.

### 4. Horsepower vs Price Analysis

The relationship between horsepower and automobile price was analyzed using scatter plots.

Where fuel type was available, it was included as an additional visual grouping variable.

This analysis helps examine how engine power relates to automobile pricing.

### 5. Fuel Efficiency Analysis

Fuel efficiency was examined using:

- City MPG
- Highway MPG
- Combined MPG

Combined MPG was calculated using:

`Combined MPG = (City MPG + Highway MPG) / 2`

The average and median fuel-efficiency values were calculated and visualized.

### 6. Manufacturer-wise Fuel Efficiency Analysis

Fuel-efficiency metrics were grouped by manufacturer.

The following measures were calculated:

- Average city MPG
- Average highway MPG
- Average combined MPG
- Number of vehicle records

A bar chart was created to compare combined fuel efficiency across manufacturers.

### 7. Curb Weight vs Fuel Efficiency

A scatter plot with a regression trend line was created to examine the relationship between vehicle weight and combined MPG.

The correlation coefficient was calculated to understand whether heavier automobiles tend to have lower fuel efficiency in the dataset.

### 8. Power-to-Weight Ratio Analysis

Power-to-weight ratio was used to compare engine horsepower relative to vehicle weight.

**Formula:**

`Power-to-Weight Ratio = Horsepower / Curb Weight`

A histogram was created to understand the distribution of this feature.

A scatter plot was also used to compare power-to-weight ratio with combined MPG.

### 9. Automobile Performance Trade-off Analysis

Performance trade-offs were examined using the following relationships:

- Price vs Combined MPG
- Horsepower vs Combined MPG
- Engine Size vs Combined MPG
- Power-to-Weight Ratio vs Combined MPG

These visualizations help compare vehicles based on cost, engine power, and fuel efficiency.

### 10. Correlation Analysis

A correlation matrix and heatmap were generated to examine relationships between important numerical attributes.

The analysis included:

- Price
- Horsepower
- Engine size
- Curb weight
- City MPG
- Highway MPG
- Combined MPG
- Power-to-weight ratio

Correlation values help identify positive and negative associations between automobile attributes.

## Automobile Price Classification

Automobiles were classified into four price categories using quartiles from the observed dataset.

The categories include:

- Budget
- Mid-Range
- Premium
- Luxury

The analysis compared:

- Number of automobiles in each category
- Average price
- Median price
- Average horsepower
- Average combined MPG

This classification is based on the dataset's price distribution rather than fixed market price boundaries.

## Automobile Performance Profiles

Manufacturer-wise performance summaries were generated using:

- Number of vehicle records
- Average automobile price
- Average horsepower
- Average engine size
- Average combined MPG
- Average power-to-weight ratio

Manufacturers with the highest and lowest average combined MPG were also identified.

## Reports Generated

The following CSV reports were exported:

| File Name | Description |
|---|---|
| `automobile_week12_analysis.csv` | Automobile dataset used for Week 12 analysis |
| `manufacturer_price_summary.csv` | Manufacturer-wise automobile price analysis |
| `manufacturer_fuel_efficiency_summary.csv` | Manufacturer-wise fuel-efficiency analysis |
| `fuel_efficiency_summary.csv` | City, highway, and combined MPG statistics |
| `price_category_summary.csv` | Automobile price category comparison |
| `manufacturer_performance_summary.csv` | Manufacturer-wise performance comparison |
| `automobile_tradeoff_correlation.csv` | Correlation matrix of pricing and performance attributes |

## GitHub Folder Structure

```text
Week-12-Automobile-Pricing-Performance/
│
├── Automobile_Pricing_Performance_Analysis.ipynb
├── README.md
│
├── data/
│   └── automobile_cleaned.csv
│
└── reports/
    ├── automobile_week12_analysis.csv
    ├── manufacturer_price_summary.csv
    ├── manufacturer_fuel_efficiency_summary.csv
    ├── fuel_efficiency_summary.csv
    ├── price_category_summary.csv
    ├── manufacturer_performance_summary.csv
    └── automobile_tradeoff_correlation.csv
```

*Note: Include only the reports actually generated by the notebook.*

## Expected Learning Outcomes

After completing this project, the following skills are developed:

- Performing exploratory data analysis on automobile datasets.
- Comparing automobile prices across manufacturers.
- Analyzing engine size and horsepower relationships with price.
- Evaluating city, highway, and combined fuel efficiency.
- Understanding the relationship between vehicle weight and fuel economy.
- Interpreting power-to-weight ratios.
- Identifying automobile performance trade-offs.
- Classifying automobiles based on price distribution.
- Creating manufacturer-wise analytical summaries.
- Generating data-driven automobile reports.

## Conclusion

Week 12 focuses on automobile pricing, fuel-efficiency analysis, and performance trade-offs using Python.

By examining engine specifications, horsepower, vehicle weight, and fuel efficiency, the project provides insights into how automobile characteristics are associated with price and performance.

The analysis demonstrates how exploratory data analysis and visualization can support automobile comparisons and help understand different vehicle performance profiles.
