# Week 13 – Hotel Booking Demand Data Cleaning and Preprocessing

## 1. Project Overview

Week 13 focuses on cleaning and preprocessing the Hotel Booking Demand dataset using Python. The objective is to identify and handle missing values, remove duplicate records, correct data types, validate data, identify outliers, and create useful features for further analysis.

The cleaned dataset will be used in **Week 14 – Hotel Booking Demand: Revenue Management and Seasonality Analytics**.

## 2. Dataset Information

**Dataset Name:** Hotel Booking Demand Dataset  
**File Name:** `hotel_bookings.csv`  
**Format:** CSV

The dataset contains hotel reservation information from two hotel types:

- City Hotel
- Resort Hotel

### Important Dataset Attributes

| Column | Description |
|---|---|
| hotel | Type of hotel |
| is_canceled | Whether the booking was canceled |
| lead_time | Number of days between booking and arrival |
| arrival_date_year | Year of arrival |
| arrival_date_month | Month of arrival |
| arrival_date_day_of_month | Day of arrival |
| stays_in_weekend_nights | Weekend nights stayed |
| stays_in_week_nights | Weekday nights stayed |
| adults | Number of adults |
| children | Number of children |
| babies | Number of babies |
| meal | Meal package booked |
| country | Guest's country of origin |
| market_segment | Market segment |
| distribution_channel | Booking distribution channel |
| customer_type | Type of customer |
| adr | Average Daily Rate |
| reservation_status | Final reservation status |

*The exact number of records and columns depends on the dataset version used.*

## 3. Problem Statement

Hotel booking datasets may contain missing values, duplicate records, inconsistent data types, invalid numerical values, and unusual observations.

These data quality issues can affect the accuracy of hotel booking analysis and business decisions.

This project aims to prepare a reliable and structured dataset through systematic data cleaning, validation, and feature engineering.

## 4. Project Objectives

1. Understand the structure and characteristics of hotel booking data.
2. Identify missing values and duplicate records.
3. Standardize column names and categorical values.
4. Convert numerical columns into appropriate data types.
5. Handle missing values using suitable techniques.
6. Identify invalid and inconsistent numerical values.
7. Perform outlier detection using the IQR method.
8. Create meaningful features from existing columns.
9. Generate statistical summaries and data quality reports.
10. Export the cleaned dataset for Week 14 analysis.

## 5. Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 6. Data Preprocessing

### 6.1 Data Loading and Inspection
- Upload and load the CSV dataset.
- Examine the first and last records.
- Identify the number of rows and columns.
- Inspect column names and data types.
- Generate descriptive statistics.

### 6.2 Column Standardization
- Convert column names to lowercase.
- Replace spaces and hyphens with underscores.
- Maintain consistent naming conventions.

### 6.3 Missing Value Analysis
- Identify missing values in each column.
- Calculate missing value percentages.
- Visualize missing values using a heatmap.
- Apply suitable missing value handling techniques.
- Preserve missing agent and company identifiers rather than inventing values.

### 6.4 Duplicate Removal
- Identify duplicate records.
- Remove exact duplicate rows.
- Verify the dataset after duplicate removal.

### 6.5 Data Type Conversion
- Convert numerical columns into numeric formats.
- Handle invalid numerical conversions.
- Clean categorical text values.

### 6.6 Data Validation
- Identify negative values in fields that should be non-negative.
- Investigate invalid ADR values.
- Check guest counts and booking information.
- Identify bookings with zero guests without automatically deleting them.

### 6.7 Outlier Detection
Apply the Interquartile Range (IQR) method to selected numerical columns:

- Lead Time
- Average Daily Rate (ADR)
- Total Nights
- Total Guests
- Days in Waiting List

Outliers are identified and reported rather than automatically removed.

## 7. Feature Engineering

New features are created to improve the usefulness of the dataset.

| Feature | Description |
|---|---|
| total_nights | Total weekend and weekday nights |
| total_guests | Total adults, children, and babies |
| is_family | Indicates whether children or babies are included |
| has_booking_changes | Indicates whether booking changes occurred |
| has_special_requests | Indicates whether special requests were made |
| arrival_date | Combined arrival year, month, and day |
| arrival_year | Year extracted from arrival date |
| arrival_month | Numerical arrival month |
| arrival_month_name | Name of the arrival month |
| arrival_quarter | Arrival quarter |
| booking_status | Canceled or Not Canceled |

## 8. Exploratory Data Analysis

Basic exploratory analysis is performed to understand the cleaned dataset.

The analysis includes:

- Hotel type distribution.
- Booking cancellation status.
- Lead-time distribution.
- Average Daily Rate distribution.
- Total nights distribution.
- Guest count distribution.
- Categorical value summaries.
- Numerical descriptive statistics.
- Boxplots for outlier identification.

## 9. Reports Generated

The notebook generates the following output files:

| File Name | Description |
|---|---|
| hotel_bookings_cleaned.csv | Final cleaned dataset |
| missing_value_summary.csv | Missing value counts and percentages |
| duplicate_summary.csv | Duplicate record summary |
| invalid_records_removed.csv | Records removed due to negative values |
| outlier_summary.csv | IQR-based outlier analysis |
| hotel_booking_summary.csv | Overall dataset summary |
| hotel_wise_summary.csv | Hotel-wise booking summary, if available |

## 10. Project Folder Structure

```text
Week-13-Hotel-Booking-Data-Cleaning/
│
├── Hotel_Booking_Data_Cleaning.ipynb
├── README.md
│
├── data/
│   ├── hotel_bookings.csv
│   └── hotel_bookings_cleaned.csv
│
└── reports/
    ├── missing_value_summary.csv
    ├── duplicate_summary.csv
    ├── invalid_records_removed.csv
    ├── outlier_summary.csv
    ├── hotel_booking_summary.csv
    └── hotel_wise_summary.csv
```

*Note: The hotel-wise summary is generated only if the dataset contains the required hotel column. Keep the original dataset and cleaned dataset in the data folder. Save the generated reports in the reports folder.*

## 11. Expected Learning Outcomes

After completing this project, students will be able to:

- Understand real-world hotel booking datasets.
- Perform data cleaning using Pandas.
- Handle missing and duplicate values.
- Apply data validation techniques.
- Identify outliers using statistical methods.
- Perform feature engineering.
- Create visualizations using Matplotlib and Seaborn.
- Export clean datasets and analytical reports.
- Prepare data for business analytics.

## 12. Conclusion

The Week 13 project focuses on transforming raw hotel booking data into a structured and analysis-ready dataset. Data cleaning, validation, outlier identification, and feature engineering help improve data quality and reliability.

The resulting cleaned dataset provides the foundation for Week 14, where hotel booking patterns, revenue performance, cancellation trends, and seasonal demand will be analyzed.

