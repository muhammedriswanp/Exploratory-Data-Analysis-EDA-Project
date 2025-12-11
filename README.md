# 🏥 Stroke Prediction EDA Project

### 1. Project Overview
**Objective:** Perform a comprehensive Exploratory Data Analysis (EDA) on the Stroke Prediction dataset to identify key risk factors associated with stroke.
**Context:** According to the WHO, stroke is a leading cause of death globally (approx. 11% of total deaths). This project analyzes patient demographics, health conditions (hypertension, heart disease), and lifestyle choices to uncover patterns that can aid in early detection.

### 2. Dataset Information
The dataset contains **5,110 observations** with **12 features**.
* **Source:** [Kaggle - Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
* **Target Variable:** `stroke` (0 = No Stroke, 1 = Stroke)
* **Key Features:** Age, BMI, Glucose Level, Smoking Status, Hypertension, Heart Disease.

---

### 3. Repository Structure
```text
eda-project/
│
├── data/
│   ├── raw/                  # Original dataset (healthcare-dataset-stroke-data.csv)
│   ├── interim/              # Cleaned versions (created during Day 2)
│   └── processed/            # Final datasets for modeling
│
├── notebooks/
│   ├── 01_data_overview.ipynb              # Day 1: Profiling & Issues Log
│   ├── 02_cleaning_preprocessing.ipynb     # Day 2: Cleaning & Imputation
│   ├── 03_univariate_bivariate_eda.ipynb   # Day 3: Visualization
│   └── 04_stats_time_features_final.ipynb  # Day 4: Stats & Final Insights
│
├── reports/
│   └── figures/              # Exported PNG plots
│
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation