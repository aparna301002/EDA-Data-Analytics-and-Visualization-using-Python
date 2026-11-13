# Week 11 – Automobile Data Cleaning and Feature Engineering

## Project Overview

This project focuses on understanding, cleaning, and preparing automobile technical specification data using Python.

The Automobile Dataset contains information about vehicle manufacturers, engine specifications, fuel types, dimensions, horsepower, vehicle weight, fuel efficiency, and prices.

The main objective is to transform raw automobile data into a clean and structured dataset by handling missing values, correcting data types, identifying invalid records, performing statistical analysis, and creating meaningful features for further analysis.

This project also examines automobile specifications through exploratory analysis and identifies unusual values using statistical techniques.

## Dataset Information

**Dataset Name:** Automobile Dataset

**Input Dataset:** `Automobile_data.csv`

**Platform:** Google Colab

### Important Dataset Attributes

| Column | Description |
|---|---|
| make | Automobile manufacturer |
| fuel_type | Fuel type of the vehicle |
| aspiration | Engine aspiration type |
| num_of_doors | Number of doors |
| body_style | Vehicle body style |
| drive_wheels | Drive-wheel configuration |
| engine_location | Engine location |
| wheel_base | Distance between front and rear wheels |
| length | Vehicle length |
| width | Vehicle width |
| height | Vehicle height |
| curb_weight | Vehicle weight without passengers or cargo |
| engine_type | Engine configuration |
| num_of_cylinders | Number of engine cylinders |
| engine_size | Engine displacement |
| fuel_system | Fuel delivery system |
| bore | Cylinder bore measurement |
| stroke | Piston stroke measurement |
| compression_ratio | Engine compression ratio |
| horsepower | Engine power |
| peak_rpm | Engine speed at peak power |
| city_mpg | City fuel efficiency |
| highway_mpg | Highway fuel efficiency |
| price | Automobile price |

*Note: The exact columns may vary depending on the version of the Automobile Dataset used.*

## Problem Statement

Raw automobile datasets may contain missing values, inconsistent data types, duplicate records, invalid numerical values, and incomplete technical specifications.

These problems can affect the accuracy of automobile analysis and future predictive modelling.

Therefore, the dataset must be cleaned and transformed before conducting detailed pricing and performance analysis.

## Objectives

1. Understand automobile technical specifications.
2. Identify missing values and inconsistent entries.
3. Replace missing value symbols such as `?` with proper null values.
4. Remove duplicate records.
5. Convert numerical columns into appropriate data types.
6. Handle invalid zero and non-positive values.
7. Impute missing numerical and categorical values.
8. Perform statistical analysis of automobile specifications.
9. Create power-to-weight ratio and combined MPG features.
10. Identify outliers using the IQR method.
11. Analyze relationships between automobile attributes.
12. Export the cleaned dataset and analytical reports.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Data Cleaning and Preprocessing

### 1. Data Understanding

The initial dataset was inspected to understand:

- Number of rows and columns.
- Column names.
- Data types.
- Statistical summaries.
- Missing values.
- Duplicate records.

### 2. Column Standardization

Column names were standardized by:

- Converting names to lowercase.
- Removing unnecessary spaces.
- Replacing spaces and hyphens with underscores.

This ensures consistent column naming throughout the project.

### 3. Missing Value Handling

Some automobile datasets represent missing values using `?`.

The following preprocessing steps were performed:

- Replaced `?` with `NaN`.
- Identified missing values in each column.
- Calculated missing value percentages.
- Visualized missing values using a heatmap.

### 4. Duplicate Record Removal

Duplicate records were identified and removed to avoid repeated observations in the analysis.

### 5. Data Type Conversion

Important numerical attributes were converted into numeric data types.

These include:

- Wheel base
- Length
- Width
- Height
- Curb weight
- Engine size
- Bore
- Stroke
- Compression ratio
- Horsepower
- Peak RPM
- City MPG
- Highway MPG
- Price

### 6. Invalid Value Handling

Non-positive values were treated as invalid for selected measurements such as:

- Vehicle dimensions
- Engine size
- Horsepower
- Peak RPM
- Fuel efficiency
- Price

These values were converted into missing values before imputation.

### 7. Missing Value Imputation

Numerical missing values were handled using:

- Manufacturer-wise median imputation.
- Overall median imputation as a fallback.

Categorical missing values were handled using the mode of the respective column.

## Statistical Analysis

Descriptive statistics were calculated for important numerical attributes.

