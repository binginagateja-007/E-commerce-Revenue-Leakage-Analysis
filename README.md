# E-commerce-Revenue-Leakage-Analysis

## 🎯 Project Overview

This project analyzes **3 years of e-commerce transaction data** (2023-2025) to identify revenue leakage patterns and profitability risks across a multi-region platform. Using Python data analysis libraries, I uncovered **$4.4M in annual revenue losses** due to product returns and developed a composite risk scoring model to prioritize strategic interventions.

### Key Achievement
Built a data-driven framework that identified Fashion category as the primary financial risk driver, where reducing return rates from 12% to 8% could recover substantial profit without acquiring new customers.

---

## 📁 Project Structure

```
├── Analysis.ipynb          # Main Jupyter notebook with complete analysis
├── synthetic.csv           # Dataset (synthetic e-commerce transactions)
├── README.md              # Project documentation
```

---

## 🔍 Business Problem

**Challenge:**  
While overall revenue appeared stable at $73.4M, the company needed to understand:
- How much revenue was being lost to product returns?
- Which product categories posed the greatest financial risk?
- What strategic interventions would maximize profitability?

**Objective:**  
Identify category-level vulnerabilities, quantify financial impact, and provide actionable recommendations to reduce revenue leakage.

---

## 📊 Dataset

**Source:** Synthetic e-commerce transaction data  
**Time Period:** January 2023 - December 2025  
**Records:** 12,000+ transactions  
**Regions:** North America, Europe, Asia  

**Key Features:**
- Order details (order_id, customer_id, order_date)
- Product information (category, price, quantity)
- Transaction data (revenue, discount_percent, payment_method)
- Customer behavior (is_returned, customer_rating, delivery_days)
- Geographic data (region)

---

## 🛠️ Tools & Technologies

- **Python 3.8+**
- **Pandas** - Data manipulation and aggregation
- **NumPy** - Numerical computations and array operations
- **Matplotlib** - Data visualization and plotting
- **Jupyter Notebook** - Interactive development environment

---

## 📈 Methodology

### Phase 1: Data Loading & Exploration
- Loaded dataset and performed initial exploration
- Identified 13 columns across 12,000+ transactions
- Examined data distributions and unique values

### Phase 2: Data Cleaning
- Converted `order_date` to datetime format
- Extracted year and month features for temporal analysis
- Validated data types and checked for missing values
- No duplicates or missing data found

### Phase 3: Revenue Validation
- Recalculated revenue: `price × quantity × (1 - discount%)`
- Validated against provided revenue column
- Identified 31 minor discrepancies (max difference: $0.01)
- Confirmed data integrity for analysis

### Phase 4: Return & Leakage Analysis
- Calculated overall return rate: **6.06%**
- Quantified revenue tied to returns: **$4.41M**
- Created category-level return metrics
- Analyzed discount impact on return behavior

### Phase 5: Temporal Analysis
- Examined monthly and yearly revenue trends
- Identified seasonal return patterns
- Created pivot tables for year-over-year comparison
- Detected November/December return rate increases

### Phase 6: Regional Analysis
- Compared return rates across geographic regions
- Calculated regional revenue loss percentages
- Analyzed Fashion category performance by region
- Identified Europe as highest revenue loss contributor

### Phase 7: Profit Simulation
- Assigned cost-to-revenue ratios by category
- Calculated profit margins for each transaction
- Simulated net profit impact of returns
- Overall profit margin: **22.38%**

### Phase 8: Leakage Risk Scoring Model
- Developed composite risk score using:
  - Return rate (normalized)
  - Revenue loss percentage (normalized)
  - Profit margin (inverse normalized)
  - Profit loss (normalized)
- Ranked categories from highest to lowest risk
- Created strategic prioritization framework

---

## 🔑 Key Findings

### 1. Overall Financial Impact
- **Total Revenue:** $73.41M
- **Revenue Lost to Returns:** $4.41M (6%)
- **Net Revenue After Returns:** $69.01M
- **Overall Profit:** $15.44M
- **Profit Margin:** 22.38%

### 2. Category-Level Insights

| Category    | Return Rate | Revenue Loss | Profit Margin | Risk Score |
|-------------|-------------|--------------|---------------|------------|
| Fashion     | **12.0%**   | **$1.27M**   | 24%           | **Highest** |
| Electronics | 6.1%        | $634K        | **11%**       | High |
| Automotive  | 5.9%        | $602K        | 20%           | Medium |
| Sports      | 6.0%        | $572K        | 25%           | Medium |
| Beauty      | **5.1%**    | **$429K**    | **33%**       | **Lowest** |

