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

##  Day 1 — Initial Setup & Profiling

**Tasks Completed**
* Added project folder structure.
* Uploaded raw dataset to `data/raw/`.
* Created notebook `01_data_overview.ipynb`.
* Performed initial inspection: `.head()`, `.info()`, `.describe()`, `.nunique()`.
* Identified Numerical & Categorical columns.
* Analyzed missing values & class distribution.
* Created **Data Quality Issue Log**.

**Key Findings**
* **Missing Values:** 201 missing BMI values.
* **Data Quality:** 1 gender entry = “Other”; Work type labels inconsistent.
* **Hidden Missing:** Smoking status contains “Unknown” (30%).
* **Imbalance:** Severe class imbalance (stroke cases ≈ 4.8%).

---

## ✔ Day 2 — Cleaning, Imputation & Outliers

**Tasks Completed**
* **Fix Datatypes:** Removed irrelevant column `id`.
* **Standardize:** Dropped rare gender value (“Other”) & standardized labels (`work_type`, `smoking_status`).
* **Optimization:** Converted selected columns to `category` dtype.
* **Imputation:** Filled missing `BMI` values using the median.
* **Duplicates:** Checked for duplicates (none found).
* **Outliers:** Performed detection using IQR for `BMI` and `Glucose` (decided to keep them).
* **Save Data:** Saved cleaned dataset to: `data/interim/cleaned_day2.csv`.

## Day 3 — Univariate & Bivariate EDA

**Data Loading & Setup**
* Loaded cleaned_day2.csv and converted key columns to categorical types.
* Set Seaborn theme for consistent visualizations.

**Univariate Analysis**
* **Age:** Most individuals are 30–60 years old.
* **BMI & Glucose:** Normal ranges with meaningful high outliers.
* **Categorical:** Stroke is rare (~5%), most people are married, private workers, and many have "Never Smoked".

**Numeric Relationships**
* **Age vs BMI:** Weak positive correlation (~0.32).
* **Age vs Glucose:** Weak positive trend.
* **Heatmap:** All correlations are weak indicating stroke depends on multiple factors.

**Stroke Comparisons**
* **Age:** Stroke patients are much older.
* **Glucose:** Stroke group has higher glucose levels.

**Categorical Insights**
* **Work Type vs BMI:** Private & govt workers show higher BMI.
* **Smoking / Gender:** Former smokers (especially males) have highest stroke rates.

**Age Group Segmentation**
* Created age groups: 0–20, 21–40, 41–60, 60+.
* Stroke rate increases sharply with age (highest in seniors).
* Middle-aged group has highest BMI.
* Young rarely smoke; middle-aged smoke most; seniors mostly former smokers.


## 📁 Repository Structure

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