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

The aim of this machine learning project is to develop a predictive model that identifies customers at risk of churning based on behavioral and usage data. The project will analyze features including:

**Customer duration (tenure)**
**Total amount spent per customer**
**Activeness level (e.g., frequency or consistency of use)**
**Ratio of on-net to off-net calls**
* To develop a predictive model capable of identifying customers at high risk of churn.
* To analyze key behavioral and usage factors such as the Customer duration (tenure), Activeness level (usage frequency or consistency), Total amount spent per customer and the Customer location.
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
<img width="1489" height="1490" alt="GrpPRJ2" src="https://github.com/user-attachments/assets/539c7936-1842-48f2-ad7c-89ba9f3d66fe" />



# Key Insights

One of the most significant findings was the impact of tenure on churn rates. Customers with a shorter duration on the network were found to be more likely to churn compared to long-term customers. This underscores the importance of early engagement strategies to build loyalty and reduce the likelihood of churn within the first year of a customer’s lifecycle.

Another critical observation centered on revenue and activity patterns. Customers who generated low revenue or displayed low activity levels were more prone to leaving the network. This indicates that customer engagement and revenue generation are strongly linked to retention, suggesting that boosting customer interaction and usage could help reduce churn.

During the modeling process, an imbalance in the dataset presented a notable challenge. The dataset contained a disproportionately high number of “no churn” cases compared to “churn” cases, leading the initial predictive models to favor non-churn predictions. This imbalance affected the models' ability to accurately identify customers at risk of churning.

In terms of model performance, the results varied before and after balancing the dataset. Before balancing, Logistic Regression and Random Forest models each achieved an accuracy of 87%, while XGBoost slightly outperformed them with 88% accuracy. However, the models struggled to identify churned customers effectively due to the imbalance issue. After balancing, the Random Forest model demonstrated the best overall performance, achieving 86% accuracy with a more balanced trade-off between precision and recall, making it more reliable for churn detection. Logistic Regression performed slightly lower at 84% accuracy but showed improved recall for churned customers, indicating better detection of at-risk users. Conversely, XGBoost’s performance dropped sharply to around 54% accuracy, suggesting that it had overfitted after the balancing process.

These insights highlight not only the behavioral patterns that influence churn but also the importance of handling data imbalance to build robust predictive models. By leveraging these findings, organizations can develop targeted retention strategies and deploy more effective models for proactive customer engagement.

# Recommendations

From a retention perspective, the company should prioritize strategies that build loyalty among new customers during their first year. Personalized onboarding offers, tailored communication, and early engagement programs can help establish strong relationships and reduce the likelihood of early churn. Additionally, identifying and monitoring low-activity customers is critical. Proactive engagement through targeted promotions, loyalty incentives, or personalized offers can encourage these users to increase their activity and remain connected to the network.

In terms of revenue optimization, the analysis highlights the importance of increasing customer engagement to reduce churn risk. Encouraging frequent recharges, upselling data packages, and promoting premium services can boost both customer satisfaction and revenue. These strategies not only enhance customer value but also foster long-term relationships with the brand.

For model deployment, the Random Forest model has been identified as the most balanced and reliable option. Implementing this model in production will allow the company to make accurate and actionable predictions on at-risk customers. To maintain its effectiveness, the model should be retrained periodically with updated data to adapt to evolving customer behaviors and market trends.

Finally, there are opportunities for further improvements to enhance prediction accuracy and insight generation. Experimenting with advanced techniques such as SMOTE or ensemble sampling can help address data imbalance more effectively, improving the model’s ability to detect churn cases. Additionally, integrating behavioral and demographic data can provide a more comprehensive view of customer profiles, enabling the creation of more targeted retention and revenue strategies.