The following measures were analyzed:

- Count
- Mean
- Median
- Standard deviation
- Minimum
- Maximum

This analysis provides an overview of automobile technical specifications and their variations.

## Feature Engineering

New analytical features were created to improve automobile performance analysis.

### 1. Power-to-Weight Ratio

Power-to-weight ratio measures engine horsepower relative to vehicle weight.

**Formula:**

`Power-to-Weight Ratio = Horsepower / Curb Weight`

A higher value indicates more horsepower relative to the vehicle's weight.

### 2. Combined MPG

Combined MPG provides a simple average of city and highway fuel efficiency.

**Formula:**

`Combined MPG = (City MPG + Highway MPG) / 2`

This feature helps compare fuel efficiency across automobiles.

*Note: This is a simple average, not an official driving-cycle weighted combined fuel-economy rating.*

### 3. Weight Category

Vehicles were grouped according to curb weight:

- Light
- Medium
- Heavy
- Very Heavy

### 4. Engine Category

Vehicles were classified based on engine size:

- Small
- Medium
- Large
- Very Large

These categories support comparisons of automobile specifications.

## Exploratory Data Analysis

The following analyses were performed:

### 1. Manufacturer Analysis

- Counted automobile records by manufacturer.
- Compared manufacturer representation.
- Visualized the number of records using a count plot.

### 2. Fuel Type Analysis

- Examined fuel types.
- Counted vehicles under each fuel category.
- Visualized fuel type distribution.

### 3. Outlier Detection

The Interquartile Range (IQR) method was applied to identify unusual values in important numerical attributes.

Attributes analyzed include:

- Horsepower
- Peak RPM
- Price
- Engine size
- Curb weight
- Bore
- Stroke

**IQR Formula:**

`IQR = Q3 - Q1`

`Lower Bound = Q1 - 1.5 × IQR`

`Upper Bound = Q3 + 1.5 × IQR`

Box plots were created to visualize potential outliers.

Outliers were identified for investigation and were not automatically removed because extreme values may represent genuine automobile specifications.

### 4. Correlation Analysis

A correlation matrix and heatmap were created to understand relationships between numerical automobile attributes.

The analysis included:

- Engine size
- Horsepower
- Peak RPM
- Curb weight
- City MPG
- Highway MPG
- Price
- Power-to-weight ratio
- Combined MPG

## Reports Generated

The following CSV reports were exported:

| File Name | Description |
|---|---|
| `automobile_cleaned.csv` | Cleaned automobile dataset with engineered features |
| `automobile_statistics_summary.csv` | Descriptive statistical summary |
| `automobile_missing_value_summary.csv` | Missing value count and percentage |
| `automobile_outlier_summary.csv` | IQR-based outlier summary |
| `automobile_correlation_matrix.csv` | Correlation between numerical attributes |
| `manufacturer_summary.csv` | Manufacturer-wise vehicle count |
| `fuel_type_summary.csv` | Fuel type distribution |

## GitHub Folder Structure

```text
Week-11-Automobile-Data-Cleaning/
│
├── Automobile_Data_Cleaning_Feature_Engineering.ipynb
├── README.md
│
├── data/
│   └── Automobile_data.csv
│
└── reports/
    ├── automobile_cleaned.csv
    ├── automobile_statistics_summary.csv
    ├── automobile_missing_value_summary.csv
    ├── automobile_outlier_summary.csv
    ├── automobile_correlation_matrix.csv
    ├── manufacturer_summary.csv
    └── fuel_type_summary.csv
```

*Note: Include only the report files actually generated by the notebook. The manufacturer and fuel type reports are created only when their respective columns are available.*

## Expected Learning Outcomes

After completing this project, the following skills are developed:

- Understanding automobile technical specifications.
- Cleaning raw datasets using Pandas.
- Handling missing and invalid values.
- Performing numerical and categorical data preprocessing.
- Applying statistical imputation techniques.
- Creating meaningful analytical features.
- Detecting outliers using the IQR method.
- Performing correlation analysis.
- Preparing datasets for further automobile analytics.

## Conclusion

Week 11 focuses on preparing automobile data for further analysis by applying data cleaning, preprocessing, statistical analysis, and feature engineering techniques.

The cleaned dataset includes important automobile specifications and additional features such as power-to-weight ratio and combined MPG.

These prepared data attributes will be used in Week 12 to explore automobile pricing, fuel efficiency, and performance trade-offs.

