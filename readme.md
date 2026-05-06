# 📊 E-Commerce Sales & Cohort Analysis Dashboard

An end-to-end retail analytics project focused on analyzing customer purchasing behavior, revenue trends, product performance, and cohort retention patterns using Python and Power BI.

---

## 🚀 Project Overview

This project analyzes a real-world UK-based e-commerce dataset containing over 500K retail transactions. The objective was to uncover actionable business insights related to:

- Revenue performance
- Customer retention
- Product demand
- Country-wise sales distribution
- Customer acquisition trends

The project combines data cleaning, exploratory data analysis, cohort analysis, and interactive dashboard development to simulate a real business intelligence workflow.

---

## 🛠️ Tech Stack

| Layer | Tools |
|---|---|
| Programming | Python, Pandas, Matplotlib, Seaborn |
| Visualization | Power BI Desktop |
| Environment | Jupyter Notebook, VS Code |

---

## 📂 Dataset Information

- **Dataset:** UK E-Commerce Dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
- **Transactions:** 500K+
- **Products:** 4000+
- **Countries:** 38

---

## 🔥 Key Features

- ✅ Data Cleaning & Preprocessing
- ✅ Feature Engineering (Year, Month, Quarter, Day, Revenue)
- ✅ Revenue & Sales Trend Analysis
- ✅ Customer Cohort Retention Analysis
- ✅ Product Performance Analytics
- ✅ Country-wise Revenue Analysis
- ✅ Interactive Power BI Dashboard (3 Pages)
- ✅ KPI Tracking & Business Insights

---

## 📈 Dashboard Pages

### Page 1 — Executive Overview
High-level overview of overall business performance.

| Visual | Description |
|---|---|
| KPI Cards | Total Revenue, Orders, Customers, AOV |
| Line Chart | Monthly Revenue Trend |
| Bar Chart | Top 10 Products by Revenue |
| Bar Chart | Revenue by Country |
| Column Chart | Revenue by Day of Week |

---

### Page 2 — Cohort Retention Analysis
Analyzes customer retention behavior across acquisition cohorts.

| Visual | Description |
|---|---|
| Matrix Heatmap | Cohort Retention % with conditional formatting |
| Column Chart | Cohort Size by Month |

**Key Insight:** Customer retention drops significantly after Month 1, highlighting opportunities for retention-focused marketing strategies.

---

### Page 3 — Product & Country Analysis
Deep dive into product demand and country-wise sales contribution.

| Visual | Description |
|---|---|
| Donut Chart | UK vs Rest of World Revenue Split |
| Treemap | Revenue by Country |
| Scatter Plot | Quantity vs Revenue by Product |
| Table | Product Revenue Breakdown |

---

## 📊 Business Insights

- 🇬🇧 United Kingdom contributes approximately **82% of total revenue**
- 📈 Sales peak during **Q4 (October–December)**
- 🛒 Top 10 products generate a **major share** of total revenue
- 👥 Customer retention **drops sharply after Month 1**
- 🌍 Majority of international revenue comes from **European countries**

---

## 📁 Project Structure

```
Retail-Ecommerce-Analytics/
│
├── data/
│   ├── raw/                  ← Original Kaggle CSV
│   └── cleaned/              ← Cleaned dataset
│
├── notebooks/
│   ├── 01_cleaning.ipynb
│   ├── 02_eda.ipynb
│   └── 03_cohort.ipynb
│
├── exports/                  ← CSVs for Power BI
│
├── dashboard/
│   └── E-Commerce Cohort.pbix
│
├── screenshots/
│
├── README.md
└── requirements.txt
```

---

## ⚙️ How to Run

```bash
# 1. Clone the repo
git clone https://github.com/Suraj-monarch/Ecommerce-Cohort-Analytics.git

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run notebooks in order
# 01_cleaning.ipynb → 02_eda.ipynb → 03_cohort.ipynb

# 4. Open dashboard
# Open dashboard/E-Commerce Cohort.pbix in Power BI Desktop
```

---

## 📦 Requirements

```
pandas
matplotlib
seaborn
openpyxl
jupyter
```

---

## 📌 Future Improvements

- Add sales forecasting using Linear Regression
- Integrate inventory optimization logic
- Deploy dashboard via Power BI Service
- Add RFM customer segmentation


---

⭐ If you found this project useful, consider giving it a star!
