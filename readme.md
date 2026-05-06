# Credit Card Customer Segmentation
**Unsupervised Machine Learning | K-Means Clustering | Power BI Dashboard**

Segmented 8,950 credit card customers into 4 distinct behavioral profiles using K-Means clustering, enabling targeted marketing strategies and proactive risk management.

---

## Project Overview

Banks hold vast amounts of customer transaction data but rarely leverage it to understand *who* their customers actually are. This project applies unsupervised machine learning to a real-world credit card dataset to answer: **Can we automatically group customers by spending behavior — and what actions should each group trigger?**

**Dataset:** UCI Credit Card Dataset (Kaggle) — 8,950 customers, 17 behavioral features including balance, purchases, cash advances, payment frequency, and credit utilization.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data cleaning & EDA |
| Scikit-learn | RobustScaler, KMeans, PCA |
| Matplotlib / Seaborn | EDA visualizations |
| Power BI | Interactive 3-page dashboard |

---

## Methodology

### Data Cleaning & EDA
- Loaded raw CSV (8,950 rows × 18 columns)
- Imputed 313 missing values in `MINIMUM_PAYMENTS` and 1 in `CREDIT_LIMIT` using **median imputation** (robust to outliers)
- Confirmed zero duplicate records
- Generated distribution plots, correlation heatmap, and boxplots
- Key finding: extreme outliers exist (PURCHASES up to ~$50K, BALANCE up to ~$18K) — preserved intentionally as they represent real high-value customers

### Clustering
- Dropped `CUST_ID` (non-informative identifier)
- Applied **RobustScaler** over StandardScaler — chosen because boxplots revealed severe outliers; RobustScaler uses median/IQR and is less distorted by extreme values
- Ran **Elbow Method** (K=1–10): no sharp elbow found — typical for real-world financial data
- Selected **K=4** for business interpretability (4 actionable customer archetypes)
- Fit `KMeans(n_clusters=4, random_state=42, n_init=10)`
- Validated clusters using **PCA 2D visualization** — clusters show meaningful separation
- Output: `clustered_customers.csv` with `Cluster` column appended

### Power BI Dashboard
- Built 3-page interactive dashboard with cluster slicer
- Page 1: Executive Overview (KPIs + segment distribution + scatter)
- Page 2: Spending Behavior (payment patterns, purchase type split, frequency matrix)
- Page 3: Risk Analysis (cash advance vs balance, cash advance frequency, business insights)

---

## Cluster Results

| Cluster | Segment | Size | Avg Purchases | Avg Balance | Avg Cash Advance | Full Pay Rate |
|---|---|---|---|---|---|---|
| C0 | **Mainstream Users** | 7,141 (79.8%) | $734 | $918 | $364 | 17% |
| C1 | **Cash Revolvers** | 1,442 (16.1%) | $579 | $4,269 | $4,081 | 4% |
| C2 | **High-Value Spenders** | 329 (3.7%) | $8,669 | $3,372 | $670 | 34% |
| C3 | **Credit Risk** | 38 (0.4%) | $1,295 | $4,693 | $1,542 | 0% |

---

## Business Insights

**Mainstream Users (79.8%)** — The backbone of the customer base. Moderate spending ($734 avg purchases), low balances, and reasonable payment behavior. Opportunity: re-engagement through cashback offers and spend-based rewards to increase transaction frequency.

**Cash Revolvers (16.1%)** — Characterized by very high cash advance usage ($4,081 avg) and near-zero full payment rate (4%). They carry large revolving balances ($4,269 avg), generating significant interest revenue for the bank. Risk: monitor for delinquency as balance-to-limit ratios grow. Action: offer balance consolidation products and financial counseling.

**High-Value Spenders (3.7%)** — The most commercially valuable segment. Highest average purchases ($8,669), highest credit limits ($9,643), and best full payment rate (34%). These customers transact heavily and pay responsibly. Action: premium card upgrades, exclusive rewards tiers, and concierge services to improve retention.

**Credit Risk (0.4%)** — Small but critical. Highest average balance ($4,693), 0% full payment rate, and elevated cash advance usage. These customers show signs of financial stress. Action: flag for early intervention by collections team; consider proactive credit limit reviews.

---

## Key Learnings

- **Outliers in financial data should be visualized, not removed** — a $50K purchase transaction is a real VIP customer, not a data error
- **No elbow bend is normal** for real-world customer datasets — business interpretability should guide K selection
- **RobustScaler > StandardScaler** when boxplots show extreme outliers — prevents high-spend customers from distorting the feature space

---

## Repository Structure

```
credit-card-clustering/
├── data/
│   ├── CC GENERAL.csv
│   └── cleaned_customers        
│   └── clustered_customers.csv       
├── notebooks/
│   ├── eda.ipynb             
├── plots/
│   ├── distributions.png
│   ├── correlation_heatmap.png
│   ├── boxplots.png
│   └── pca_clusters.png
└── README.md
```


## Dataset

[UCI Credit Card Dataset — Kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)


*Built as a portfolio project demonstrating end-to-end data science: cleaning → EDA → unsupervised ML → business insights → BI dashboard.*

<img width="1919" height="1197" alt="Screenshot 2026-05-02 093919" src="https://github.com/user-attachments/assets/39207a7d-7c23-41e8-8a17-9ca26ee12d78" />


<img width="1919" height="1196" alt="Screenshot 2026-05-02 093936" src="https://github.com/user-attachments/assets/68cc5a37-e38b-482d-a1f9-943212aacbfc" />


<img width="1918" height="1199" alt="Screenshot 2026-05-02 093954" src="https://github.com/user-attachments/assets/d1978824-150e-430c-9b9a-118e2db0d734" />


