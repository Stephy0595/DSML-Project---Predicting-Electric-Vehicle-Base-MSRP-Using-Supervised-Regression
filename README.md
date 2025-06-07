# Predicting Electric Vehicle Base MSRP Using Supervised Regression

## Problem Statement
The objective of this project is to develop a **predictive regression model** that estimates the **Base MSRP (Manufacturer’s Suggested Retail Price)** of electric vehicles (EVs) based on their specifications and characteristics.

Understanding how features such as **range**, **battery capacity**, and **model year** affect EV pricing is crucial for stakeholders including:

- **EV Manufacturers**: Optimize pricing strategies  
- **Policymakers**: Evaluate the impact of EV incentive programs  
- **Consumers & Analysts**: Understand market value and pricing trends

 ##  Dataset Overview

- **Source**: [Electric Vehicle Population Data – data.gov](https://catalog.data.gov/dataset/electric-vehicle-population-data)
- **Type**: Public government dataset  
- **Format**: CSV



##  Project Type

- **Learning Type**: Supervised Learning  
- **Modeling Task**: Regression  
- **Target Variable**: `Base MSRP`  



##  Objectives

## Phase 1. Data Preprocessing & Cleaning

A clean and structured dataset is essential for effective modeling. The following steps were applied:

- **Data Overview**: 223,995 rows × 17 columns.
- **Data Types**: Identified numerical and categorical features using `df.info()`.
- **Basic Statistics**: Explored data distributions using `df.describe()`.
- **Unique Values**: Checked variability with `df.nunique()`.
- **Missing Values**:
  - Numerical: Filled with column-wise **mean**.
  - Categorical: Filled with **mode**.
  - ✅ All missing values handled.
- **Duplicates**: No duplicate records found (`df.duplicated().sum() = 0`).

 Dataset is now clean and ready for modeling.


## Phase 2.  Model Evaluation

To evaluate model performance in predicting the Base MSRP of electric vehicles, six supervised regression models were assessed using:

- **R² Score** – Variance explained by the model.
- **MSE (Mean Squared Error)** – Penalizes large errors.
- **MAE (Mean Absolute Error)** – Average magnitude of errors.
- **RMSE (Root Mean Squared Error)** – Square root of MSE, in MSRP units.

 ###  Results Summary

| Model                       | R² Score | MSE          | MAE       | RMSE     |
|----------------------------|----------|--------------|-----------|----------|
| Linear Regression          | 0.8051   | 1,212,303.66 | 654.92    | 1,100.14 |
| Decision Tree Regressor    | 0.9026   | 725,039.79   | 479.11    | 851.49   |
| Random Forest Regressor    | 0.9244   | 577,997.18   | 448.30    | 760.33   |
| Gradient Boosting Regressor| 0.9201   | 607,245.41   | 461.75    | 779.31   |
| Support Vector Regressor   | 0.5514   | 2,446,690.90 | 928.94    | 1,563.17 |
| MLP Regressor              | 0.8917   | 806,504.39   | 506.52    | 897.50   |

 ###  Key Insights

- **Random Forest Regressor** delivered the best results, with the highest R² and lowest errors.
- **Gradient Boosting** closely followed, also showing strong generalization.
- **MLP Regressor** (neural network) performed well, though slightly less than ensemble models.
- **Support Vector Regressor** had the weakest performance, suggesting room for tuning.
- **Linear Regression** couldn’t capture complex relationships effectively.

 ###  Visual Evaluation

- Actual vs Predicted Plots  
- Residual Plots  
- Feature Importance Graphs (for tree-based models)  

