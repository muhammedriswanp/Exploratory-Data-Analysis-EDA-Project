# Exploratory-Data-Analysis-EDA-Project
<br>

## Day 2: Data Cleaning & Preprocessing
**Date:** 2025-12-09
**Status:** ✅ Completed

**Key Changes Made:**
1. **Data Type Fixes:**
   - Converted `SignUpDate`, `PurchaseDate`, and `LastLogin` to datetime objects.
   - Converted `UserID` and `ProductID` to strings (categorical) to prevent accidental math operations.

2. **Outlier Treatment:**
   - **ReviewScore:** Identified as a 0-10 scale. Removed 3 rows with invalid negative scores.
   - **TotalAmount:** Detected 723 statistical outliers using IQR, but **retained them** as they represent valid high-value transactions.

3. **Data Quality Checks:**
   - **Missing Values:** Confirmed 0 missing values across the dataset.
   - **Duplicates:** Confirmed 0 duplicate rows.
   - **Categoricals:** Verified consistency in `Gender`, `Country`, and `ReferralSource`.

**Outcome:**
- **Final Dataset Shape:** (99,997 rows, 21 columns)
- **Saved File:** `data/interim/cleaned_day2.csv`