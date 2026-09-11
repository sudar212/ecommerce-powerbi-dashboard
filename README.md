# 🛒 E-Commerce Customer Analytics & Retention Intelligence

An end-to-end data analytics pipeline and interactive Power BI dashboard engineered to evaluate customer lifetime behavior, segment buyer cohorts using RFM methodology, and detect churn indicators across retail transactions.

---

## 📊 Executive Dashboard Preview

### Page 1: Executive KPI & Revenue Overview
![Page 1 Overview](dashboard_page1.png)

### Page 2: Customer Retention & RFM Matrix
![Page 2 Retention](dashboard_page2.png)

---

## 🚀 Business Impact & Key Metrics

* **Total Revenue Analyzed:** £17.32M across multi-year retail transactions.
* **Total Retained Customer Base:** 5,860 unique customers analyzed with zero data loss.
* **Customer Churn Rate:** 38.00% benchmarked at a 90-day inactivity threshold.
* **Revenue At Risk:** £1.92M identified in dormant and slipping customer cohorts.
* **Pareto Revenue Concentration:** Top customer segment (*Champions*) accounts for 65.49% (£11.35M) of total enterprise revenue.

---

## 🛠️ Architecture & Technical Stack

SQLite Database (retail_warehouse.db)
│
▼
Python ETL Pipeline (export.py - Pandas, NumPy)
├── Rank-based transaction ordering using DB ROWID
├── Deterministic Recency, Frequency, and Monetary scoring (1-5)
└── Cohort categorization (Champions, Loyal, At-Risk, Lost)
│
▼
Power BI Semantic Model & Report (.pbix)
├── Star-schema data modeling
├── DAX measures for Revenue, Churn %, and Risk Value
└── Modern executive UI with interactive multi-attribute slicers


---

## 📌 RFM Segmentation Logic

| Segment | RF Score Criteria | Business Strategy |
| :--- | :--- | :--- |
| **Champions** | 55, 54, 45 | VIP rewards, early product launches, retention incentives |
| **Loyal Customers** | 53, 44, 35, 34 | Upsell higher AOV items, loyalty program enrollment |
| **Promising / New** | 52, 51, 42, 41 | Onboarding journeys, brand engagement discounts |
| **Need Attention** | 33, 32, 23 | Limited-time reactivation deals |
| **At Risk** | 25, 24, 15, 14 | Win-back email flows, churn prevention surveys |
| **Lost / Churned** | 11, 12, 21, 22 | Low-cost re-engagement or archive |

---

## 📂 Project Repository Structure

* `Ecommerce Sample.pbix`: Power BI production dashboard file.
* `export.py`: Python script handling SQLite extraction and RFM rank transformation.
* `dashboard_page1.png`: High-resolution visual of the executive overview page.
* `dashboard_page2.png`: High-resolution visual of the customer retention matrix page.
