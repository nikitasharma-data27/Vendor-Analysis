# 📊 Vendor & Inventory Performance Analysis

## Overview
This project provides a comprehensive analysis of vendor performance, inventory efficiency, and profit margins. It combines **Exploratory Data Analysis (EDA)**, **statistical insights**, and actionable business recommendations to support data-driven decision-making.

---

## 🔎 Exploratory Data Analysis (EDA)
- Surveyed database tables to determine key variables and their relationships.
- Constructed a consolidated table capturing **vendor performance, sales, purchases, and profit metrics**.
- Explored each column to uncover **patterns, anomalies, and quality issues** before deeper analysis.

---

## 📈 Summary Statistics Insights

### 1. Negative & Zero Values
| Metric | Observation |
|--------|-------------|
| Gross Profit | Min: −₹52,002.78 — some SKUs sold at a loss due to discounts or high-cost inventory |
| Profit Margin | Min = −∞, Mean = −∞, NaN std dev — caused by division by zero when TotalSalesDollars = 0 |
| Total Sales Quantity/Dollars | Min = 0 — indicates unsold inventory that may be obsolete or slow-moving |

### 2. Outliers & High Variance
- **Purchase Price:** Avg ₹24.39, Max ₹5,681.81 — premium inventory exists  
- **Actual Price:** Avg ₹35.64, Max ₹7,499.99 — mix of luxury goods  
- **Freight Cost:** Avg ₹61,433.76, Range ₹0.09–₹257,032.07 — variable logistics behavior  
- **Stock Turnover:** Avg 1.71, Range 0–274.5 — both stagnant and fast-moving SKUs  
- **Sales-to-Purchase Ratio:** Avg 2.50, Range 0–352.9 — high ratios may reflect drawing from existing stock  

**Key Takeaways:**
- Data contains loss-making products and unsold inventory.  
- Inventory, pricing, and logistics vary widely; consider capping outliers or filtering zeroes.  

---

## 🔍 Correlation Insights
| Variables | Correlation (r) | Insight |
|-----------|----------------|---------|
| Purchase Price vs Total Sales Dollars | −0.012 | Negligible effect |
| Purchase Price vs Gross Profit | −0.016 | Negligible effect |
| Total Purchase Quantity vs Total Sales Quantity | 0.999 | High operational efficiency |
| Profit Margin vs Total Sales Price | −0.179 | Moderate negative; higher price → lower margin |
| Stock Turnover vs Gross Profit/Margin | −0.05 | Faster turnover doesn’t guarantee higher profit |

**Visualization: Heatmap of Correlations**  
![Correlation Heatmap](images/heatmap.png)

---

## 📦 Bulk Purchasing & Unit Pricing
- Large orders have the lowest unit cost (~₹10.78), compared to Small and Medium orders.  
- Unit cost difference (~72%) highlights the efficiency of **tiered pricing** for vendors.

---

## 🧩 Profit Margin Analysis: Top vs Low Sales Vendors
- **Confidence Intervals:**
  - Low-performing vendors: 40.48% – 42.62%  
  - Top-performing vendors: 30.74% – 31.61%  
- **Insight:** Lower-sales vendors enjoy higher margins, likely due to premium pricing or lower overheads.

**Business Implications:**
- **High-performing vendors:** Boost margins via dynamic pricing, cost optimization, or bundling.  
- **Low-performing vendors:** Improve marketing, pricing strategy, or distribution efficiency.

**Visualization: Comparative Vendor Margins**  
![Vendor Margins](images/bar_chart.png)

---

## 📊 Hypothesis Testing: Profit Margin Differences
- **H₀:** No difference in mean profit margins  
- **Hₐ:** Significant difference exists  
- **T-Statistic:** −17.6695  
- **P-Value:** 0.0000  

**Conclusion:** Reject H₀ — profit margins between groups are significantly different.

---

## ✅ Next Steps
1. Clean & filter out **zero-sales records** to avoid distortions.  
2. Handle **outliers** via capping, winsorizing, or vendor-specific filtering.  
3. Enhance visualizations:
   - Distribution of inventory value vs. profit margin  
   - Comparative bar charts for top/low vendor margins  

**Advanced Analysis Ideas:**
- Profit margin vs. brand, category, or seasonality  
- Time-series trends on turnover or margin  
- Regression to predict margin based on cost, sales, and logistics  

---

