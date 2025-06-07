# Predicting Electric Vehicle Base MSRP Using Supervised Regression

## *Problem Statement*
The objective of this project is to develop a **predictive regression model** that estimates the **Base MSRP (Manufacturer’s Suggested Retail Price)** of electric vehicles (EVs) based on their specifications and characteristics.

Understanding how features such as **range**, **battery capacity**, and **model year** affect EV pricing is crucial for stakeholders including:

- **EV Manufacturers**: Optimize pricing strategies  
- **Policymakers**: Evaluate the impact of EV incentive programs  
- **Consumers & Analysts**: Understand market value and pricing trends

##  *Dataset Overview*

- **Source**: [Electric Vehicle Population Data – data.gov](https://catalog.data.gov/dataset/electric-vehicle-population-data)
- **Type**: Public government dataset  
- **Format**: CSV



##  *Project Type*

- **Learning Type**: Supervised Learning  
- **Modeling Task**: Regression  
- **Target Variable**: `Base MSRP`

 # *Phase 1. Data Preprocessing & Cleaning*

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

# *Phase 2.  Model Evaluation*

To evaluate model performance in predicting the Base MSRP of electric vehicles, six supervised regression models were assessed using:

- **R² Score** – Variance explained by the model.
- **MSE (Mean Squared Error)** – Penalizes large errors.
- **MAE (Mean Absolute Error)** – Average magnitude of errors.
- **RMSE (Root Mean Squared Error)** – Square root of MSE, in MSRP units.

## *Model Performance Summary*

| Best Model             | R² Score | MSE    | MAE    | RMSE   |
| ----------------- | -------- | ------ | ------ | ------ |
| **Random Forest** | 0.9900   | 0.0099 | 0.0025 | 0.0996 |

##  *Key Insights*

- **Random Forest Regressor** delivered the best results, with the highest R² and lowest errors.
- **Gradient Boosting** closely followed, also showing strong generalization.
- **MLP Regressor** (neural network) performed well, though slightly less than ensemble models.
- **Support Vector Regressor** had the weakest performance, suggesting room for tuning.
- **Linear Regression** couldn’t capture complex relationships effectively.

##  *Visual Evaluation*
 
- **Actual vs Predicted Plots** to visually assess prediction accuracy.

- **Residual Plots** to check the distribution and randomness of errors.

- **Feature Importance Graphs** (for tree-based models) to identify the most influential features driving the predictions.

## *Conclusion*
This project demonstrates how ensemble-based regression models, especially Random Forest, can effectively predict EV prices using structured data. The approach supports informed decision-making for stakeholders across the EV ecosystem.

