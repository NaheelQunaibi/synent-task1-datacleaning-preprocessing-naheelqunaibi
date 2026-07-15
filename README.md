# synent-task1-datacleaning-preprocessing-naheelqunaibi
# Task 1: Data Cleaning & Preprocessing

## Overview

This project performs comprehensive data cleaning and preprocessing on the **Titanic Dataset** to prepare it for analysis and machine learning. The raw data contains missing values, incorrect data types, and inconsistent formatting that must be addressed before any meaningful analysis can be performed.

The goal is to transform raw, messy data into a clean, structured, and analysis-ready dataset while documenting all transformations applied.

---

## Dataset Description

The Titanic dataset contains information about 891 passengers aboard the RMS Titanic, including:

| Feature | Description |
|---------|-------------|
| `PassengerId` | Unique passenger identifier |
| `Survived` | Survival status (0 = No, 1 = Yes) |
| `Pclass` | Passenger class (1st, 2nd, 3rd) |
| `Name` | Passenger name |
| `Sex` | Gender |
| `Age` | Age in years |
| `SibSp` | Number of siblings/spouses aboard |
| `Parch` | Number of parents/children aboard |
| `Ticket` | Ticket number |
| `Fare` | Passenger fare |
| `Cabin` | Cabin number |
| `Embarked` | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

---

## Data Cleaning Steps Applied

### 1. Handle Missing Values

| Column | Missing Count | Action Taken |
|--------|---------------|--------------|
| `Age` | 177 | Filled with median value (28) |
| `Embarked` | 2 | Filled with mode value ('S') |
| `Cabin` | 687 | Dropped entirely (too many missing values) |

### 2. Remove Duplicates

- **Duplicate rows found:** 0
- **Action:** No duplicates to remove; dataset remains at 891 rows

### 3. Convert Data Types

| Column | Original Type | Converted Type |
|--------|---------------|----------------|
| `Survived` | int64 | `bool` |
| `Pclass` | int64 | `category` |
| `Sex` | object | `category` |
| `Embarked` | object | `category` |
| `Age` | float64 | `int64` |
| `Fare` | float64 | `float64` (rounded to 2 decimals) |

### 4. Standardize Values
- `Sex` values converted to lowercase (`male`/`female`)
- `Fare` rounded to 2 decimal places

### 5. Rename Columns

| Original Name | New Name |
|---------------|----------|
| `PassengerId` | `Passenger_Id` |
| `Pclass` | `P_Class` |

---

---

## 🛠️ Tools & Libraries Used

| Tool | Purpose |
|------|---------|
| **Python** | Core programming language |
| **Pandas** | Data manipulation and analysis |
| **KaggleHub** | Dataset download from Kaggle |
| **Jupyter Notebook** | Interactive development environment |

---

## 📄 Files in This Repository

| File | Description |
|------|-------------|
| `Data_Cleaning_&_Preprocessing.ipynb` | Main Jupyter notebook with all cleaning steps |
| `Data_Cleaning_&_Preprocessing.html` | Exported HTML version of the notebook |
| `titanic.csv` | Original raw dataset |
| `titanic_cleaned.csv` | Final cleaned dataset (ready for analysis) |

