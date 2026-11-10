# Week 6: Healthcare Data Visualization and Exploratory Data Analysis (EDA) Using Python

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on a cleaned healthcare dataset using Python. The analysis explores patient demographics, medical conditions, admission trends, insurance providers and billing patterns.

The cleaned dataset generated during Week 5 is used as the input for this analysis. Various statistical techniques and data visualization methods are applied to identify meaningful patterns, distributions and relationships within the healthcare data.

## Dataset Information

**Dataset Name:** Healthcare Dataset

**Input File:** `healthcare_preprocessed.csv`

**Total Records:** 49,992

**Original Columns:** 10

### Dataset Attributes

| Column Name | Description |
|---|---|
| Name | Patient name |
| Age | Age of the patient |
| Gender | Gender of the patient |
| Blood Type | Patient's blood group |
| Medical Condition | Medical condition of the patient |
| Date of Admission | Date on which the patient was admitted |
| Doctor | Name of the doctor |
| Hospital | Name of the hospital |
| Insurance Provider | Patient's insurance provider |
| Billing Amount | Amount billed for the healthcare service |

## Objectives

- Understand the structure and characteristics of the cleaned healthcare dataset.
- Perform descriptive statistical analysis.
- Analyze patient age and gender distributions.
- Explore blood group and medical condition distributions.
- Analyze admission patterns by year and month.
- Examine healthcare billing distributions.
- Compare billing amounts across medical conditions.
- Analyze billing patterns across insurance providers.
- Identify potential outliers using statistical methods.
- Study relationships between numerical variables.
- Generate meaningful healthcare insights through visualizations.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Exploratory Data Analysis

### 1. Dataset Understanding

- Loaded the cleaned healthcare dataset.
- Examined the first and last records.
- Checked dataset dimensions and column names.
- Reviewed data types and dataset information.
- Generated descriptive statistical summaries.

### 2. Univariate Analysis

Analyzed individual variables to understand their distributions.

Visualizations created:

- Patient age distribution using a histogram.
- Gender distribution using a pie chart.
- Blood group distribution using a count plot.
- Medical condition distribution using a count plot.
- Insurance provider distribution using a count plot.

### 3. Bivariate Analysis

Examined relationships between two variables.

Visualizations created:

- Age distribution by gender using a boxplot.
- Medical conditions by gender using a count plot.
- Average billing amount by medical condition using a bar chart.
- Average billing amount by insurance provider using a bar chart.
- Relationship between age and billing amount using a scatter plot.

### 4. Multivariate Analysis

Examined multiple numerical and categorical variables together.

Analysis performed:

- Correlation analysis using a heatmap.
- Patient classification into age groups.
- Medical condition distribution across different age groups.

Age groups created:

- 0–18
- 19–35
- 36–59
- 60+

### 5. Admission Date Analysis

The admission date column was converted into datetime format.

Additional features created:

- Admission Year
- Admission Month

Visualizations created:

- Year-wise patient admissions using a line chart.
- Month-wise patient admissions using a bar chart.

### 6. Outlier Analysis

The Interquartile Range (IQR) method was used to identify potential outliers in billing amounts.

Statistical measures calculated:

- First Quartile (Q1)
- Third Quartile (Q3)
- Interquartile Range (IQR)
- Lower Bound
- Upper Bound

A boxplot was also generated to visualize the distribution and potential outliers.

Potential outliers were identified for further investigation rather than automatically removed.

### 7. Billing Analysis

Analyzed healthcare billing patterns using:

- Billing amount distribution.
- Billing amount by gender.
- Average billing by medical condition.
- Average billing by insurance provider.
- Minimum, maximum and average billing amounts.

## Key Performance Indicators

The following metrics were calculated:

- Total patient records.
- Average patient age.
- Most common gender.
- Most common blood group.
- Most common medical condition.
- Most common insurance provider.
- Average billing amount.
- Maximum billing amount.
- Minimum billing amount.
- Year with the highest admission count.

## Output Files

The following files were generated after completing the analysis.

| File Name | Description |
|---|---|
| `healthcare_week6_eda.csv` | Healthcare dataset with additional EDA features |
| `condition_billing_summary.csv` | Patient count and billing statistics by medical condition |
| `insurance_billing_summary.csv` | Patient count and billing statistics by insurance provider |

## Project Folder Structure

```text
Week-06-Healthcare-Data-Visualization/
│
├── Healthcare_Data_Visualization_EDA.ipynb
│
├── README.md
│
├── data/
│   └── healthcare_preprocessed.csv
│
└── reports/
    ├── condition_billing_summary.csv
    └── insurance_billing_summary.csv
```

## Expected Outcomes

After completing this project, the analysis provides an understanding of:

- Patient demographic patterns.
- Distribution of medical conditions.
- Blood group and insurance provider distributions.
- Admission trends over time.
- Healthcare billing patterns.
- Differences in average billing across medical conditions and insurance providers.
- Potential outliers in billing amounts.
- Relationships between numerical variables.

The visualizations and statistical summaries help communicate the characteristics of the healthcare dataset and support further exploratory investigation.

## Conclusion

This project demonstrates how Python can be used to perform Exploratory Data Analysis on healthcare data. Using Pandas, NumPy, Matplotlib and Seaborn, the cleaned dataset was explored through statistical summaries, univariate analysis, bivariate analysis, multivariate analysis, time-based analysis and outlier detection.

The analysis helps identify patterns in patient demographics, medical conditions, admission records and billing amounts. The generated visualizations and summary reports provide a foundation for further healthcare data analysis.
