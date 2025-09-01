# Telecommunication-Customer-Churn-Prediction
## Table of Content
- [Overview](#Overview)
- [Data_Source](#Data_Source)
- [Tools_and_Skills](#Tools_and_Skills)
- [Skills_Demonstrated](#Skills_Demonstrated)
- [Objectives](#Objectives)
- [Data_Analysis_and_visualization](#Data_Analysis_and_visualization)
- [Key_Insights](#Key_Insights)
- [Recommendations](#Recommendations)



# Overview
Analyzing network services usage by customers of a Telecommunication network. Customer churn poses a major challenge in the telecommunications industry, often resulting in significant revenue losses. This project aimed to analyze customer behavioral data and develop predictive models to identify customers at risk of churning. The analysis focused on understanding key factors influencing churn and creating actionable insights for customer retention strategies.

# Data_Source

Data was sourced from African telecommunications company Espresso in Senegal.

# Tools_and_Skills

The project utilized Python on Google Colab for data preprocessing, exploratory data analysis (EDA), and model building.

Key libraries used were
* pandas, numpy – for cleaning, transforming, and managing data.
* matplotlib, seaborn – for creating visualizations to identify trends and patterns.
* scikit-learn, imblearn – for machine learning modeling and handling imbalanced datasets.
* xgboost – for building an efficient gradient boosting model.
* joblib – for saving and deploying the trained models.

# Skills_Demonstrated

Data Engineering: Cleaning and transforming raw datasets for modeling.
EDA: Identifying patterns and feature relationships using visualizations.
Feature Engineering: Encoding categorical variables and scaling numeric values.
Model Development: Implemented and compared Logistic Regression, Random Forest, and XGBoost models.
Model Optimization: Improved results using Random Under Sampling to handle class imbalance.
Model Deployment: Saved the final XGBoost model for future predictions


# Objectives

The key objectives of the project were:
* To develop a predictive model capable of identifying customers at high risk of churn.
* To analyze key behavioral and usage factors such as the Customer duration (tenure), Activeness level (usage frequency or consistency), Total amount spent per customer and the Customer location.

# Objectives

The aim of this machine learning project is to develop a predictive model that identifies customers at risk of churning based on behavioral and usage data. The project will analyze features including:

**Customer duration (tenure)**
**Total amount spent per customer**
**Activeness level (e.g., frequency or consistency of use)**
**Ratio of on-net to off-net calls**
By applying and comparing various machine learning algorithms, the project seeks to determine the most effective approach for predicting churn. The outcomes will help telecom companies implement proactive, data-driven customer retention strategies to reduce churn rates and enhance customer lifetime value.


# Data_Analysis_and_visualization
**Data Preparation**

Loaded raw data using Pandas.
Cleaned the dataset by removing irrelevant features and standardizing column names.
<img width="1366" height="471" alt="Screenshot (750)" src="https://github.com/user-attachments/assets/1a2cbf3a-9817-4764-a0d1-9b561b80b9f8" />

Handled missing values and outliers to improve data quality.
Dropped irrelevant columns (user_id, ZONE1, ZONE2, MRG).
Handled missing values using median and mode imputation.



**Exploratory Data Analysis (EDA)**

Categorized columns for better interpretation.
Used correlation heatmaps to identify relationships and null values.
Generated bar charts and visual summaries for key customer segments.
<img width="1187" height="590" alt="GrpPRJ" src="https://github.com/user-attachments/assets/eedde1e3-7d17-4ffe-93e4-70e2c8a7a12b" />


<img width="1194" height="590" alt="GrpPRJ1" src="https://github.com/user-attachments/assets/d4038d2f-1e41-4c33-bb68-f78ece51faa4" />

**Data Preprocessing**

Encoded categorical variables and scaled numeric features.
<img width="1366" height="468" alt="Screenshot (756)" src="https://github.com/user-attachments/assets/f61bea3b-f841-4e7c-8b2c-fe3067bfad9d" />

Defined feature and target variables for model training.






Visual Analysis:

Heatmaps for missing value detection.
<img width="1366" height="451" alt="Screenshot (754)" src="https://github.com/user-attachments/assets/8e86e149-d060-4ac7-ae6e-c2589ea485b7" />


Distribution plots for tenure, recharge amounts, and city distribution.
Histograms for revenue and usage patterns.



