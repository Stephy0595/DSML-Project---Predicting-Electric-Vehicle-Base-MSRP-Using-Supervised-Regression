# Predicting-Electric-Vehicle-Base-MSRP-Using-Supervised-Regression

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

### Phase 1. Data Preprocessing & Cleaning

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




