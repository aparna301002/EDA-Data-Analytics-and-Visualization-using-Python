# Week 1: Superstore Sales Data Cleaning and Exploratory Analysis

## Project Overview

This project focuses on understanding, cleaning, and preparing the Superstore Sales dataset using Python. Data cleaning is an essential step in data analytics because raw datasets may contain missing values, duplicate records, inconsistent data formats, incorrect data types, and outliers.

The objective is to prepare a reliable dataset for further analysis and business insights.

## Problem Statement

Raw retail datasets often contain missing values, duplicate entries, inconsistent data types, and extreme outliers. Before generating meaningful business insights, the data must be inspected, cleaned, and standardized.

## Objectives

- Inspect dataset dimensions, column names, data types, and basic statistics.
- Identify and handle missing values.
- Detect and remove duplicate records.
- Convert Order Date and Ship Date into proper datetime formats.
- Standardize categorical attributes.
- Calculate summary statistics for numerical attributes.
- Detect outliers using IQR and Z-score methods.

## Dataset Description

**Dataset Name:** Superstore Sales Dataset

**Dataset File:** Sample-Superstore.csv

The dataset contains retail transaction information, including:

- Row ID
- Order ID
- Order Date
- Ship Date
- Ship Mode
- Customer ID
- Customer Name
- Segment
- Country/Region
- City
- Sales
- Quantity
- Discount
- Profit

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy

## Tasks Performed

### 1. Data Loading

Imported the Superstore Sales dataset using Pandas and examined the initial records.

### 2. Data Understanding

Inspected the dataset using:

- `head()`
- `tail()`
- `shape`
- `columns`
- `info()`
- `describe()`

### 3. Missing Value Analysis

Identified missing values using `isnull()` and calculated missing-value percentages. Applied suitable imputation methods where appropriate.

### 4. Duplicate Handling

Identified duplicate records using `duplicated()` and removed exact duplicate rows using `drop_duplicates()`.

### 5. Data Type Conversion

Converted Order Date and Ship Date into datetime format and ensured numerical attributes were in appropriate numeric formats.

### 6. Text Standardization

Standardized categorical attributes such as Category, Sub-Category, Segment, Ship Mode, and City by removing unnecessary spaces and applying consistent text formatting.

### 7. Statistical Analysis

Calculated descriptive statistics for:

- Sales
- Quantity
- Profit
- Discount

Measures included mean, median, standard deviation, minimum, maximum, and quartiles.

### 8. Outlier Detection Using IQR

Identified potential outliers using the Interquartile Range method.

- Lower Bound = Q1 − 1.5 × IQR
- Upper Bound = Q3 + 1.5 × IQR

### 9. Outlier Detection Using Z-Score

Identified potential extreme values using a Z-score threshold of ±3.

### 10. Data Export

Exported the cleaned dataset into a CSV file for further analysis.

**Output File:** Superstore_Cleaned.csv

## Repository Structure

```text
Week-01-Superstore-Sales-Data-Cleaning/
│
├── Superstore_Data_Cleaning.ipynb
├── README.md
│
└── data/
    ├── Sample-Superstore.csv
    └── Superstore_Cleaned.csv
```

## How to Run the Project

1. Clone or download the repository.
2. Install the required Python libraries.
3. Place the original CSV dataset inside the data folder.
4. Open the Jupyter Notebook.
5. Execute all cells sequentially.
6. Review the analysis results and visualizations.
7. Find the cleaned dataset in the data folder.

### Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### Run Jupyter Notebook

```bash
jupyter notebook
```

## Key Deliverables

- Data inspection and understanding.
- Missing-value analysis and handling.
- Duplicate detection and removal.
- Date conversion and text standardization.
- Numerical summary statistics.
- IQR-based outlier detection.
- Z-score-based outlier detection.
- Final cleaned CSV dataset.

## Conclusion

The Superstore Sales dataset was examined and prepared through data cleaning and exploratory analysis. Missing values and duplicate records were handled, data types and categorical formats were standardized, and numerical summary statistics were calculated.

Potential outliers were identified using IQR and Z-score methods for further investigation. The cleaned dataset provides a suitable foundation for Week 2, which focuses on retail sales visualization, relationship analysis, and business insights.

---

**Project:** EDA – Data Analytics and Visualization using Python  
**Week:** 01  
**Topic:** Superstore Sales Data Cleaning and Exploratory Analysis
