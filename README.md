# Healthcare Attrition Analysis

## Overview

This project aims to analyze employee attrition in the US healthcare sector, a critical issue with a significant impact on healthcare delivery. By utilizing machine learning models and analytics, the project investigates the factors contributing to high attrition rates, the key predictors of employee departure, and potential solutions for reducing turnover. The analysis uses synthetic data based on the IBM Watson Healthcare dataset, modified to reflect healthcare-specific roles and departments.

### Objective

The goal of this project is to explore employee attrition in the healthcare industry:

- Factors contributing to employee attrition in healthcare.
- Key predictors of employee turnover.
- Employee sentiment analysis and key attributes influencing job satisfaction.

### Problem Statement

Employee attrition is a persistent challenge in the US healthcare system, with high turnover rates leading to increased recruitment and training costs and reduced care quality. This project aims to uncover patterns in employee departure, analyze contributing factors, and provide insights into how healthcare institutions can mitigate these challenges.

### Datasets

#### Watson Healthcare Attrition Dataset

- Contains employee data across various departments in a healthcare setting.
- The target variable: Attrition (whether an employee left or not).
- Employee-related features such as age, job satisfaction, work-life balance, and education.
- Synthetic data, with modifications to roles and outcomes to enhance machine learning performance.

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

#### Over Time and Job Satisfaction
Investigate if employees who work overtime have lower job satisfaction, as that could lead to higher attrition. This can guide policy changes around workload distribution and employee well-being.

#### Tenure and Attrition
Since longer tenure is correlated with lower attrition, explore if long-term employees are being overlooked in terms of career development opportunities. They might also need more engagement or new challenges to stay motivated.

#### Stock Option Levels and Attrition
Further analysis could be done on why employees with higher stock option levels leave more frequently. Perhaps the stock options are not seen as a sufficient long-term incentive.

#### Age and Attrition
Explore whether younger employees (likely early in their careers) have higher attrition rates and whether that’s due to personal growth, better career opportunities, or dissatisfaction.

### Future Work

- Explore deep learning models for improved predictions.
- Investigate the use of other performance metrics like ROC-AUC for imbalanced datasets.
- Implement strategies for addressing high attrition beyond predictive modeling (e.g., employee engagement programs).

### Sources

Dataset: [Employee Attrition for Healthcare Dataset on Kaggle](https://www.kaggle.com/datasets/jpmiller/employee-attrition-for-healthcare/data)
