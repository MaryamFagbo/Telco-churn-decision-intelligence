# Telco-churn-decision-intelligence
# Telco Customer Churn Prediction & Retention Decision Model

**Decision Intelligence Project**  
Personal project built on the public Telco Customer Churn dataset (Kaggle).

**Colab Notebook:** [Open in Google Colab](https://colab.research.google.com/drive/1RqemJhTG4NOyRUk1o8FDOxYxBfBF187o?usp=sharing)

---

## Project Overview

This project goes beyond standard churn prediction.  
It combines data cleaning, SQL analysis, exploratory data analysis, machine learning, and **profit-based decision making** to create a practical retention decision tool.

The goal is not only to predict who will churn, but to decide **when it is profitable to intervene**.

---

## Problem Statement

Telecom companies lose significant revenue when customers leave.  
Blanket retention offers are expensive and often given to customers who were not going to churn.

We need a system that:
1. Identifies high-risk customers
2. Recommends action only when the expected profit is positive

---

## Objectives

- Clean real-world messy data (especially the classic `TotalCharges` issue)
- Answer business questions using SQL
- Perform clear exploratory analysis with visualizations
- Train and compare classification models (Logistic Regression vs Random Forest)
- Select the decision threshold based on expected profit (not just accuracy)
- Deliver a clean Excel summary report for stakeholders

---

## Key Results

- Overall churn rate: **~26.5%**
- Highest risk segments:
  - Month-to-month contracts
  - Fiber optic internet
  - Electronic check payment method
- Best model: **Logistic Regression** (ROC-AUC ≈ 0.84)
- Optimal decision threshold (by expected profit): **≈ 0.35**  
  (using $80 retention cost and $400 customer value assumptions)

---

## Visualizations

The following charts were created during the analysis:

1. **Overall Churn Distribution** (Pie Chart)  
   Shows that approximately 26.5% of customers churned.

2. **Churn Rate by Contract Type** (Bar Chart)  
   Month-to-month contracts have significantly higher churn than one-year or two-year contracts.

3. **Churn Rate by Internet Service** (Bar Chart)  
   Fiber optic customers show much higher churn compared to DSL and no-internet customers.

4. **Monthly Charges Distribution by Churn** (Box Plot)  
   Churned customers tend to have higher monthly charges on average.

5. **Tenure Distribution by Churn** (Histogram)  
   Customers with short tenure are at much higher risk of leaving.

6. **ROC Curve Comparison**  
   Logistic Regression and Random Forest performance comparison.

---

## Technologies Used

- Python
- Pandas & NumPy
- SQLite
- Matplotlib & Seaborn
- Scikit-learn (Logistic Regression + Random Forest)
- openpyxl (Excel report generation)
- Google Colab

---

## Project Structure
telco-churn-decision-intelligence/

├── README.md

├── Telco_Churn_Decision_Report.xlsx

├── notebooks/

│   └── telco_churn_analysis.ipynb

└── data/

└── README.md

---

## How to Run

1. Download the dataset from Kaggle:  
   [Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

2. Open the notebook in Google Colab using the link at the top of this README,  
   **or** download the notebook and run it locally / in Colab.

3. Upload the CSV file when prompted.

4. Run all cells in order.

5. The Excel decision report will be generated automatically.

---

## Business Assumptions

| Parameter                        | Value   |
|----------------------------------|---------|
| Retention Offer Cost             | $80     |
| Value of Retaining a Customer    | $400    |

These values are assumptions for demonstration purposes. In a real company they would come from the finance / customer success team.

---

## Main Learning Outcomes

- Real-world data cleaning (handling hidden blank values)
- Using SQL for business questions
- Proper model evaluation (Precision, Recall, ROC-AUC)
- Translating model probabilities into business decisions using expected profit
- Creating clean, stakeholder-ready reports

---

## Limitations

- The dataset is public/synthetic (not live company data)
- Customer Lifetime Value is assumed, not calculated from real historical data
- No real-time deployment or dashboard in this version

---

## Future Improvements

- Calculate real Customer Lifetime Value from historical data
- Test more advanced models (XGBoost, LightGBM)
- Build a simple Streamlit dashboard for business users
- Add cost-sensitive learning techniques

---

## Author
Maryam Fagbo
Personal project created for learning and portfolio purposes.