**Critical Findings:**
- **Fashion** shows 2x higher return rate (12%) vs platform average (6%)
- **Electronics** has lowest profit margin (11%), making it vulnerable to returns
- **Beauty** demonstrates best performance: highest margin (33%) + lowest returns (5%)

### 3. Discount Analysis
- Return rates remain **stable across discount levels** (0%-20%)
- Average discount for returned items: 9.91%
- Average discount for kept items: 9.99%
- **Conclusion:** Discounting is NOT the primary driver of returns

### 4. Regional Patterns
- Return rates similar across regions (5.8% - 6.3%)
- **Europe** contributes highest revenue loss percentage
- Fashion returns consistent across all regions

### 5. Temporal Trends
- Slight return rate increase in **November/December** (promotional seasons)
- Year-over-year revenue remains stable
- Consistent return patterns across 3 years

---

## 💡 Strategic Recommendations

### 1. **Reduce Fashion Return Rate** (Highest Priority)
**Current Impact:** 12% return rate = $867K profit loss

**Actions:**
- Improve product descriptions and size accuracy
- Implement virtual fitting technology or size recommendation algorithms
- Analyze customer-level return patterns to identify serial returners
- Offer store credit instead of refunds to retain revenue
- Add customer reviews with fit feedback

**Estimated Impact:** Reducing return rate from 12% → 8% could recover $300K+ in profit

---

### 2. **Protect Electronics Margins**
**Current Impact:** 11% margin makes returns particularly costly

**Actions:**
- Negotiate better supplier costs to increase margin buffer
- Reduce deep discount campaigns (20%+ off)
- Implement bundle pricing instead of individual discounts
- Improve product quality checks before shipment
- Enhance product documentation to reduce confusion-based returns

---

### 3. **Focus Growth on High-Performing Categories**
**Opportunity:** Beauty and Home show strong profitability + low leakage

**Actions:**
- Shift marketing budget toward Beauty and Home categories
- Expand product selection in high-margin categories
- Use Beauty/Home as customer acquisition channels
- Cross-sell high-margin items with high-return categories

---

### 4. **Implement Seasonal Return Controls**
**Pattern:** Return rates increase during November/December

**Actions:**
- Adjust return policies during peak promotional periods
- Reduce return windows from 30 → 14 days for sale items
- Implement restocking fees for final sale periods
- Communicate return policies clearly during checkout

---

## 📊 Visualizations

The analysis includes 12 professional visualizations:

1. **Leakage Risk Score** - Composite risk ranking by category
2. **Profit Margin by Category** - Profitability comparison
3. **Return Rate by Category** - Return behavior patterns
4. **Monthly Return Trend** - Temporal analysis
5. **Profit Loss by Category** - Dollar impact of returns
6. **Revenue Loss by Region** - Geographic patterns
7. **Return Rate by Region** - Regional comparison
8. **Risk Quadrant** - Profit margin vs return rate scatter plot
9. **Category × Region Heatmap** - Multi-dimensional analysis
10. **Discount vs Return Scatter** - Discount impact analysis
11. **Correlation Matrix** - Feature relationship analysis
12. **Additional supporting charts**

---

## 🚀 How to Run This Project

### Prerequisites
```bash
Python 3.8 or higher
Jupyter Notebook
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/ecommerce-revenue-leakage-analysis.git
cd ecommerce-revenue-leakage-analysis
```

2. **Install required packages**
```bash
pip install pandas numpy matplotlib jupyter
```

3. **Launch Jupyter Notebook**
```bash
jupyter notebook Analysis.ipynb
```

4. **Run all cells** to reproduce the analysis

---

## 📌 Key Learnings

### Technical Skills Developed
- Advanced Pandas operations (groupby, aggregations, pivot tables)
- Creating custom metrics and scoring models
- Multi-dimensional data analysis
- Data visualization best practices with Matplotlib
- Data validation and quality assurance

### Business Insights Gained
- Revenue growth ≠ profitability (category-level analysis is critical)
- Low-margin products are high-risk even with moderate returns
- Operational improvements (reducing returns) can drive profit without new sales
- Discounting isn't always the problem - product quality and description accuracy matter more

---


*This project demonstrates end-to-end data analysis skills including data cleaning, exploratory analysis, statistical analysis, business intelligence, and strategic recommendation development.*
