# Week 9 – House Sales Data Cleaning and Feature Engineering

## 1. Project Overview

Week 9 focuses on understanding, cleaning, preprocessing, and transforming real-estate sales data using Python.

The project uses the King County House Sales Dataset to examine property characteristics, sale dates, construction years, renovation details, living areas, and house prices.

Raw real-estate datasets may contain missing values, duplicate records, invalid measurements, inconsistent data types, and extreme property valuations. Data cleaning and feature engineering are essential before conducting further real-estate analysis.

This project prepares a structured dataset for Week 10, which focuses on real-estate valuation and spatial analytics.

## 2. Dataset Information

**Dataset Name:** King County House Sales Dataset

**Input File:** `kc_house_data.csv`

**Output File:** `house_sales_cleaned.csv`

### Important Dataset Attributes

| Column | Description |
|---|---|
| id | Unique house identification |
| date | Date of property sale |
| price | Selling price of the house |
| bedrooms | Number of bedrooms |
| bathrooms | Number of bathrooms |
| sqft_living | Living area in square feet |
| sqft_lot | Total lot area in square feet |
| floors | Number of floors |
| waterfront | Waterfront property indicator |
| view | Property view rating |
| condition | Property condition rating |
| grade | Construction and design grade |
| sqft_above | Area above ground |
| sqft_basement | Basement area |
| yr_built | Year of construction |
| yr_renovated | Year of renovation |
| zipcode | Property postal code |
| lat | Latitude |
| long | Longitude |
| sqft_living15 | Average living area of nearby 15 houses |
| sqft_lot15 | Average lot area of nearby 15 houses |

## 3. Problem Statement

Real-estate valuation requires accurate information about property size, location, construction year, renovation history, and sale price.

Raw housing datasets may contain missing entries, invalid zero values, incorrect data types, and extreme price observations. These issues can affect the reliability of property analysis.

Therefore, the dataset must be cleaned and transformed by extracting date-related information, calculating property age, creating renovation indicators, and deriving price-per-square-foot metrics.

## 4. Objectives

- Inspect property features such as bedrooms, bathrooms, living area, grade, and construction year.
- Identify missing values and duplicate records.
- Handle invalid zero values in room counts and area measurements.
- Convert sale dates into appropriate datetime formats.
- Extract sale year, month, quarter, and day.
- Calculate property age using sale year and construction year.
- Identify renovated and non-renovated properties.
- Calculate price per square foot for living area and total lot area.
- Detect extreme property valuation outliers using statistical methods.
- Export the cleaned dataset and feature engineering reports.

## 5. Tools and Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 6. Data Understanding and Inspection

The dataset was loaded into Google Colab using Pandas.

The following inspection activities were performed:

- Displayed the first and last records.
- Checked the number of rows and columns.
- Examined column names and data types.
- Generated descriptive statistical summaries.
- Identified numerical and categorical attributes.
- Checked missing values and duplicate records.

## 7. Data Cleaning and Preprocessing

The following cleaning operations were performed:

### Column Standardization
- Converted column names into lowercase.
- Replaced spaces with underscores.
- Removed unnecessary spaces from column names.

### Missing Value Handling
- Identified missing values in all columns.
- Calculated missing value percentages.
- Used median imputation for selected numerical property attributes.
- Removed records with invalid sale dates.

### Duplicate Handling
- Identified duplicate records.
- Removed duplicate rows.
- Inspected repeated property IDs separately.

### Invalid Zero Value Handling
- Investigated zero values in bedrooms, bathrooms, living area, and lot area.
- Converted invalid zero measurements into missing values before imputation.
- Preserved zero renovation years because they indicate no recorded renovation.

### Data Type Conversion
- Converted sale dates into datetime format.
- Converted relevant property attributes into numerical data types.

## 8. Temporal Feature Engineering

The sale date was processed to create additional time-related features.

The following attributes were generated:

| Feature | Description |
|---|---|
| sale_year | Year in which the property was sold |
| sale_month | Month of property sale |
| sale_quarter | Quarter of property sale |
| sale_day | Day of property sale |

These features help support future analysis of property sales over time.

## 9. Property Age Calculation

Property age was calculated using the sale year and construction year.

**Formula:**

`Property Age = Sale Year - Year Built`

The new feature `property_age` represents the approximate age of a property at the time of sale.

Property age categories were also created:

- New
- Recent
- Middle Aged
- Old
- Very Old

These categories were created using project-defined age intervals.

## 10. Renovation Feature Engineering

Renovation information was used to identify renovated and non-renovated properties.

A new feature named `is_renovated` was created.

