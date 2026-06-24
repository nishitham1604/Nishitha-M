# Exploratory-Data-Analysis-EDA-and-predictive-modelling-using-Python

A notebook covering statistics and ML concepts using the California Housing dataset:  

Outlier detection via boxplots and IQR fences 

Correlation analysis (heatmap, Chi-Square test on binned categorical features) 

Simple linear regression: predicting median house value from median income 

Live prediction demo with linear regression 


# 🏠 California Housing — Exploratory Data Analysis (EDA)

> **MBA in AI & Data Analytics | SVYASA University**  
> Course: Data Analysis using Python  
> Dataset: `california_housing_test.csv` (California Housing Dataset)


## 📌 Project Overview

End-to-end EDA on California housing data covering data profiling, statistical testing, and predictive modelling using Python.


## 📊 Analysis Sections

| # | Section | Techniques |
|---|---------|-----------|
| 1 | **Data Loading & Inspection** | `head()`, `shape`, `info()`, `describe()` |
| 2 | **Data Quality Check** | Null values, duplicates |
| 3 | **Univariate Analysis** | Histograms, Box plots (outlier detection) |
| 4 | **Bivariate Analysis** | Correlation matrix, Heatmap |
| 5 | **Income Distribution** | `histplot`, KDE, Mean/Median/Mode |
| 6 | **Central Limit Theorem** | Bootstrap sampling (n=1000, sample size=30) |
| 7 | **Covariance & Correlation** | `median_income` vs `median_house_value` |
| 8 | **T-Test** | High vs Low income neighborhoods |
| 9 | **ANOVA** | House prices across Young / Middle / Old housing age groups |
| 10 | **Chi-Square Test** | Association between age group and income group |
| 11 | **Linear Regression** | Predicting house value from median income |


## 🔑 Key Findings

- **T-Test**: p-value ≈ 0.000001 < 0.05 → House prices differ significantly between high and low income areas. *(H₀ rejected)*
- **Correlation**: Positive correlation between `median_income` and `median_house_value`
- **Linear Regression**: Model equation → `House Value = β₀ + β₁ × Income`; evaluated using R² and RMSE
- **Extrapolation Warning**: Feeding extreme values (e.g., income = 30,000) produces absurd predictions — model is only valid within training range


## 📈 Dataset Features

| Column | Description |
|--------|-------------|
| `longitude` | Geographic longitude |
| `latitude` | Geographic latitude |
| `housing_median_age` | Median age of houses in block |
| `total_rooms` | Total rooms in block |
| `total_bedrooms` | Total bedrooms in block |
| `population` | Block population |
| `households` | Number of households |
| `median_income` | Median household income (in $10,000s) |
| `median_house_value` | Median house value (target variable) |

CAPSTONE REPORT: California Housing Analysis
=============================================

1. PROBLEM STATEMENT
What drives median house value across California block groups?

2. DATA OVERVIEW
- 3000 rows, 9 columns, california_housing_test.csv
- No duplicate rows; total_bedrooms had some missing values, imputed with median
  
3. KEY EDA FINDINGS
- median_income is right-skewed
- median_income and median_house_value show a strong positive correlation (r ~ 0.68)
  
4. STATISTICAL TESTS
- t-test: high vs low income groups differ significantly in house value (p < 0.001)
- ANOVA: house value differs significantly across housing age groups (p < 0.05)
- Chi-Square: age_group and income_group show a significant association (p < 0.05)
  
5. PREDICTIVE MODEL
- Linear Regression: median_house_value ~ median_income
- R-squared on test set: 0.47 RMSE: ~$83,000
  
6. RECOMMENDATION
- Income is the strongest available driver of house value; further models should add
location-based features (longitude/latitude) to improve prediction accuracy.

7. LIMITATIONS
- Single-predictor model leaves much variance unexplained
- Correlation does not establish causation between income and house value
  

## 👤 

**Nishitha M**  
MBA — AI & Data Analytics (SAS)| SVYASA University, Bengaluru  
📧🔗https://www.linkedin.com/in/nishitha-m-3725b540a?utm_source=share_via&utm_content=profile&utm_medium=member_android


**Supervised by**
**Aishwarya Mishra** — AI Researcher
