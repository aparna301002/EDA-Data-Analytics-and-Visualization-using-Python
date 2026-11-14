# Week 14: Hotel Booking Visualization, Revenue Management & Hospitality Insights

## Project Overview

This project focuses on analyzing hotel booking data to understand booking demand, cancellation patterns, seasonal trends, and revenue performance.

Using Python, Pandas, Matplotlib, and Seaborn, the project compares City Hotels and Resort Hotels, examines cancellation rates across market segments, analyzes booking lead times, and identifies monthly variations in arrivals and Average Daily Rate (ADR).

The final objective is to provide actionable revenue management recommendations that help hotels improve pricing strategies, reduce cancellation risks, and prepare for seasonal demand fluctuations.

## Dataset

**Dataset Name:** Hotel Booking Demand Dataset

**Source:** Preprocessed dataset from Week 13

**Input File:** `hotel_bookings_cleaned.csv`

The dataset contains hotel reservation information, including:

- Hotel type (City Hotel and Resort Hotel)
- Booking cancellation status
- Lead time
- Arrival date and month
- Market segment
- Average Daily Rate (ADR)
- Reservation status
- Total number of nights
- Guest and booking information

## Problem Statement

Hotel management needs visual analytics to optimize pricing strategies, reduce cancellation risks, and plan for seasonal demand surges.

The project analyzes booking behavior, cancellation patterns, monthly demand, and ADR fluctuations to support better hospitality and revenue management decisions.

## Objectives

1. Compare booking demand and cancellation patterns between City Hotels and Resort Hotels.
2. Analyze cancellation rates across different market segments.
3. Examine the relationship between booking lead time and cancellation rates.
4. Identify monthly seasonality trends in hotel arrivals.
5. Analyze Average Daily Rate (ADR) fluctuations across different months.
6. Compare revenue performance between hotel types.
7. Generate actionable recommendations for pricing optimization and cancellation management.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Data Preparation

The preprocessed dataset from Week 13 is used as the input for this analysis.

The following preparation steps are performed:

- Load the cleaned hotel booking dataset.
- Inspect dataset dimensions and column information.
- Standardize and validate column names.
- Convert relevant columns into appropriate data types.
- Prepare arrival dates and monthly fields for time-based analysis.
- Create cancellation status labels.
- Prepare data for hotel-wise, market-segment-wise, and monthly comparisons.
- Filter completed reservations for the estimated revenue analysis.

## Analysis and Visualizations

### 1. Hotel Booking Demand Analysis

- Compare total bookings between City Hotels and Resort Hotels.
- Visualize booking distribution by hotel type.
- Identify differences in booking demand.

### 2. Cancellation Analysis

- Calculate cancellation rates for each hotel type.
- Compare cancellation rates across market segments.
- Analyze cancellation patterns by hotel type and market segment.
- Identify segments with higher cancellation rates.

### 3. Lead Time Analysis

- Compare lead time distributions for canceled and non-canceled reservations.
- Use box plots to identify differences in booking lead times.
- Group reservations by lead-time ranges.
- Analyze cancellation rates across lead-time groups.

### 4. Monthly Arrival Trend Analysis

- Calculate monthly hotel arrival counts.
- Compare arrival trends across different years.
- Visualize seasonal booking demand using line charts.
- Identify months with higher and lower arrival activity.

### 5. Average Daily Rate (ADR) Analysis

- Calculate monthly ADR.
- Compare ADR fluctuations across years.
- Analyze ADR patterns for City Hotels and Resort Hotels.
- Identify months with relatively higher and lower room rates.

### 6. Hotel Revenue Analysis

- Estimate revenue using ADR multiplied by total nights.
- Include completed reservations in the revenue estimate.
- Compare estimated revenue between hotel types.
- Generate hotel-wise revenue summaries.

### 7. Executive Revenue Management Report

Generate a report containing:

- Hotel-wise booking demand.
- Hotel cancellation comparisons.
- Market segments with higher cancellation rates.
- Lead-time cancellation patterns.
- Peak arrival months.
- Monthly ADR trends.
- Estimated revenue comparisons.
- Pricing optimization recommendations.
- Cancellation management strategies.
- Overbooking protection recommendations.

