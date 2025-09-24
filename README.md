# 📊 Vendor & Inventory Performance Analysis  

## 📌 Business Problem  
Companies often **lose millions due to inefficient vendor management, slow-moving inventory, and inconsistent profit margins**.  
This project aims to **analyze vendor performance, identify inventory inefficiencies, and recommend strategies to improve profitability**.  

**Key Questions Answered:**  
- Which vendors drive the most profit — and which negatively affect margins?  
- How efficiently are purchases converted into sales?  
- Are there opportunities to optimize pricing, freight, and procurement strategies?  

---

## 🔍 Project Approach  
I approached this analysis like a **real-world supply chain consulting engagement**:  

1. **Data Exploration & Cleaning**  
   - Consolidated multiple tables into a single vendor-performance dataset.  
   - Flagged negative profits, zero-sales SKUs, and missing values.  

2. **Exploratory Data Analysis (EDA)**  
   - Investigated pricing, profit margins, sales-to-purchase ratios, stock turnover, and freight costs.  
   - Identified outliers and anomalies to ensure data quality before advanced analysis.  

3. **Statistical Analysis & Hypothesis Testing**  
   - Examined correlations between purchase price, sales revenue, gross profit, and stock turnover.  
   - Conducted t-tests to verify differences in profit margins between top- and low-performing vendors.  

4. **Business Insights & Recommendations**  
   - Translated findings into actionable strategies for procurement, pricing, and inventory optimization.  

---

## 📊 Key Findings  

### 1. Summary Statistics  
| Metric | Observation |
|--------|-------------|
| **Gross Profit** | Min: −₹52,002.78 → Some SKUs sold at a loss, likely due to discounts or high purchase prices |
| **Profit Margin** | Invalid values for some SKUs due to division by zero → Need filtering of zero-sales SKUs |
| **Total Sales Quantity & Dollars** | Min: 0 → Some inventory purchased but never sold, potential slow movers or obsolete stock |
| **Purchase & Actual Prices** | High variance (₹24.39 avg vs ₹5,681.81 max) → Presence of low-cost and premium products |
| **Freight Cost** | ₹0.09–₹257,032.07 → Logistics efficiency varies greatly |
| **Stock Turnover** | 0–274.5 → Mix of unsold, normal, and fast-moving products |
| **Sales-to-Purchase Ratio** | 0–352.9 → Some SKUs sold entirely from stockpile, signaling inventory imbalance |

---

### 2. Correlation Insights  
| Variables | Correlation | Business Insight |
|-----------|-------------|-----------------|
| Purchase Price ↔ Total Sales Dollars | −0.012 | Purchase cost has minimal impact on total sales revenue |
| Total Purchase Qty ↔ Total Sales Qty | 0.999 | Purchases align closely with sales — **efficient inventory management** |
| Profit Margin ↔ Total Sales Price | −0.179 | Higher sales prices tend to lower margins → pricing strategy consideration |
| Stock Turnover ↔ Profit Margin | −0.055 | Fast-moving products don’t always yield higher profitability |

---

### 3. Vendor Profit Margin Analysis  

- **Low-performing vendors:** 95% CI = 40.48–42.62% → Higher margins, likely premium/niche products  
- **Top-performing vendors:** 95% CI = 30.74–31.61% → Lower margins despite higher sales  

**Hypothesis Testing:**  
- **H₀:** No difference in mean profit margins between vendor groups  
- **Hₐ:** Significant difference exists  
- **Result:** p < 0.001 → Reject H₀. Profit margins differ significantly between top and low-performing vendors.  

**📷 95% Confidence Interval Visualization**  
![Profit Margins 95% CI](<img width="1266" height="739" alt="Screenshot 2025-09-24 152206" src="https://github.com/user-attachments/assets/84c46933-b719-4d35-8935-5e2feaf8d35f" />
)  

---

### 4. Vendor Contribution to Total Purchases  

- Majority of purchase dollars are concentrated among a few vendors → **focus on high-value vendors for negotiations**  
- Remaining vendors account for smaller purchases → **monitor for cost-effectiveness and slow movers**  

**📷 Vendor Contribution Visualization**  
![Vendor Purchase Contribution](<img width="1239" height="740" alt="Screenshot 2025-09-24 152125" src="https://github.com/user-attachments/assets/d8b69a09-02af-4515-8275-59557e4b3539" />
)  

---

## 💡 Business Recommendations  
- **Eliminate or renegotiate loss-making SKUs** to prevent revenue leakage.  
- **Optimize freight costs** by consolidating shipments or reviewing high-cost vendors.  
- **Leverage bulk purchase discounts** to reduce per-unit costs and increase margins.  
- **Segment vendors** based on profit contribution → tailor procurement and pricing strategies.  
- **Focus marketing and distribution** for low-performing but high-margin vendors.  
- **Automate zero-sales filtering** to prioritize revenue-generating SKUs.  

---

## ✅ Next Steps  
1. Develop **interactive dashboards** for vendor performance, profit margins, and inventory turnover.  
2. Build **predictive models** for profit margin forecasting and stock movement prediction.  
3. Present findings to procurement and finance teams to guide strategic decisions.  

---

## 🎯 Business Impact  
By implementing these recommendations, companies can:  
- Reduce **logistics costs** by up to 20%  
- Improve **profit margins** through optimized pricing and vendor strategies  
- Minimize **inventory holding costs** by identifying slow movers  
- Establish a **data-driven vendor negotiation framework**  
v
