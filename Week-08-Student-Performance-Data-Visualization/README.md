# Week 8 – Student Performance Visualization, Demographic Analysis and Educational Insights

## 1. Project Overview

Week 8 focuses on analyzing and visualizing student examination performance using Python. This project builds upon the cleaned and feature-engineered dataset prepared in Week 7.

The analysis explores relationships between student performance and demographic and educational factors such as gender, race/ethnicity, parental education, lunch type, and test preparation course.

Using data visualization and statistical summaries, the project aims to identify patterns, compare subject-wise performance, and generate meaningful educational insights.

## 2. Dataset Information

**Dataset Name:** Student Performance in Exams

**Input Dataset:** `student_performance_processed.csv`

The cleaned dataset contains student demographic information and examination scores.

### Important Columns

| Column | Description |
|---|---|
| gender | Gender of the student |
| race_ethnicity | Race/ethnicity group |
| parental_level_of_education | Parent's highest education level |
| lunch | Type of lunch received |
| test_preparation_course | Test preparation course status |
| math_score | Mathematics examination score |
| reading_score | Reading examination score |
| writing_score | Writing examination score |
| total_score | Combined score of all three subjects |
| average_score | Average score across three subjects |
| percentage | Overall examination percentage |
| pass_fail_status | Student's pass/fail classification |
| performance_category | Overall performance category |

## 3. Objectives

- Analyze student examination performance across demographic groups.
- Compare Mathematics, Reading, and Writing scores.
- Study the relationship between parental education and student performance.
- Examine performance differences by lunch type.
- Analyze the relationship between test preparation and examination scores.
- Visualize score distributions using appropriate charts.
- Identify correlations between subject scores.
- Generate meaningful educational insights from the dataset.

## 4. Tools and Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 5. Data Understanding

The cleaned dataset was loaded into Google Colab and examined to understand its structure.

The following activities were performed:

- Displayed the first and last records.
- Checked dataset dimensions.
- Examined column names and data types.
- Checked missing values.
- Reviewed categorical variables.
- Generated descriptive statistical summaries.

## 6. Demographic Performance Analysis

Student performance was compared across different demographic categories.

### Gender-wise Analysis

- Compared average Mathematics scores.
- Compared average Reading scores.
- Compared average Writing scores.
- Visualized subject-wise performance using grouped bar charts.

### Race/Ethnicity Analysis

- Calculated average scores for each race/ethnicity group.
- Compared performance across the three subjects.
- Visualized group-wise score differences.

### Parental Education Analysis

- Examined student scores based on parental education levels.
- Compared subject-wise averages.
- Identified differences in score distributions.

### Lunch Type Analysis

- Compared student scores across lunch categories.
- Examined the distribution of examination scores.
- Visualized differences using grouped bar charts and boxplots.

## 7. Test Preparation Course Analysis

The relationship between test preparation course status and examination performance was explored.

Activities included:

- Calculating average Mathematics scores.
- Calculating average Reading scores.
- Calculating average Writing scores.
- Comparing students who completed and did not complete test preparation.
- Visualizing average scores using bar charts.
- Comparing score distributions using boxplots.

## 8. Data Visualization Techniques

The following visualizations were created:

| Visualization | Purpose |
|---|---|
| Grouped Bar Chart | Compare subject averages across demographic groups |
| Boxplot | Examine score distributions and outliers |
| Correlation Heatmap | Identify relationships between subject scores |
| Bar Chart | Compare average scores across educational categories |
| Score Distribution Plots | Understand variation in student performance |

## 9. Correlation Analysis

Correlation analysis was performed to understand relationships between Mathematics, Reading, and Writing scores.

A correlation matrix and heatmap were generated to identify positive or negative relationships between the examination subjects.

A positive correlation indicates that higher scores in one subject tend to be associated with higher scores in another subject.

Correlation does not establish causation.

## 10. Key Insights and Findings

The analysis provides a basis for investigating:

- Differences in subject-wise performance across gender groups.
- Score variations across race/ethnicity categories.
- Associations between parental education and examination scores.
- Performance patterns across lunch categories.
- Differences between students who completed test
