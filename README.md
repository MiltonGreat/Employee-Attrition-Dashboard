# Healthcare Attrition Analysis

## Overview

This project aims to analyze employee attrition within the US healthcare sector, a critical issue with a significant impact on healthcare delivery. By utilizing machine learning models and analytics, the project investigates the factors contributing to high attrition rates, the key predictors of employee departure, and potential solutions for reducing turnover. The analysis uses synthetic data based on the IBM Watson Healthcare dataset, modified to reflect healthcare-specific roles and departments.

### Objective

The goal of this project is to explore employee attrition in the healthcare industry and provide actionable insights into:

- Factors contributing to employee attrition in healthcare.
- Key predictors of employee turnover.
- Imbalanced dataset challenges and solutions, including handling class imbalance.
- Employee sentiment analysis and key attributes influencing job satisfaction.
- Model interpretation and feature importance to guide healthcare management decisions.

### Datasets

#### Watson Healthcare Attrition Dataset

- Contains employee data across various departments in a healthcare setting.
- The target variable: Attrition (whether an employee left or not).
- Employee-related features such as age, job satisfaction, work-life balance, and education.
- Synthetic data, with modifications to roles and outcomes to enhance machine learning performance.

### Problem Statement

Employee attrition is a persistent challenge in the US healthcare system, with high turnover rates leading to increased recruitment and training costs and reduced care quality. This project aims to uncover patterns in employee departure, analyze contributing factors, and provide insights into how healthcare institutions can mitigate these challenges.

### Solution Approach

#### Data Cleaning:
- Missing Values: All missing values were handled appropriately, ensuring that the dataset was complete for analysis.
- Outliers: Outliers were analyzed and addressed to improve model accuracy.
- Class Imbalance: The dataset had a high class imbalance (Attrition = No vs. Attrition = Yes), addressed using the SMOTE technique for oversampling.
- Categorical Variables: Categorical variables were encoded using one-hot encoding.

#### Exploratory Data Analysis (EDA):

- Analyzed the distribution of employee attrition and demographic trends.
- Used correlation heatmaps to uncover relationships between features such as job satisfaction, age, and monthly income.
- Visualized class imbalance and analyzed its impact on model performance.

#### Feature Engineering:

- Engineered features like job satisfaction, environment satisfaction, and work-life balance to understand their influence on attrition.
- Identified highly correlated features, e.g., JobLevel and MonthlyIncome, to address multicollinearity.

#### Machine Learning Model:

- A RandomForestClassifier was trained to predict employee attrition, with data preprocessing, feature importance analysis, and SHAP values used for interpretation.
- The model was evaluated based on precision, recall, and F1-score, and achieved an accuracy of 91% with strong performance in predicting non-attrition employees.

#### Model Interpretation:

- SHAP values were used to explain the influence of each feature on model predictions.
- Visualized feature importance to identify the top factors contributing to attrition predictions.

### Key Findings

#### Class Imbalance:

- The dataset had a significant imbalance, with a ratio of 7.42:1 between non-attrition (No) and attrition (Yes) employees.

#### Employee Demographics:

- Employee age had a mild positive skew, with younger employees (under 30) exhibiting higher attrition.
- The MonthlyIncome variable showed high skewness, with a large portion of employees having low to average income.

#### Feature Importance:

- The most important features influencing employee attrition were JobLevel, MonthlyIncome, and JobSatisfaction.

### Future Work

- Explore deep learning models for improved predictions.
- Investigate the use of other performance metrics like ROC-AUC for imbalanced datasets.
- Implement strategies for addressing high attrition beyond predictive modeling (e.g., employee engagement programs).

### Sources

https://www.kaggle.com/datasets/jpmiller/employee-attrition-for-healthcare/data

