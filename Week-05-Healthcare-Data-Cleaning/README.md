# Week 5: Healthcare Data Understanding, Cleaning & Exploratory Analysis

## 1. Project Overview

This project focuses on understanding, cleaning and performing Exploratory Data Analysis (EDA) on healthcare patient records using Python.

The dataset contains patient demographic details, blood groups, medical conditions, admission dates, doctor information, hospital details, insurance providers and billing amounts.

The main objective is to improve data quality, identify patterns in healthcare records and prepare a cleaned dataset for further visualization and analysis.

## 2. Problem Statement

Healthcare datasets contain large amounts of patient information that may include missing values, duplicate records, inconsistent categorical values and numerical irregularities.

Analyzing raw healthcare data without proper preprocessing can lead to inaccurate results.

This project applies data cleaning, transformation and exploratory analysis techniques to understand patient demographics, medical conditions, admission patterns, insurance providers and healthcare billing information.

## 3. Objectives

- Understand the structure and characteristics of healthcare data.
- Identify and handle missing values.
- Detect and remove duplicate records.
- Standardize categorical attributes.
- Convert date and numerical columns into appropriate data types.
- Create age groups for demographic analysis.
- Analyze patient distribution by gender and blood type.
- Examine medical conditions and admission patterns.
- Analyze billing amounts across medical conditions.
- Compare billing amounts across insurance providers.
- Prepare a preprocessed dataset for Week 6.

## 4. Dataset Information

**Dataset Name:** Healthcare Dataset

**Source:** Kaggle

**Dataset Link:** https://www.kaggle.com/datasets/prasad22/healthcare-dataset

**Total Records:** 49,992

**Total Attributes:** 10

### Dataset Attributes

| Column Name | Description |
|---|---|
| Name | Patient name |
| Age | Patient age |
| Gender | Patient gender |
| Blood Type | Patient blood group |
| Medical Condition | Patient's recorded medical condition |
| Date of Admission | Hospital admission date |
| Doctor | Doctor's name |
| Hospital | Hospital name |
| Insurance Provider | Patient's insurance provider |
| Billing Amount | Patient's healthcare billing amount |

## 5. Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 6. Project Workflow

### 6.1 Data Understanding

- Load the healthcare dataset using Pandas.
- Examine the number of rows and columns.
- Inspect column names and data types.
- Generate descriptive statistical summaries.
- Understand the distribution of numerical and categorical attributes.

### 6.2 Data Cleaning

- Standardize column names into lowercase format.
- Remove leading and trailing spaces from categorical values.
- Identify missing values and calculate missing percentages.
- Detect duplicate records.
- Remove exact duplicate records.
- Convert age and billing amount into numerical formats.
- Convert admission dates into datetime format.
- Handle missing numerical and categorical values.
- Investigate invalid age and negative billing values.

### 6.3 Feature Engineering

Create an additional feature called `age_group` to categorize patients.

Age groups:

- 0–18
- 19–35
- 36–59
- 60+

This feature helps compare patient demographics across different age categories.

Additional feature:

- `admission_year` – Extracted from the date of admission to analyze yearly admission patterns.

### 6.4 Patient Demographic Analysis

Analyze patient distribution based on:

- Gender
- Age groups
- Blood types

### 6.5 Medical Condition Analysis

- Calculate patient counts for each medical condition.
- Identify commonly recorded medical conditions.
- Compare medical-condition distribution across patient records.

### 6.6 Admission Date Analysis

- Convert admission dates into datetime format.
- Extract admission year.
- Analyze yearly patient admission patterns.
- Visualize admission trends over time.

### 6.7 Insurance Provider Analysis

- Calculate patient counts for each insurance provider.
- Compare insurance provider distributions.
- Examine billing amounts across insurance providers.

### 6.8 Healthcare Billing Analysis

Calculate:

- Average billing amount.
- Median billing amount.
- Minimum billing amount.
- Maximum billing amount.
- Total billing amount.
- Billing distribution by medical condition.
- Billing distribution by insurance provider.

Investigate negative billing values and unusual observations before drawing conclusions.

## 7. Exploratory Data Analysis and Visualizations

The following visualizations are created:

1. Patient Distribution by Gender.
2. Patient Distribution by Blood Type.
3. Patient Distribution by Age Group.
4. Patient Count by Medical Condition.
5. Patient Admissions by Year.
6. Patient Distribution by Insurance Provider.
7. Healthcare Billing Amount Distribution.
8. Average Billing Amount by Medical Condition.
9. Billing Amount by Insurance Provider.

## 8. Expected Deliverables

- Healthcare Data Cleaning and Analysis Jupyter Notebook.
- Preprocessed Healthcare Dataset.
- Healthcare Summary Report.
- Condition-wise Billing Summary.
- Insurance-wise Billing Summary.
- Exploratory Data Analysis Visualizations.

## 9. GitHub Folder Structure

```text
Week-05-Healthcare-Data-Cleaning/
│
├── Healthcare_Data_Cleaning_Analysis.ipynb
│
├── README.md
│
├── data/
│   ├── healthcare_dataset.csv
│   └── healthcare_preprocessed.csv
│
└── reports/
    ├── healthcare_summary.csv
    ├── condition_billing_summary.csv
    └── insurance_billing_summary.csv
