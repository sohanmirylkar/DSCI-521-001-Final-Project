# DSCI-521-001-Final-Project

---

# 💳 Credit Card Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)
![License](https://img.shields.io/badge/License-MIT-green)

Predicting customer churn is one of the most important tasks for financial institutions. When customers stop using their credit cards, banks lose long-term revenue and valuable customer relationships. Detecting churn early allows companies to take proactive retention actions.

This project uses **data analysis, statistical testing, and machine learning models** to predict whether a credit card customer is likely to churn. The analysis focuses on identifying behavioral patterns that signal disengagement before customers leave.

The final result is a predictive system capable of helping financial institutions **identify at-risk customers and implement targeted retention strategies.**

---

# 📌 Project Highlights

✔ Exploratory Data Analysis of customer behavior
✔ Statistical testing to validate churn indicators
✔ Feature importance analysis using mutual information
✔ Machine learning models for churn prediction
✔ Business insights for customer retention strategies

---

# 🎯 Problem Statement

Customer churn rarely happens suddenly. In many cases, customers show early behavioral signals such as:

* Reduced transaction activity
* Lower spending patterns
* Higher inactivity periods
* Increased contact with customer support

The goal of this project is to:

1. Analyze behavioral patterns of credit card customers
2. Identify key drivers of customer churn
3. Build machine learning models to predict churn
4. Provide actionable insights for business decision-making

---

# 📊 Dataset

The dataset used in this project is the **Credit Card Customers dataset**, commonly used for churn prediction analysis.

### Dataset Overview

| Metric             | Value  |
| ------------------ | ------ |
| Total Customers    | 10,127 |
| Existing Customers | ~83.9% |
| Attrited Customers | ~16.1% |
| Total Features     | 21     |

### Feature Categories

**Customer Demographics**

* Customer Age
* Gender
* Number of Dependents
* Education Level
* Marital Status

**Account Information**

* Months on Book
* Credit Limit
* Total Revolving Balance
* Available Credit

**Behavioral Metrics**

* Total Transaction Amount
* Total Transaction Count
* Transaction Activity Change
* Credit Utilization Ratio
* Months Inactive
* Customer Contact Count

The **target variable**:

```
Attrition_Flag
```

Converted to binary:

```
0 → Existing Customer
1 → Attrited Customer
```

---

# 🔬 Project Workflow

## 1️⃣ Data Preprocessing

Steps performed:

* Data loading using Pandas
* Removed unnecessary columns
* Converted churn label to binary format
* Checked missing values
* Prepared dataset for modeling

---

## 2️⃣ Exploratory Data Analysis

EDA was conducted to understand behavioral differences between churned and active customers.

Key visualizations included:

* Distribution plots
* Boxplots for churn comparison
* Correlation heatmaps
* Behavioral feature analysis

### Key Observations

Attrited customers typically show:

* Lower transaction counts
* Lower spending amounts
* Higher inactivity periods
* Lower credit utilization
* Increased customer service interactions

This suggests that **customer behavior is a strong signal of churn risk.**

---

# 📈 Statistical Analysis

To confirm whether the observed differences were statistically significant, **independent t-tests** were performed.

Features strongly associated with churn include:

* Total Transaction Count
* Total Transaction Amount
* Transaction Activity Change
* Revolving Balance
* Credit Utilization Ratio
* Customer Contact Frequency

This confirms that **behavioral metrics are stronger churn indicators than demographic variables.**

---

# 🔍 Feature Importance

Mutual Information analysis identified the most predictive variables:

Top predictors of churn:

1. Total Transaction Amount
2. Total Transaction Count
3. Transaction Activity Change
4. Revolving Balance
5. Credit Utilization Ratio

This reinforces the insight that **how customers use their credit cards matters more than who they are.**

---

# 🤖 Machine Learning Models

Two machine learning models were implemented and compared.

## Logistic Regression

Used as a baseline model due to its interpretability.

Advantages:

* Simple
* Fast
* Easy to explain

---

## Random Forest

Used as the primary predictive model.

Advantages:

* Handles nonlinear relationships
* Captures feature interactions
* High predictive performance

---

# 📊 Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression | 84.9%    | 51.9%     | 80.6%  | 63.1%    |
| Random Forest       | 94.8%    | 92.0%     | 74.2%  | 82.1%    |

### Interpretation

* Logistic Regression achieved **higher recall**, detecting more churners.
* Random Forest achieved **higher precision and overall accuracy**.

The **Random Forest model performed best overall** and was selected as the final model.

---

# 📊 Behavioral Insights

Important behavioral signals that indicate churn risk:

* Decline in transaction activity
* Reduced spending patterns
* Higher inactivity months
* Increased customer support interactions
* Lower credit utilization

An interesting pattern discovered was a **bimodal distribution in transaction activity among active customers**, indicating the presence of a potential early churn-risk segment.

---

# 💼 Business Applications

This predictive model can support several real-world applications:

* Early churn detection systems
* Targeted customer retention campaigns
* Customer segmentation strategies
* Portfolio risk monitoring
* Customer lifetime value optimization

Financial institutions can integrate such models into CRM systems to proactively retain valuable customers.

---

# ⚠️ Limitations

Despite strong performance, several limitations exist:

* Dataset represents a **single snapshot rather than time-series behavior**
* Model hyperparameters were not extensively tuned
* Dataset size is moderate compared to real banking data
* Random Forest interpretability can be limited

---

# 🚀 Future Improvements

Potential improvements include:

* Time-series churn prediction models
* Hyperparameter optimization
* Advanced models such as XGBoost or LightGBM
* Explainable AI using SHAP
* Real-time churn prediction API deployment

---

# 🛠 Technologies Used

Programming Language:

* Python

Libraries:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* scipy

Tools:

* Jupyter Notebook
* GitHub

---

# 📂 Project Structure

```
Credit-Card-Churn-Prediction
│
├── data
│   └── credit_card_customers.csv
│
├── notebooks
│   └── churn_analysis.ipynb
│
├── presentation
│   └── churn_prediction_presentation.pptx
│
├── images
│   └── visualizations
│
└── README.md
```

---

# 📸 Sample Visualizations

* Transaction count vs churn
* Transaction amount distribution
* Feature correlation heatmap
* Feature importance chart

---

# 👨‍💻 Author's

* Aadesh Kalbhor (ak4567@drexel.edu)
* Ahmed Syed (as6387@drexel.edu)
* Sohan Miryalkar (sm5243@drexel.edu)

