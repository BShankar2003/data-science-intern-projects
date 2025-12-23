📉 Customer Churn Analysis & Prediction
📌 Overview

This project focuses on analyzing customer churn behavior and building a predictive machine learning model to identify customers who are likely to leave. The goal is to help businesses proactively reduce churn by understanding key risk factors and taking data-driven retention actions.

This project was built as part of my Data Science Intern portfolio, following an end-to-end analytics workflow.

🎯 Business Problem

Customer churn directly impacts revenue and long-term growth.
The business wants to:

Understand why customers churn

Identify high-risk customers

Predict churn before it happens

Design retention strategies based on insights

🗂️ Project Structure
customer-churn-analysis/
│
├── data/
│   └── Customer-Churn.csv
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_feature_engineering.ipynb
│   └── 03_modelling.ipynb
│
└── README.md

🛠 Tools & Technologies

Python

Pandas, NumPy – Data processing

Matplotlib, Seaborn – Data visualization

Scikit-learn – Machine Learning

Logistic Regression – Classification model

Git & GitHub – Version control

📊 Exploratory Data Analysis (EDA)

Key analyses performed:

Churn rate calculation

Churn distribution analysis

Churn vs contract type

Churn vs tenure

Churn vs monthly charges

🔍 Key EDA Insights

Customers on month-to-month contracts churn the most

High monthly charges significantly increase churn risk

New customers (low tenure) are more likely to churn

Customers without security-related services churn more often

⚙️ Feature Engineering

Removed non-informative columns (Customer ID)

Converted categorical variables using one-hot encoding

Scaled numerical features using StandardScaler

Performed stratified train-test split to handle class imbalance

🤖 Model Building

Model Used: Logistic Regression

Reason: Interpretable, lightweight, and business-friendly

Focus Metric: Recall for churn class

📈 Model Performance

Accuracy: ~81%

Recall (Churn): ~58%

ROC-AUC Score: 0.84

This provides a strong baseline churn prediction model.

🔑 Feature Importance (Top Churn Drivers)

Key factors increasing churn probability:

Fiber optic internet service

High total and monthly charges

Month-to-month payment behavior

Electronic check payment method

Low customer tenure

💡 Business Recommendations

Based on analysis and model insights:

Encourage customers to switch to long-term contracts

Provide discounts or offers to high monthly charge customers

Improve onboarding for new customers

Target high-risk customers with personalized retention campaigns

Monitor churn-prone segments proactively

✅ Conclusion

This project demonstrates how data analysis and machine learning can be combined to understand customer behavior and support strategic business decisions. The model and insights can be directly used by business teams to reduce churn and improve customer lifetime valu
