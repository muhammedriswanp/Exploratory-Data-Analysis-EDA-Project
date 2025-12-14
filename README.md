# Exploratory Data Analysis (EDA) Project
### Stroke Prediction Dataset

**Duration:** 5 Days  
**Mode:** Individual Project  
**Tools:** Python, Jupyter Notebook, pandas, numpy, matplotlib, seaborn, Git, GitHub

---

## Project Overview

This project performs a complete Exploratory Data Analysis (EDA) on a real-world healthcare dataset related to stroke occurrence.

* **Objective:** The objective is to understand how demographic, medical, and lifestyle factors such as age, glucose level, BMI, hypertension, heart disease, and smoking behavior are associated with stroke risk.
* **Workflow:** The project follows a structured, day-wise EDA workflow covering data profiling, cleaning, visualization, statistical testing, and feature engineering, with clear documentation and daily GitHub commits.

---

## Instructions to Run

**1. Clone the repository**
    ```bash
    git clone <your-github-repo-url>

## 2. Install dependencies

pip install -r requirements.txt
    
## 3. Run notebooks in sequence

* 01_data_overview.ipynb

* 02_cleaning_preprocessing.ipynb

* 03_univariate_bivariate_eda.ipynb

* 04_stats_time_features_final_insights.ipynb

## 4. Final processed dataset Located at: 
data/processed/final_cleaned_day4.csv

---

## Key Insights (Top 10)

* **Rarity:** Stroke cases are relatively rare in the dataset, requiring cautious interpretation of comparisons.
* **Data Quality:** Data quality issues such as missing BMI values and categorical inconsistencies were identified and resolved.
* **Age Factor:** Stroke risk increases sharply with age, with seniors being the most affected group.
* **Distributions:** Average glucose level and BMI show right-skewed distributions with a small high-risk subgroup.
* **Multifactorial Risk:** No single variable strongly predicts stroke; risk emerges from multiple combined factors.
* **Comparison:** Stroke patients are significantly older and have higher glucose levels than non-stroke individuals.
* **Clinical Benchmark:** Mean glucose level is significantly higher than the normal clinical benchmark of 100 mg/dL.
* **Comorbidities:** Individuals with stroke or heart disease have higher average BMI.
* **Associations:** Smoking status, hypertension, work type, and age group show statistically significant associations with stroke.
* **Risk Stratification:** Engineered features such as Medical Risk Score and Age–Glucose Interaction clearly identify high-risk individuals.

---

## Segment Findings

**Age Groups**
Stroke risk increases sharply across age groups, with seniors showing the highest occurrence.

**Smoking & Gender**
Former and current smokers exhibit higher stroke rates compared to never-smokers, especially among males.

**Medical Conditions**
Individuals with hypertension, heart disease, high glucose, or obesity show substantially higher stroke risk.

**Occupational Health**
BMI and glucose levels vary across work types, suggesting occupational and lifestyle influences on health risk.

---

## Data Quality Issues

**Missing Values**
Missing BMI values were handled using median imputation.

**Class Imbalance**
Stroke cases are relatively rare, which may affect the stability of some statistical comparisons.

**Inconsistencies**
Categorical inconsistencies (e.g., work type labels, smoking status formatting) required standardization.

**Rare Categories**
A single rare gender category was removed to avoid distortion in categorical analysis.

**Time-Series Limitation**
The dataset does not include a date/time column, so time-based EDA was not performed.

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
└── requirements.txt