# Week 2: Superstore Sales Visualization, Relationship Analysis & Business Insights

## Project Overview

This project focuses on analyzing and visualizing retail sales performance using the Superstore Sales Dataset prepared during Week 1.

Numerical summaries alone cannot fully explain why certain product categories generate losses or how discounting affects overall profitability. Therefore, this project uses data visualization and relationship analysis to identify sales patterns, profit variations, and possible business improvement opportunities.

The analysis focuses on understanding sales and profit distributions, comparing performance across product categories and geographical regions, and examining the relationship between discounts and profitability.

## Objectives

- Perform univariate, bivariate, and multivariate analysis of sales performance.
- Evaluate profit margins across categories, sub-categories, and geographical regions.
- Analyze the relationship between discounts, sales volume, and overall profitability.
- Identify possible discount levels associated with reduced profitability.
- Generate a correlation heatmap for numerical attributes.
- Prepare a one-page business insights report based on the analysis.

## Dataset

**Dataset Name:** Superstore Sales Dataset

**Input File:** `Superstore_Cleaned.csv`

**Source:** Cleaned dataset generated from Week 1 – Superstore Sales Data Cleaning.

### Important Columns

| Column | Description |
|---|---|
| Order Date | Date on which the order was placed |
| Ship Date | Date on which the order was shipped |
| Ship Mode | Shipping method selected |
| Segment | Customer segment |
| Region | Geographical sales region |
| Category | Main product category |
| Sub-Category | Product sub-category |
| Sales | Total sales amount |
| Quantity | Number of products sold |
| Discount | Discount applied to the order |
| Profit | Profit or loss generated |

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Tasks Performed

### 1. Data Loading and Preparation

- Import the cleaned Superstore dataset.
- Inspect dataset dimensions, column names, and data types.
- Verify the availability of important numerical and categorical columns.
- Convert numerical attributes into appropriate data types.
- Calculate profit margin using Sales and Profit.

### 2. Univariate Analysis

Analyze individual numerical attributes to understand their distributions.

- Sales distribution
- Profit distribution
- Quantity distribution
- Discount distribution

Visualization techniques:
- Histograms
- Distribution plots

### 3. Category-Wise Sales and Profit Analysis

Compare sales and profitability across product categories.

- Calculate total sales for each category.
- Calculate total profit for each category.
- Visualize category-wise sales and profit using bar plots.

### 4. Sub-Category Profit Analysis

- Calculate total profit for each sub-category.
- Identify sub-categories with comparatively high and low profits.
- Visualize sub-category performance using bar plots.

### 5. Sales and Profit Distribution

Use box plots to compare sales and profit distributions across product categories.

The visualizations help identify:
- Distribution differences between categories.
- Unusual values and potential outliers.
- Variations in sales and profit performance.

### 6. Discount vs Profitability Analysis

Analyze the relationship between discount levels and profitability.

- Group records by discount level.
- Calculate total sales and total profit.
- Calculate average profit and profit margin.
- Visualize discount levels against profit margin.
- Identify discount ranges associated with lower profitability.

### 7. Discount Band Analysis

Group discount values into ranges to simplify comparison.

The analysis examines profitability across different discount bands and helps identify discount levels that may require further investigation.

### 8. Regional Sales and Profit Analysis

- Calculate total sales by region.
- Calculate total profit by region.
- Compare regional sales and profitability.
- Visualize regional performance using bar plots.

### 9. Correlation Analysis

Generate a correlation matrix for numerical attributes.

Create a heatmap to examine relationships between numerical variables such as:

- Sales
- Quantity
- Discount
- Profit

Correlation indicates the strength and direction of a linear relationship. It does not establish causation.

### 10. Business Insights Report

Prepare a one-page report summarizing the actual results obtained from the analysis.

The report should include:

- Category-wise sales and profit observations.
- Sub-category profitability observations.
- Regional performance.
- Discount and profit relationship.
- Important correlation findings.
- Business recommendations supported by the data.

## Project Folder Structure

```text
Week-02-Superstore-Sales-Visualization/
│
├── Superstore_Sales_Visualization.ipynb
├── README.md
│
├── data/
│   └── Superstore_Cleaned.csv
│
└── reports/
    ├── One_Page_Business_Insights_Report.md
    ├── category_summary.csv
    ├── subcategory_summary.csv
    ├── regional_summary.csv
    └── discount_analysis.csv
```

## How to Run the Project

1. Download or clone the repository.
2. Open the Week 2 project folder.
3. Place `Superstore_Cleaned.csv` inside the `data` folder.
4. Open `Superstore_Sales_Visualization.ipynb` using Jupyter Notebook or JupyterLab.
5. Install the required libraries if they are not already installed.

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

6. Run all notebook cells sequentially.
7. Review the generated visualizations and summary tables.
8. Check the `reports` folder for exported analysis results.
9. Complete the one-page business insights report using the actual results.

## Expected Deliverables

- Jupyter Notebook containing complete analysis and visualizations.
- Category-wise sales and profit comparison.
- Sub-category profit analysis.
- Sales and profit box plots.
- Discount versus profit margin visualization.
- Discount band analysis.
- Regional sales and profit comparison.
- Numerical correlation heatmap.
- One-page business insights report.
- Exported summary CSV files.

## Key Considerations

- Use the cleaned dataset generated in Week 1.
- Do not assume that higher discounts always result in lower profits; verify this using the actual analysis.
- Correlation does not imply causation.
- Do not report findings or numerical values without checking the generated results.
- Interpret visualizations in terms of actual business performance.

## Conclusion

This project uses exploratory data analysis and visualization techniques to understand retail sales performance. By comparing product categories, sub-categories, regions, and discount levels, the analysis aims to identify important business patterns and provide data-supported recommendations for improving sales and profitability.