## Key Deliverables

The notebook generates the following reports in the `week14_reports` folder:

| Report File | Description |
|---|---|
| `hotel_demand_summary.csv` | Booking demand by hotel type |
| `hotel_cancellation_summary.csv` | Cancellation rate by hotel |
| `market_segment_cancellation.csv` | Cancellation rate by market segment |
| `segment_hotel_cancellation.csv` | Segment-wise cancellation comparison by hotel |
| `monthly_arrival_summary.csv` | Monthly arrival trends |
| `monthly_adr_summary.csv` | Monthly ADR analysis |
| `lead_time_summary.csv` | Lead-time distribution summary |
| `lead_time_cancellation_summary.csv` | Cancellation rate by lead-time group |
| `hotel_monthly_demand.csv` | Monthly demand by hotel type |
| `hotel_monthly_adr.csv` | Monthly ADR by hotel type |
| `hotel_revenue_summary.csv` | Estimated revenue by hotel |
| `executive_revenue_management_report.txt` | Final executive analysis and recommendations |

## Expected Outcomes

After completing this project, the analysis will help:

- Understand booking demand differences between City and Resort Hotels.
- Identify market segments with higher cancellation rates.
- Understand how booking lead time relates to cancellation behavior.
- Identify seasonal patterns in hotel arrivals.
- Examine monthly ADR fluctuations.
- Compare estimated revenue across hotel types.
- Develop data-driven pricing and cancellation management strategies.

## Business Recommendations

Based on the actual results generated by the notebook, hotel management can consider the following strategies:

1. **Pricing Optimization:** Adjust room rates according to seasonal demand and observed ADR trends.
2. **Cancellation Management:** Monitor market segments with higher cancellation rates and review their booking policies.
3. **Lead-Time Management:** Use historical cancellation patterns to improve reservation monitoring and targeted confirmation strategies.
4. **Seasonal Planning:** Prepare staffing and room availability according to monthly arrival trends.
5. **Overbooking Protection:** Consider cautious overbooking policies only after evaluating historical cancellations, no-shows, room inventory, and booking patterns.
6. **Revenue Improvement:** Compare hotel-wise revenue estimates to identify opportunities for better pricing and demand management.

## Project Folder Structure

```text
Week-14-Hotel-Booking-Revenue-Management/
│
├── Hotel_Booking_Revenue_Management_Analysis.ipynb
│
├── README.md
│
├── data/
│   └── hotel_bookings_cleaned.csv
│
└── reports/
    ├── hotel_demand_summary.csv
    ├── hotel_cancellation_summary.csv
    ├── market_segment_cancellation.csv
    ├── segment_hotel_cancellation.csv
    ├── monthly_arrival_summary.csv
    ├── monthly_adr_summary.csv
    ├── lead_time_summary.csv
    ├── lead_time_cancellation_summary.csv
    ├── hotel_monthly_demand.csv
    ├── hotel_monthly_adr.csv
    ├── hotel_revenue_summary.csv
    └── executive_revenue_management_report.txt
```

## Important Notes and Limitations

- The analysis uses the preprocessed dataset generated in Week 13.
- Revenue is estimated using ADR multiplied by total nights; it is not actual accounting revenue.
- Completed reservations are identified using the `Check-Out` reservation status.
- Room inventory data is not available, so occupancy rate and RevPAR cannot be reliably calculated.
- Monthly trends should be interpreted alongside year-wise comparisons.
- Overbooking recommendations should be validated against actual room availability and operational constraints.
- The analysis identifies historical relationships and patterns; it does not guarantee future booking or revenue outcomes.

## Conclusion

This project demonstrates how Python-based exploratory data analysis and visualization can support hotel revenue management.

By examining booking demand, cancellation behavior, lead time, monthly arrivals, and ADR fluctuations, the analysis provides useful insights for pricing optimization, seasonal planning, and cancellation risk management.

The final executive report translates the analytical findings into practical recommendations for improving hotel operations and revenue management.