| Value | Meaning |
|---|---|
| 1 | Property has a recorded renovation year |
| 0 | No recorded renovation year |

Additional features:

- `renovation_year`
- `years_since_renovation`

The renovation age was calculated only for valid renovation years that did not occur after the property sale year.

## 11. Price per Square Foot Calculation

Unit valuation metrics were calculated to understand property prices relative to their size.

### Price per Square Foot of Living Area

**Formula:**

`Price per Sqft Living = House Price / Living Area`

New feature: `price_per_sqft_living`

### Price per Square Foot of Lot Area

**Formula:**

`Price per Sqft Lot = House Price / Total Lot Area`

New feature: `price_per_sqft_lot`

These metrics provide different perspectives on property valuation based on usable living space and total land area.

## 12. Additional Feature Engineering

The following additional features were created:

| Feature | Description |
|---|---|
| total_rooms | Combined bedroom and bathroom count |
| living_lot_ratio | Ratio of living area to lot area |
| property_age_category | Categorized property age |

These features help organize property information for future analysis.

## 13. Statistical Analysis

Descriptive statistical measures were calculated for important property attributes.

The analysis included:

- Mean
- Median
- Mode
- Standard deviation
- Variance
- Minimum and maximum values
- Quartiles

Important numerical variables included:

- House price
- Bedrooms
- Bathrooms
- Living area
- Lot area
- Property age
- Price per square foot

## 14. House Price Distribution Analysis

Data visualization was used to understand the distribution of property prices and measurements.

The following visualizations were generated:

| Visualization | Purpose |
|---|---|
| Histogram | Understand house price distribution |
| Boxplot | Identify potential extreme price values |
| Histogram of Living Area | Examine the distribution of property living space |
| Boxplots of Property Attributes | Compare distributions and identify potential outliers |

## 15. Outlier Detection Using IQR

The Interquartile Range method was used to identify potential outliers in property-related numerical variables.

**Formulas:**

`IQR = Q3 - Q1`

`Lower Bound = Q1 - 1.5 × IQR`

`Upper Bound = Q3 + 1.5 × IQR`

Outlier detection was performed on:

- Price
- Living area
- Lot area
- Bedrooms
- Bathrooms
- Price per square foot of living area
- Price per square foot of lot area

Outliers were identified and summarized rather than automatically removed, because extreme property values may represent genuine high-value or large properties.

## 16. Property Age and Renovation Analysis

Summary tables were generated to compare:

- Average house price across property age categories.
- Median house price across property age categories.
- Number of properties in each age category.
- Average and median prices of renovated and non-renovated properties.
- Average price per square foot across renovation categories.

These comparisons provide an initial understanding of property characteristics and valuation patterns.

## 17. Output Files

The project generates the following output files:

| File Name | Description |
|---|---|
| `house_sales_cleaned.csv` | Cleaned and feature-engineered dataset |
| `house_sales_summary_statistics.csv` | Descriptive statistical summary |
| `house_sales_outlier_summary.csv` | IQR-based outlier summary |
| `property_age_summary.csv` | Property age category analysis |
| `renovation_summary.csv` | Renovation-based price comparison |
| `house_sales_engineered_features.csv` | Selected engineered property features |

## 18. GitHub Repository Structure

```text
Week-09-House-Sales-Data-Cleaning/
│
├── House_Sales_Data_Cleaning_Feature_Engineering.ipynb
├── README.md
│
├── data/
│   ├── kc_house_data.csv
│   └── house_sales_cleaned.csv
│
└── reports/
    ├── house_sales_summary_statistics.csv
    ├── house_sales_outlier_summary.csv
    ├── property_age_summary.csv
    └── house_sales_engineered_features.csv
```

## 19. Expected Learning Outcomes

After completing this project, learners will be able to:

- Understand and inspect real-estate datasets using Pandas.
- Identify and handle missing values and duplicate records.
- Clean invalid property measurements.
- Convert date columns into datetime format.
- Extract temporal features from sale dates.
- Calculate property age using construction and sale years.
- Create renovation-related features.
- Calculate price per square foot for living and lot areas.
- Detect potential outliers using the IQR method.
- Visualize property price distributions.
- Export cleaned datasets and analytical reports.

## 20. Conclusion

Week 9 focuses on preparing real-estate sales data through data cleaning, preprocessing, and feature engineering.

The project transforms raw King County house sales records into a structured dataset containing cleaned property attributes, sale date features, property age, renovation information, and price-per-square-foot metrics.

The cleaned dataset and generated reports provide a foundation for Week 10, which focuses on house price visualization, spatial analytics, valuation patterns, and real-estate insights.


