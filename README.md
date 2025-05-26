# Task-1-Data-Preprocessing# - Sales Data Cleaning and Preprocessing

This project focuses on cleaning and preprocessing a raw sales dataset using **Python (Pandas)**. It demonstrates essential data wrangling skills every Data Analyst needs, including handling missing values, standardizing text, fixing data types, and preparing the data for analysis.

---

# Dataset

- **Source:** Kaggle Sales Dataset
- **File Used:** `dmart.csv`

---

## 🎯 Objective

To clean and prepare the raw dataset for further analysis and reporting by performing the following tasks:

1. Handle missing values
2. Remove duplicate rows
3. Standardize categorical text fields (like gender, state, subscription)
4. Convert dates to consistent format
5. Rename column headers for consistency
6. Correct inappropriate data types

---

## 🧰 Tools Used

- Python
- Pandas
- Jupyter Notebook / VSCode

---

## ✅ Cleaning Steps Performed

### 1. **Missing Values**
- Identified using `.isnull().sum()`
- Handled using imputation or left as-is if meaningful (e.g., cancellation dates)

### 2. **Duplicates**
- Removed using `df.drop_duplicates()`

### 3. **Standardization**
- Standardized categorical text values using `.str.strip().str.lower().str.capitalize()`

### 4. **Date Conversion**
- Converted columns like `order_date`, `delivery_date`, `cancellation_date` to `datetime64` format

### 5. **Column Renaming**
- Cleaned all column names using:
  ```python
  df.columns = df.columns.str.lower().str.strip().str.replace(" ", "_").str.replace("/", "_")
