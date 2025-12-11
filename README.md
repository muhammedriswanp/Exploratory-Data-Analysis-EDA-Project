# 📊 Exploratory Data Analysis (EDA) Project

**Duration:** 5 Days  
**Mode:** Individual Project  
**Focus:** Exploratory Analysis of the [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

## 1. Project Overview
In this project, I perform a complete Exploratory Data Analysis (EDA) on a real-world dataset. The goal is to demonstrate core and intermediate EDA skills, Git discipline, and the ability to communicate insights clearly through notebook documentation.

## 2. Learning Objectives
By the end of this project, the following objectives are met:
* Understand raw datasets and business context
* Perform systematic data cleaning
* Handle missing values and outliers
* Conduct univariate and bivariate analysis
* Perform basic statistical tests
* Engineer new features for modeling
* Document workflow clearly in notebooks
* Maintain a clean GitHub repository with daily pushes

## 📁 Repository Structure

```text
eda-project/
│
├── data/
│   ├── raw/                     # Original dataset
│   ├── interim/                 # Cleaned dataset (Day 2)
│   └── processed/               # Final dataset (Day 4)
│
├── notebooks/
│   ├── 01_data_overview.ipynb
│   ├── 02_cleaning_preprocessing.ipynb
│   ├── 03_univariate_bivariate_eda.ipynb
│   └── 04_stats_time_features_final_insights.ipynb
│
├── reports/
│   └── figures/                 # Exported plots
│
└── README.md

✔ Day 1 — Initial Setup & Profiling
Tasks Completed

[x] Added project folder structure.

[x] Uploaded raw dataset to data/raw/.

[x] Created notebook 01_data_overview.ipynb.

[x] Performed initial inspection: .head(), .info(), .describe(), .nunique().

[x] Identified Numerical & Categorical columns.

[x] Analyzed missing values & class distribution.

[x] Created Data Quality Issue Log.

Key Findings

Missing Values: 201 missing BMI values.

Data Quality: 1 gender entry = “Other”; Work type labels inconsistent.

Hidden Missing: Smoking status contains “Unknown” (30%).

Imbalance: Severe class imbalance (stroke cases ≈ 4.8%).

✔ Day 2 — Cleaning, Imputation & Outliers
Tasks Completed

[x] Fix Datatypes: Removed irrelevant column id.

[x] Standardize: Dropped rare gender value (“Other”) & standardized labels (work_type, smoking_status).

[x] Optimization: Converted selected columns to category dtype.

[x] Imputation: Filled missing BMI values using the median.

[x] Duplicates: Checked for duplicates (none found).

[x] Outliers: Performed detection using IQR for BMI and Glucose (decided to keep them).

[x] Save Data: Saved cleaned dataset to: data/interim/cleaned_day2.csv.