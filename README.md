# Exploratory Data Analysis (EDA) Project

**Duration:** 5 Days  
**Mode:** Individual Project  
**Tools:** Python, pandas, numpy, matplotlib, seaborn, Jupyter Notebook, Git, GitHub  
**Dataset:** [Stroke Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

---

## 1. Project Overview
This project performs a complete Exploratory Data Analysis (EDA) on a real-world healthcare dataset related to stroke occurrence.

* **Objective:** To understand how demographic, medical, and lifestyle factors such as age, glucose level, BMI, hypertension, heart disease, and smoking behavior are associated with stroke risk.
* **Scope:** The project demonstrates structured EDA workflow, data cleaning, statistical testing, feature engineering, and clear documentation following industry-style Git discipline.

## 2. Instructions to Run
1. Clone the repository:
   ```bash
   git clone <your-github-repo-url>

2. Install required packages:
    ```bash
    pip install -r requirements.txt

3. Open the notebooks in order:

    01_data_overview.ipynb

    02_cleaning_preprocessing.ipynb

    03_univariate_bivariate_eda.ipynb

    04_stats_time_features_final_insights.ipynb

4. The final cleaned dataset is available in: data/processed/final_cleaned_day4.csv

## Repository Structure

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

## Day 1 — Initial Setup & Profiling
**Tasks Completed**

    Setup: Added project folder structure and uploaded raw dataset.

    Profiling: Created 01_data_overview.ipynb and performed initial inspection (.info(), .describe()).

    Analysis: Identified Numerical & Categorical columns and analyzed class imbalance.

    Logging: Created a Data Quality Issue Log.

**Key Findings**

    Missing Values: 201 missing BMI values.

    Data Quality: 1 gender entry = "Other"; inconsistent work type labels.

    Hidden Missing: Smoking status contains "Unknown" (30%).

## Day 2 — Cleaning, Imputation & Outliers
**Tasks Completed**

    Fix Datatypes: Removed irrelevant column id.

    Standardize: Dropped rare gender value ("Other") & standardized labels.

    Imputation: Filled missing BMI values using the median.

    Outliers: Performed detection using IQR for BMI and Glucose (decided to retain outliers).

    Export: Saved cleaned dataset to data/interim/cleaned_day2.csv.

## Day 3 — Univariate & Bivariate EDA
**Data Loading & Setup**

    Setup: Loaded cleaned_day2.csv and set Seaborn theme for consistent visualizations.

**Univariate Analysis**

    Age: Most individuals are 30–60 years old.

    BMI & Glucose: Normal ranges with meaningful high outliers.

    Categorical: Stroke is rare (~5%); most people are married, private workers, and have "Never Smoked".

**Numeric Relationships**

    Age vs BMI: Weak positive correlation (~0.32).

    Age vs Glucose: Weak positive trend.

    Heatmap: All correlations are weak, indicating stroke depends on multiple factors.

**Stroke Comparisons**

    Age: Stroke patients are significantly older.

    Glucose: Stroke group has higher glucose levels.

**Categorical Insights**

    Work Type: Private & Govt workers show higher BMI.

    Smoking/Gender: Former smokers (especially males) have highest stroke rates.

**Age Group Segmentation**

    Segmentation: Created groups: 0–20, 21–40, 41–60, 60+.

    Trend: Stroke rate increases sharply with age (highest in seniors).

    Habits: Young rarely smoke; Middle-aged smoke most; Seniors are mostly former smokers.

## Day 4 — Statistical Analysis & Feature Engineering
**Data Setup & Optimization**
    Setup: Loaded cleaned_day2.csv and converted objects to categories.

    Goal: Improved memory usage and processing speed for statistical tests.

**Numeric Hypothesis Testing**

    Glucose Baseline: Population mean is significantly higher than 100 mg/dL (p < 0.001).

    BMI vs Stroke: Stroke patients have significantly higher BMI than non-stroke group.

    Work Type: Average glucose levels differ significantly across work types.

**Categorical Hypothesis Testing**

    Hypertension: Strong statistical dependence found between hypertension and stroke.

    Smoking: Significant association exists between smoking habits and stroke risk.

    High Glucose: People with glucose >= 126 mg/dL show statistically higher stroke rates.

**Feature Engineering**

    Age Group: Segmented into Young, Adults, Middle-aged, Senior (Seniors = highest risk).

    High Glucose Flag: Created binary indicator for clinical diabetes threshold (>= 126 mg/dL).

    Medical Risk Score: Composite score (0–4) summing Hypertension, Heart Disease, Glucose, and Obesity.

    Interaction: Age_Glucose_Interaction created to capture high glucose risk in older age.

**Final Output**

    Export: Saved processed data to final_cleaned_day4.csv.

    Note: Time-series analysis skipped (no date column available).

## 3. Key Insights (Top 10 Summary)
    Rarity: Stroke cases are relatively rare in the dataset, requiring careful interpretation of group comparisons.

    Data Quality: Issues such as missing BMI values and categorical inconsistencies were successfully resolved.

    Age: Shows a strong relationship with stroke; cases are concentrated among older individuals.

    Distributions: Average glucose level and BMI distributions are right-skewed, indicating a small high-risk subgroup.

    Multifactorial Risk: Individual numeric features show weak correlations, suggesting risk arises from multiple combined factors.

    Comparison: Stroke patients are significantly older and have higher glucose levels than non-stroke individuals.

    Glucose Benchmark: Mean glucose level is significantly higher than the clinical normal benchmark of 100 mg/dL.

    Comorbidities: Stroke and heart disease patients have significantly higher BMI compared to their counterparts.

    Associations: Smoking status, hypertension, work type, and age group show statistically significant associations with stroke.

    Risk Stratification: Engineered features like Medical Risk Score highlight individuals with multiple conditions as the most vulnerable.

### Note
    The dataset does not contain a date or time column; therefore, time-based EDA was not performed.



# 📊 Exploratory Data Analysis (EDA) Project

**Duration:** 5 Days  
**Mode:** Individual Project  
**Focus:** Exploratory Analysis of the [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

---

## 1. Project Overview
In this project, I perform a complete Exploratory Data Analysis (EDA) on a real-world dataset. The goal is to demonstrate core and intermediate EDA skills, Git discipline, and the ability to communicate insights clearly through notebook documentation.

## 2. Learning Objectives
By the end of this project, the following objectives are met:
* Understand raw datasets and business context.
* Perform systematic data cleaning.
* Handle missing values and outliers.
* Conduct univariate and bivariate analysis.
* Perform basic statistical tests.
* Engineer new features for modeling.
* Document workflow clearly in notebooks.
* Maintain a clean GitHub repository with daily pushes.

---

## 📅 Day 1 — Initial Setup & Profiling

**Tasks Completed**
* **Setup:** Added project folder structure and uploaded raw dataset.
* **Profiling:** Created `01_data_overview.ipynb` and performed initial inspection (`.info()`, `.describe()`).
* **Analysis:** Identified Numerical & Categorical columns and analyzed class imbalance.
* **Logging:** Created a **Data Quality Issue Log**.

**Key Findings**
* **Missing Values:** 201 missing BMI values.
* **Data Quality:** 1 gender entry = "Other"; inconsistent work type labels.
* **Hidden Missing:** Smoking status contains "Unknown" (30%).

---

## 🧹 Day 2 — Cleaning, Imputation & Outliers

**Tasks Completed**
* **Fix Datatypes:** Removed irrelevant column `id`.
* **Standardize:** Dropped rare gender value ("Other") & standardized labels.
* **Imputation:** Filled missing `BMI` values using the median.
* **Outliers:** Performed detection using IQR for `BMI` and `Glucose` (decided to retain outliers).
* **Export:** Saved cleaned dataset to `data/interim/cleaned_day2.csv`.

---

## 📈 Day 3 — Univariate & Bivariate EDA

**Data Loading & Setup**
* **Setup:** Loaded `cleaned_day2.csv` and set Seaborn theme for consistent visualizations.

**Univariate Analysis**
* **Age:** Most individuals are 30–60 years old.
* **BMI & Glucose:** Normal ranges with meaningful high outliers.
* **Categorical:** Stroke is rare (~5%); most people are married, private workers, and have "Never Smoked".

**Numeric Relationships**
* **Age vs BMI:** Weak positive correlation (~0.32).
* **Age vs Glucose:** Weak positive trend.
* **Heatmap:** All correlations are weak, indicating stroke depends on multiple factors.

**Stroke Comparisons**
* **Age:** Stroke patients are significantly older.
* **Glucose:** Stroke group has higher glucose levels.

**Categorical Insights**
* **Work Type:** Private & Govt workers show higher BMI.
* **Smoking/Gender:** Former smokers (especially males) have highest stroke rates.

**Age Group Segmentation**
* **Segmentation:** Created groups: 0–20, 21–40, 41–60, 60+.
* **Trend:** Stroke rate increases sharply with age (highest in seniors).
* **Habits:** Young rarely smoke; Middle-aged smoke most; Seniors are mostly former smokers.

---

## 🧪 Day 4 — Statistical Analysis & Feature Engineering

**Data Setup & Optimization**
* **Setup:** Loaded `cleaned_day2.csv` and converted objects to categories.
* **Goal:** Improved memory usage and processing speed for statistical tests.

**Numeric Hypothesis Testing**
* **Glucose Baseline:** Population mean is significantly higher than 100 mg/dL ($p < 0.001$).
* **BMI vs Stroke:** Stroke patients have significantly higher BMI than non-stroke group.
* **Work Type:** Average glucose levels differ significantly across work types.

**Categorical Hypothesis Testing**
* **Hypertension:** Strong statistical dependence found between hypertension and stroke.
* **Smoking:** Significant association exists between smoking habits and stroke risk.
* **High Glucose:** People with glucose $\ge$ 126 mg/dL show statistically higher stroke rates.

**Feature Engineering**
* **Age Group:** Segmented into Young, Adults, Middle-aged, Senior (Seniors = highest risk).
* **High Glucose Flag:** Created binary indicator for clinical diabetes threshold ($\ge$ 126 mg/dL).
* **Medical Risk Score:** Composite score (0–4) summing Hypertension, Heart Disease, Glucose, and Obesity.
* **Interaction:** `Age_Glucose_Interaction` created to capture high glucose risk in older age.

**Final Output**
* **Export:** Saved processed data to `final_cleaned_day4.csv`.
* **Note:** Time-series analysis skipped (no date column available).

---

## 📁 Repository Structure

```text
eda-project/
│
├── data/
│   ├── raw/                 # Original dataset
│   ├── interim/             # Cleaned dataset (Day 2)
│   └── processed/           # Final dataset (Day 4)
│
├── notebooks/
│   ├── 01_data_overview.ipynb
│   ├── 02_cleaning_preprocessing.ipynb
│   ├── 03_univariate_bivariate_eda.ipynb
│   └── 04_stats_time_features_final_insights.ipynb
│
├── reports/
│   └── figures/             # Exported plots
│
└── README.md