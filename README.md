# 🛒 E-Commerce Revenue Leakage & Profitability Analysis

![Python](https://img.shields.io/badge/Python-Analysis-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Computation-013243?style=for-the-badge&logo=numpy)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

A **Python-based Exploratory Data Analysis (EDA) project** that investigates revenue leakage and profitability erosion across an e-commerce retailer's product categories.

---

## 📌 The Problem

The retailer was losing money and didn't know exactly where. Revenue leakage, return spikes, and steep item-level discounting were eroding profit margins — but this was happening **blindly**, across multiple retail categories with no monitoring in place to isolate which categories, products, or behaviors were responsible.

Specifically:

- No one could say which product categories were driving the losses versus which were healthy
- Returns were increasing but not tied back to specific products, price points, or discount levels
- Discounting was applied without visibility into whether it was actually protecting or destroying margin
- The retailer was operating with an estimated **$4.4M profitability deficit** with no clear diagnostic behind it

---

## 📂 The Data

Transaction-level e-commerce data covering **12,000+ transaction lines**, including:

- Order Date & Transaction ID
- Product / Category
- Unit Price, Discount %, Quantity
- Return Status
- Revenue & Cost/Margin fields

---

## 🛠️ What Was Built

### Tech Stack

| Technology | Purpose |
|------------|----------|
| Python | Core Analysis |
| Pandas | Data Wrangling & Aggregation |
| NumPy | Numerical Computation |
| EDA | Root-Cause Investigation |

### Approach

- Performed structured **Exploratory Data Analysis** across all 12,000+ transaction lines to build a category-by-category profitability picture
- Segmented the data by category, discount tier, and return status to isolate where margin was actually being lost — rather than assuming losses were spread evenly
- Cross-referenced discount depth against return rate and net margin per category to test whether aggressive discounting was correlated with higher returns and lower profitability
- Quantified the exact contribution of each driver (returns, discounting, category mix) to the overall deficit, rather than treating it as a single unexplained number

---

## 🎯 Key Insights Found

- Isolated the **exact operational drivers** behind the $4.4M deficit — pinpointing which categories and behaviors (rather than the business as a whole) were responsible
- Found a set of high-risk products where deep discounting was correlated with disproportionately high return rates, actively destroying margin rather than driving profitable volume
- Identified specific retail categories where return spikes were concentrated, versus categories that were performing normally
- Quantified how much aggressive discounting was contributing to margin erosion versus returns alone — showing the two problems were compounding each other in certain categories
- The analysis supported a **15% reduction in aggressive discounting** on the flagged high-risk products as a direct, data-backed lever for margin recovery

---

## 📁 Suggested Project Structure

```
E-commerce-Revenue-Leakage-Analysis
│
├── Dataset
├── Notebooks
│   └── Revenue_Leakage_EDA.ipynb
├── Reports
│   └── Category_Profitability_Summary.csv
└── README.md
```

---

## 🎓 Learning Outcomes

This project strengthened my skills in:

- Exploratory Data Analysis (EDA) at scale
- Root cause analysis using Pandas/NumPy
- Translating raw transaction data into category-level profitability diagnostics
- Quantifying the financial impact of specific operational drivers
- Communicating data-driven findings in a form category managers could act on

---

## 🚀 Future Improvements

- Automate the EDA into a recurring monthly profitability audit
- Build a Power BI dashboard on top of the analysis for ongoing monitoring
- Add predictive flagging for products at risk of margin erosion before losses accumulate
- Extend root-cause analysis to supplier/vendor-level factors

---

## 👨‍💻 Author

**Bingi Nagateja** — Aspiring Data Analyst

Skills: Python, Pandas, NumPy, EDA, Statistical Analysis, Root Cause Analysis, Data Visualization

---

⭐ If you found this project useful, don't forget to star this repository!
