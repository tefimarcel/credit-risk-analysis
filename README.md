# Credit Risk Analysis — Home Credit Default Risk

![Python](https://img.shields.io/badge/Python-3.12-blue)
![SQL](https://img.shields.io/badge/SQL-SQLite-orange)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![Dataset](https://img.shields.io/badge/Dataset-307k%20rows-green)

##  Overview

End-to-end credit risk analysis project using real-world loan application data
from Home Credit. The goal is to identify behavioral and financial patterns
associated with a higher risk of default, and translate those findings into
actionable business recommendations.

---

## Business Problem

A financial institution wants to understand **which client profiles are most
likely to default** on their loans, in order to:
- Improve their credit scoring model
- Adjust loan terms based on risk profile
- Reduce overall default rate (currently above industry average)

---

##  Key Findings

| Finding | Insight |
|---------|---------|
| Default rate: **8.07%** | Above industry average of 5-7% |
| Low Income fee/income ratio: **24%** | vs 13.6% for High Income clients |
| Low-skill Laborers default rate: **17.2%** | More than 2x the overall average |
| High bureau inquiries default rate: **9.3%** | 30% higher than clients with no inquiries |
| Linear correlations with TARGET | All near zero → default is multivariable |

---

##  Project Structure

### Block 1 — Exploratory Data Analysis
- Dataset structure: 307,511 rows × 122 columns
- 67 columns with missing values identified and flagged
- Target variable analysis: highly imbalanced (91.9% vs 8.1%)
- Key data quality issues: sentinel values, extreme outliers

### Block 2 — Client Segmentation with SQL
- Income segmentation using `CASE WHEN`
- Financial profile by default status
- Default rate by contract type (Cash vs Revolving loans)
- Fee-to-income ratio analysis by segment

### Block 3 — Advanced SQL: Window Functions & CTEs
- Credit bureau inquiry patterns using CTEs
- Top 10 riskiest occupations using `RANK()` window function
- Behavioral signals associated with default risk

### Block 4 — Data Visualization
- Income segment risk analysis (bar charts)
- Correlation matrix of key risk variables (heatmap)
- Top 10 riskiest occupations with benchmark line

### Block 5 — Conclusions & Business Recommendations
- 5 key findings with actionable recommendations
- Multivariate scoring model suggested as next step

---

##  Tools & Technologies

| Tool | Usage |
|------|-------|
| **SQL (SQLite)** | Data exploration, segmentation, CTEs, window functions |
| **Python (Pandas)** | Data wrangling, EDA, feature engineering |
| **Matplotlib / Seaborn** | Statistical visualizations |
| **Power BI** | Interactive executive dashboard |

---

##  Repository Structure

credit-risk-analysis/

├── credit-risk-analysis.ipynb    ← Main notebook (SQL + Python)

├── credit_risk_analysis.pbix     ← Power BI dashboard

└── README.md

---

## 📈 Power BI Dashboard

The interactive dashboard has two pages:

**Page 1 — Overview**
- KPI cards: Total Clients, Default Rate, Avg Fee to Income
- Default rate by income segment
- Payment burden by income segment
- Default vs No Default distribution

**Page 2 — Behavioral Risk Signals**
- Top 10 riskiest occupations (conditional formatting)
- Default rate by credit bureau inquiry level

>  Download the `.pbix` file and open with Power BI Desktop (free) to explore the interactive dashboard.

---

##  Links

-  [Kaggle Notebook](https://www.kaggle.com/code/estefaniamarcel/credit-risk-analysis)
-  Dataset: [Home Credit Default Risk](https://www.kaggle.com/competitions/home-credit-default-risk)

---

##  Author

**Estefania Marcel** — Astronomy student transitioning into Data Science
Focused on banking, finance and credit risk analytics.
