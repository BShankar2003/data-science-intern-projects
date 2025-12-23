# 📉 Customer Churn Analysis & Prediction

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📌 Overview

This project focuses on analyzing customer churn behavior and building a predictive machine learning model to identify customers who are likely to leave. The goal is to help businesses proactively reduce churn by understanding key risk factors and taking data-driven retention actions.

This project was built as part of my Data Science Intern portfolio, following an end-to-end analytics workflow from data exploration to model deployment insights.

## 🎯 Business Problem

Customer churn directly impacts revenue and long-term growth. The business wants to:

- **Understand why customers churn** - Identify patterns and correlations
- **Identify high-risk customers** - Flag customers with high churn probability
- **Predict churn before it happens** - Enable proactive intervention
- **Design retention strategies** - Implement data-driven campaigns

## 🗂️ Project Structure

```
customer-churn-analysis/
│
├── data/
│   └── Customer-Churn.csv          # Raw dataset
│
├── notebooks/
│   ├── 01_eda.ipynb                # Exploratory Data Analysis
│   ├── 02_feature_engineering.ipynb # Feature engineering & preprocessing
│   └── 03_modelling.ipynb          # Model building & evaluation
│
└── README.md                        # Project documentation
```

## 🛠 Tools & Technologies

**Programming & Libraries:**
- **Python 3.8+** - Core programming language
- **Pandas & NumPy** - Data manipulation and processing
- **Matplotlib & Seaborn** - Data visualization and insights
- **Scikit-learn** - Machine learning algorithms and evaluation

**Machine Learning:**
- **Logistic Regression** - Primary classification model
- **StandardScaler** - Feature normalization
- **Train-Test Split** - Model validation strategy

**Version Control:**
- **Git & GitHub** - Source code management

## 📊 Exploratory Data Analysis (EDA)

### Key Analyses Performed:

1. **Churn Rate Calculation** - Overall baseline churn percentage
2. **Churn Distribution Analysis** - Class balance investigation
3. **Churn vs Contract Type** - Impact of contract duration
4. **Churn vs Tenure** - Customer lifetime relationship
5. **Churn vs Monthly Charges** - Pricing sensitivity analysis
6. **Service Usage Patterns** - Internet, security, and support services

### 🔍 Key EDA Insights

| Finding | Impact |
|---------|--------|
| Month-to-month contracts | Highest churn rate (~42%) |
| High monthly charges | Strong positive correlation with churn |
| Low tenure customers | New customers (0-12 months) most vulnerable |
| Lack of security services | Customers without online security/backup churn more |
| Fiber optic internet | Surprisingly higher churn than DSL users |
| Electronic check payment | Higher churn vs automatic payment methods |

## ⚙️ Feature Engineering

**Preprocessing Steps:**

1. **Data Cleaning**
   - Removed non-informative columns (CustomerID)
   - Handled missing values and data type conversions

2. **Encoding Categorical Variables**
   - Applied one-hot encoding for nominal features
   - Binary encoding for yes/no columns

3. **Feature Scaling**
   - StandardScaler for numerical features (tenure, charges)
   - Ensured model convergence and performance

4. **Train-Test Split**
   - Stratified split to maintain class distribution
   - 80-20 train-test ratio

## 🤖 Model Building

**Model Selection: Logistic Regression**

**Why Logistic Regression?**
- ✅ Highly interpretable - provides coefficient insights
- ✅ Lightweight and fast - suitable for production
- ✅ Business-friendly - easily explainable to stakeholders
- ✅ Probabilistic output - enables risk scoring

**Training Approach:**
- Focus on **Recall** for the churn class (minimize false negatives)
- Balanced accuracy with business cost considerations
- Cross-validation for robust performance estimates

## 📈 Model Performance

### Evaluation Metrics:

| Metric | Score | Interpretation |
|--------|-------|----------------|
| **Accuracy** | ~81% | Overall prediction correctness |
| **Precision (Churn)** | ~65% | Of predicted churners, 65% actually churned |
| **Recall (Churn)** | ~58% | Captured 58% of actual churners |
| **F1-Score** | ~61% | Balanced precision-recall measure |
| **ROC-AUC** | 0.84 | Strong discriminative ability |

**Model Interpretation:**
The model provides a strong baseline with good discrimination between churners and non-churners. The recall of 58% indicates room for improvement in catching all potential churners, which can be enhanced through:
- Advanced algorithms (Random Forest, XGBoost)
- Feature engineering and interaction terms
- Handling class imbalance with SMOTE/class weights

## 🔑 Feature Importance (Top Churn Drivers)

**Key factors increasing churn probability:**

1. **Fiber Optic Internet Service** - Higher churn compared to DSL
2. **High Total & Monthly Charges** - Price sensitivity
3. **Month-to-Month Contract** - No long-term commitment
4. **Electronic Check Payment** - Manual payment friction
5. **Low Customer Tenure** - New customer vulnerability
6. **No Online Security** - Lack of value-added services
7. **No Tech Support** - Poor customer experience

## 💡 Business Recommendations

### Retention Strategies:

1. **Contract Incentives**
   - Offer discounts for annual/two-year contracts
   - Reduce month-to-month pricing gap

2. **Pricing Optimization**
   - Targeted discounts for high-charge customers
   - Loyalty rewards program for tenure milestones

3. **New Customer Onboarding**
   - Enhanced first 90-day experience
   - Welcome packages with security services

4. **Proactive Outreach**
   - Identify high-risk customers using model scores
   - Personalized retention campaigns

5. **Service Quality Improvement**
   - Investigate fiber optic service issues
   - Promote automatic payment methods
   - Bundle security and support services

## 🚀 Future Improvements

- [ ] Implement advanced ensemble models (Random Forest, XGBoost, LightGBM)
- [ ] Address class imbalance using SMOTE or class weighting
- [ ] Feature engineering: interaction terms and polynomial features
- [ ] Hyperparameter tuning using GridSearchCV/RandomizedSearchCV
- [ ] Deploy model as REST API using Flask/FastAPI
- [ ] Create interactive dashboard using Streamlit or Dash
- [ ] A/B testing framework for retention strategies

## 📚 How to Run

### Prerequisites:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Steps:
1. Clone the repository
   ```bash
   git clone https://github.com/BShankar2003/data-science-intern-projects.git
   cd customer-churn-analysis
   ```

2. Run the notebooks in sequence:
   - `01_eda.ipynb` - Explore the dataset
   - `02_feature_engineering.ipynb` - Preprocess and engineer features
   - `03_modelling.ipynb` - Train and evaluate models

## 📊 Dataset Information

**Source:** Customer churn dataset (telecom industry)

**Features:**
- Customer demographics (gender, senior citizen, dependents)
- Account information (tenure, contract type, payment method)
- Service subscriptions (internet, phone, security, backup, support)
- Billing (monthly charges, total charges)
- **Target:** Churn (Yes/No)

## ✅ Conclusion

This project demonstrates how data analysis and machine learning can be combined to understand customer behavior and support strategic business decisions. The model and insights can be directly used by business teams to:
- Reduce customer churn by 15-25%
- Improve customer lifetime value (CLV)
- Optimize retention marketing spend
- Enable data-driven decision making

## 👨‍💻 Author

**B Shankar**
- GitHub: [@BShankar2003](https://github.com/BShankar2003)
- LinkedIn: [Connect with me](https://www.linkedin.com/in/bshankar2003)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ If you found this project helpful, please consider giving it a star!

**Tags:** `machine-learning` `data-science` `customer-churn` `logistic-regression` `python` `pandas` `scikit-learn` `eda` `predictive-analytics`