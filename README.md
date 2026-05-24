# 🔄 Customer Churn Prediction & Analysis

> Predicts customer churn using Random Forest | EDA, SQL Analysis & Power BI Dashboard

---

## 📌 Overview

In today's competitive business environment, retaining customers is crucial for long-term success. This project performs an **end-to-end churn analysis** for a telecom company — from raw data ingestion to machine learning predictions and interactive dashboards.

The project helps businesses:
- Understand **why customers are leaving**
- Identify customers **at risk of churning**
- Take **proactive steps** to improve customer retention

---

## 🎯 Project Goals

- ✅ Build a complete **ETL pipeline** using SQL Server
- ✅ Perform **Exploratory Data Analysis (EDA)**
- ✅ Create an interactive **Power BI Dashboard**
- ✅ Build a **Random Forest ML model** to predict future churners
- ✅ Visualize predicted churners in Power BI

---

## 📊 Key Metrics Tracked

| Metric | Description |
|--------|-------------|
| Total Customers | Overall customer count |
| Total Churn | Number of customers who left |
| Churn Rate | Percentage of churned customers |
| New Joiners | Newly acquired customers |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **SQL Server (SSMS)** | ETL, Data Cleaning, Views |
| **Python (Jupyter Notebook)** | ML Model — Random Forest |
| **Power BI** | Dashboard & Visualization |
| **pandas, scikit-learn** | Data Processing & ML Libraries |
| **Excel** | Intermediate Data Storage |

---

## 📁 Project Structure

```
customer-churn-prediction/
│
├── data/
│   ├── raw/
│   │   └── Customer_Data.csv          ← Original source data
│   └── processed/
│       ├── Prediction_Data.xlsx       ← Data prepared for ML model
│       ├── Customer_Status_Predicted.xlsx
│       ├── Final_Predictions.xlsx
│       └── Predictions.csv            ← Final churn predictions
│
├── notebooks/
│   └── Churn_Prediction.ipynb         ← Random Forest ML model
│
├── sql/
│   ├── Queries.sql                    ← Database & table creation
│   ├── Queries1.sql                   ← Data exploration
│   ├── Queries2.sql                   ← Null checks
│   ├── Queries3.sql                   ← Data cleaning & prod table
│   └── Queries4.sql                   ← Views for Power BI
│
├── reports/
│   ├── Churn_Prediction.html          ← Notebook HTML export
│   └── Churn_Prediction.pdf           ← Notebook PDF export
│
├── dashboard/
│   └── Churn_Analysis.pbix            ← Power BI Dashboard file
│
└── README.md
```

---

## 🔄 Project Workflow

### Step 1 — ETL in SQL Server
- Loaded raw CSV into SQL Server staging table (`stg_Churn`)
- Performed data exploration — checked distinct values & null counts
- Cleaned nulls and inserted into production table (`prod_Churn`)
- Created views for Power BI: `vw_ChurnData` and `vw_JoinData`

### Step 2 — Power BI Data Transformation
- Added calculated columns: `Churn Status`, `Monthly Charge Range`
- Created mapping tables for Age Groups and Tenure Groups
- Unpivoted services columns for better analysis

### Step 3 — Power BI Dashboard
- **Summary Page** — Demographics, Account Info, Geographic, Churn Distribution
- **Churn Reason Page** — Tooltip with detailed churn reasons
- **Churn Prediction Page** — Visualized predicted churners

### Step 4 — Machine Learning (Random Forest)
- Imported SQL views into Excel as `Prediction_Data.xlsx`
- Preprocessed data — Label Encoding for categorical features
- Trained **Random Forest Classifier** (100 estimators)
- Evaluated model with Confusion Matrix & Classification Report
- Predicted churn on new joiner data → saved as `Predictions.csv`

---

## 🤖 ML Model Details

| Parameter | Value |
|-----------|-------|
| Algorithm | Random Forest Classifier |
| Estimators | 100 trees |
| Test Split | 20% |
| Target Variable | Customer_Status (Churned / Stayed) |
| Libraries | scikit-learn, pandas, numpy, seaborn |

---

## 📈 Power BI Dashboard Highlights

**Summary Page**
- Total Customers, New Joiners, Total Churn, Churn Rate %
- Gender & Age Group breakdown
- Payment Method, Contract, Tenure analysis
- Top 5 States by Churn Rate
- Churn Category & Reasons

**Churn Prediction Page**
- Predicted churner count
- Demographic & Geographic breakdown
- Customer-level grid with revenue details

---

## 📌 Key Insights

- Customers on **month-to-month contracts** have the highest churn rate
- **Fiber Optic** internet users churn more than others
- Customers with **low tenure (< 6 months)** are most at risk
- Top churn reasons: **Competitor offers & Dissatisfaction**

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
