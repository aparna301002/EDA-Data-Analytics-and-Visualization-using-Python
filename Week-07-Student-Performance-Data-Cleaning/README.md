# Week 7: Student Performance Data Understanding, Cleaning and Feature Engineering

## Project Overview

This project focuses on understanding, cleaning and performing feature engineering on the Student Performance in Exams dataset using Python.

The dataset contains student demographic information and examination scores in Mathematics, Reading and Writing. The project involves inspecting the dataset, cleaning categorical attributes, calculating statistical measures, creating meaningful performance-related features and identifying potential outliers.

The main objective is to transform raw student examination records into a structured dataset that can be used for further academic performance analysis.

## Dataset Information

**Dataset Name:** Student Performance in Exams

**Input File:** `StudentsPerformance.csv`

**Dataset Attributes:**

| Column Name | Description |
|---|---|
| gender | Gender of the student |
| race_ethnicity | Student's race/ethnicity group |
| parental_level_of_education | Parent's education qualification |
| lunch | Type of lunch provided |
| test_preparation_course | Test preparation course completion status |
| math_score | Mathematics examination score |
| reading_score | Reading examination score |
| writing_score | Writing examination score |

## Objectives

- Inspect student demographic attributes and examination score variables.
- Identify missing values and duplicate records.
- Clean and standardize categorical features.
- Convert subject score columns into appropriate numeric data types.
- Calculate mean, median, standard deviation, variance and quartiles.
- Create Total Score and Average Score features.
- Calculate overall student performance percentage.
- Generate Pass/Fail Status based on subject-wise passing criteria.
- Classify students into performance categories.
- Detect potential outliers across Mathematics, Reading and Writing scores using IQR and Z-score methods.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Data Cleaning and Preprocessing

### 1. Dataset Understanding

- Loaded the Student Performance dataset using Pandas.
- Examined the first and last five records.
- Checked the number of rows and columns.
- Inspected column names and data types.
- Generated basic dataset information.

### 2. Missing Value Analysis

- Identified missing values in each column.
- Calculated missing value percentages.
- Checked missing values in examination score columns.
- Handled missing numerical scores using median imputation when necessary.

### 3. Duplicate Handling

- Identified duplicate records.
- Counted duplicate observations.
- Removed exact duplicate records.

### 4. Categorical Data Cleaning

The following categorical attributes were standardized:

- Gender
- Race/Ethnicity
- Parental Level of Education
- Lunch
- Test Preparation Course

Text formatting operations included:

- Removing leading and trailing spaces.
- Removing unnecessary repeated spaces.
- Standardizing text capitalization.

### 5. Numerical Data Conversion

The following columns were converted into numeric data types:

- Math Score
- Reading Score
- Writing Score

Score validation was performed to identify values outside the expected 0–100 range.

## Statistical Analysis

Descriptive statistical measures were calculated for all three examination subjects.

The following measures were analyzed:

- Count
- Mean
- Median
- Standard Deviation
- Variance
- Minimum
- Maximum
- First Quartile (Q1)
- Second Quartile (Q2)
- Third Quartile (Q3)

These measures help understand the central tendency and dispersion of student examination scores.

## Feature Engineering

New features were created using the existing examination score columns.

### 1. Total Score

Calculates the combined marks obtained in all three subjects.

**Formula:**

Total Score = Math Score + Reading Score + Writing Score

Maximum possible score: 300.

### 2. Average Score

Calculates the average performance across the three subjects.

**Formula:**

Average Score = Total Score / 3

### 3. Percentage

Calculates the overall examination percentage.

**Formula:**

Percentage = (Total Score / 300) × 100

### 4. Pass/Fail Status

Students were classified based on their scores in all three subjects.

For this project, a minimum passing mark of 40 in each subject was assumed.

- Pass: Student scores at least 40 in all three subjects.
- Fail: Student scores below 40 in at least one subject.

### 5. Performance Category

Students were grouped according to their average scores.

| Average Score | Performance Category |
|---|---|
| 90 and above | Excellent |
| 75–89.99 | Very Good |
| 60–74.99 | Good |
| 40–59.99 | Average |
| Below 40 | Below Average |

These are project-defined categories for exploratory analysis.

## Data Visualization

Histograms and boxplots were generated to understand examination score distributions.

### Visualizations Created

- Mathematics score distribution using a histogram.
- Reading score distribution using a histogram.
- Writing score distribution using a histogram.
- Subject-wise score comparison using a bar chart.
- Outlier identification across all three subjects using boxplots.

These visualizations help identify score patterns, score variation and unusual observations.

## Outlier Detection

Potential outliers were identified using two statistical techniques.

### 1. Interquartile Range (IQR)

The IQR method was used to identify scores outside the lower and upper statistical bounds.

**Formulas:**

IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR

The number of potential outliers was calculated separately for Mathematics, Reading and Writing.

### 2. Z-Score Method

Z-scores were calculated to measure how far individual examination scores deviate from their respective subject means.

**Formula:**

Z = (X - Mean) / Standard Deviation

Observations with an absolute Z-score greater than 3 were identified as potential outliers.

Potential outliers were retained for investigation rather than automatically deleted.

## Performance Summary

The following performance indicators were calculated:

- Total number of students.
- Average Mathematics score.
- Average Reading score.
- Average Writing score.
- Average Total Score.
- Average Percentage.
- Number of Pass students.
- Number of Fail students.
- Highest Total Score.
- Lowest Total Score.

## Output Files

The following output files were generated.

| File Name | Description |
|---|---|
| `student_performance_processed.csv` | Cleaned dataset with engineered features |
| `subject_statistics.csv` | Statistical summary of subject scores |
| `student_score_outlier_summary.csv` | Outlier analysis using the IQR method |
| `pass_fail_summary.csv` | Student Pass/Fail count summary |

## Project Folder Structure

```text
Week-07-Student-Performance/
│
├── Student_Performance_Cleaning_Feature_Engineering.ipynb
│
├── README.md
│
├── data/
    ├── student_performance_processed.csv
│   └── StudentsPerformance.csv
│
└── reports/
    ├── subject_statistics.csv
    ├── student_score_outlier_summary.csv
    └── pass_fail_summary.csv
```

## Expected Outcomes

After completing this project, the analysis provides:

- A better understanding of student demographic attributes.
- Clean and standardized categorical data.
- Statistical summaries of Mathematics, Reading and Writing scores.
- Derived features representing overall student performance.
- Student Pass/Fail classification.
- Performance category classification.
- Identification of potential score outliers using IQR and Z-score methods.
- A structured dataset ready for further demographic and educational equity analysis.

## Conclusion

This project demonstrates the application of Python for student performance data cleaning and feature engineering.

Using Pandas and NumPy, the dataset was inspected, standardized and transformed into meaningful performance-related features. Statistical analysis was performed to understand score distributions, while IQR and Z-score techniques were used to identify potential outliers.

The processed dataset provides a foundation for Week 8, which focuses on student performance visualization, demographic analysis, educational equity and the impact of parental education and test preparation courses.

