# Homeownership-analysis

## Overview

This project presents an end-to-end data science analysis exploring the relationship between median household income, housing affordability, and homeownership rates across U.S. states from 2005–2024.

The goal of this analysis is to evaluate whether higher income leads to higher homeownership, and to determine which factors most strongly influence homeownership outcomes.

All work is contained in a single Jupyter Notebook and follows the full data science workflow: data cleaning, exploration, hypothesis testing, machine learning, evaluation, and interpretation.

## Research Question

Does an increase in median household income lead to higher homeownership rates across U.S. states?

Initial exploratory analysis suggested that this relationship may not be strictly positive. This project investigates that assumption using statistical analysis and machine learning models.

## Hypothesis

Original Hypothesis:
If the median household income of a state increases, then the homeownership rate in the state will also increase.

Revised Hypothesis (based on exploratory findings):
If median household income increases without a corresponding increase in housing affordability, homeownership rates may stagnate or decline.

## Dataset

- State-level annual data (2005–2024) including:

- Median household income

- Homeownership rate

- Population

- Housing Price Index (HPI)

- Derived affordability features (e.g., Income-to-HPI ratio)

All data is aggregated at the U.S. state level (including Washington, D.C.).

## Methodology
### 1. Data Cleaning & Preprocessing

- Removed formatting inconsistencies

- Converted data types

- Aggregated quarterly data to annual values

- Checked for missing values and duplicates

- Standardized and scaled features for modeling

### 2. Exploratory Data Analysis (EDA)

- Summary statistics

- Correlation analysis

- Trend analysis over time

- Visualizations to assess relationships and assumptions

### 3. Feature Engineering

- Log transformations for skewed variables

- Creation of affordability metrics

- Feature selection based on interpretability and performance

### 4. Models Used

- Linear Regression (baseline)

- Ridge Regression (L2 regularization)

- Lasso Regression (L1 regularization)

- Random Forest Regressor (non-linear ensemble model)

### 5. Model Evaluation

Models were evaluated using:

-- R²

-- RMSE

-- MAE

-- MAPE

-- 5-Fold Cross-Validation

#### Results Summary

| Model              | Test R² | RMSE | MAE |
|--------------------|---------|------|-----|
| Linear Regression  | ~0.28   | ~5.8 | ~4.1 |
| Ridge Regression   | ~0.28   | ~5.8 | ~4.1 |
| Lasso Regression   | ~0.28   | ~5.8 | ~4.1 |
| Random Forest      | ~0.86   | ~2.5 | ~1.9 |


**The Random Forest model significantly outperformed linear models, indicating the presence of strong non-linear relationships between affordability and homeownership.**

## Key Insights

- Median household income alone is a weak predictor of homeownership.

- Housing affordability plays a more critical role than income by itself.

- Linear models fail to capture complex relationships in the data.

- Ensemble models such as Random Forest better reflect real-world housing dynamics.

## Ethical Considerations

- Income data must be handled responsibly to protect privacy.

- Models like this should not be used directly for lending or housing decisions.

- Risk of reinforcing regional or socioeconomic inequality if misapplied.

- Non-linear models require transparency and careful interpretation.

## Technologies Used

- Python

- Pandas, NumPy

- Matplotlib, Seaborn

- Scikit-learn

- Jupyter Notebook / Google Colab

## How to Run

- Clone the repository

- Open the notebook in Jupyter or Google Colab

- Run all cells from top to bottom
