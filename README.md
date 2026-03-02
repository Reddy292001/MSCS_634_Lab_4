# Regression Analysis on Diabetes Dataset (scikit-learn)

## Student Info
- **Name:** Sakthidhar Koneru  
- **Course:** <Your Course Title>  
- **Lab Title:** Regression Analysis using Diabetes Dataset (sklearn)

---

## Overview
This lab performs regression analysis on the **Diabetes dataset** from `sklearn.datasets`.  
The goal is to predict a continuous target value (disease progression) using different regression models and compare their performance.

---

## Dataset
- **Source:** `sklearn.datasets.load_diabetes()`
- **Samples:** 442
- **Features:** 10 (already normalized in the sklearn dataset)
- **Target:** A quantitative measure of disease progression

---

## Tasks Completed

### Step 1: Data Preparation
- Loaded the dataset and converted it into a Pandas DataFrame
- Checked for missing values (none found)
- Explored feature and target distributions using summary statistics and plots

### Step 2: Simple Linear Regression
- Trained a Linear Regression model using **one feature** (`bmi`)
- Split data into train/test sets
- Evaluated using **MAE, MSE, RMSE, and R²**
- Visualized regression line and predictions

### Step 3: Multiple Linear Regression
- Trained a Linear Regression model using **all 10 features**
- Evaluated using MAE, MSE, RMSE, and R²
- Visualized predicted vs actual values

### Step 4: Polynomial Regression
- Extended the single-feature model (`bmi`) using polynomial features
- Tested multiple polynomial degrees
- Discussed underfitting vs overfitting based on degree changes

### Step 5: Ridge and Lasso Regression
- Implemented:
  - **Ridge Regression** (L2 regularization)
  - **Lasso Regression** (L1 regularization)
- Tested different `alpha` values
- Compared results using the same metrics
- Highlighted that Lasso can reduce some coefficients to **zero** (feature selection)

### Step 6: Model Comparison and Analysis
- Summarized all model performances in a comparison table
- Key observations:
  - Single-feature linear model performed worst
  - Multiple regression improved performance significantly
  - Ridge gave a small improvement over multiple linear regression
  - Lasso gave the best overall performance in this experiment

---

## Results Summary (Test Set)
Based on the final comparison table:

| Model | MAE | MSE | RMSE | R² |
|------|-----:|-----:|-----:|----:|
| Simple Linear (bmi) | 52.26 | 4061.83 | 63.73 | 0.233 |
| Multiple Linear | 42.79 | 2900.19 | 53.85 | 0.453 |
| Polynomial (bmi) degree=1 | 52.26 | 4061.83 | 63.73 | 0.233 |
| Ridge alpha=100 | 43.25 | 2858.22 | 53.46 | 0.461 |
| Lasso alpha=1.0 | 42.80 | 2824.57 | 53.15 | 0.467 |

**Best model (highest R² / lowest RMSE):** **Lasso Regression (alpha=1.0)**

---

## Files Included
- `Lab_Regression_Diabetes.ipynb` (your notebook file)
- `README.md` (this file)

---

## How to Run
1. Open the notebook:
   - Jupyter Notebook / JupyterLab / VS Code
2. Run cells from top to bottom.

---

## Requirements
Install the required libraries if needed:

```bash
pip install numpy pandas matplotlib scikit-learn
