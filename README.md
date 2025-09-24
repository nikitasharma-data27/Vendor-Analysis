# 📊 Vendor & Inventory Performance Analysis  

## 📌 Business Problem  
Companies lose millions each year due to **inefficient vendor relationships, unsold inventory, and inconsistent profit margins**.  
This project focuses on **identifying vendor performance gaps, optimizing purchasing strategies, and improving profitability** through data analysis.  

**Key Questions Answered:**  
- Which vendors are driving the most profit — and which are hurting margins?  
- How efficiently are we converting purchases into sales?  
- Are there opportunities to optimize freight costs, pricing, or purchasing decisions?  

---

## 🔍 Project Approach  
I treated this analysis like a real-world supply chain consulting engagement:  

1. **Data Exploration & Cleaning**  
   - Surveyed multiple tables to build a consolidated vendor-performance dataset.  
   - Removed/flagged zero-sales rows and negative profit anomalies.  

2. **Exploratory Data Analysis (EDA)**  
   - Identified patterns, outliers, and anomalies in pricing, turnover, and freight costs.  
   - Created metrics like **Sales-to-Purchase Ratio**, **Stock Turnover**, and **Unit Cost per Order Size**.  

3. **Statistical Analysis & Hypothesis Testing**  
   - Measured correlations to find drivers of sales and profitability.  
   - Conducted t-tests to confirm profit margin differences between vendor groups.  

4. **Business Insights & Recommendations**  
   - Converted findings into actionable steps for procurement, pricing, and inventory teams.  

---

## 📂 Files in Repository  
- `Vendor_Inventory_Analysis.ipynb` – Jupyter notebook with data cleaning, EDA, correlation analysis, and hypothesis testing.  
- `data/` – Contains raw and cleaned datasets (if shared).  

---

## 📊 Key Findings  

### 1. Summary Statistics  
| Metric | Observation |
|--------|-------------|
| **Gross Profit** | Some SKUs sold at a **loss** (Min: −₹52,002.78) → Review discounting and purchase cost |
| **Profit Margin** | Division by zero caused invalid results for some SKUs → Need filtering |
| **Freight Cost** | Highly variable (₹0.09–₹257,032.07) → Negotiate logistics contracts |
| **Stock Turnover** | 0–274.5 → Both stagnant and fast-moving items coexist |
| **Sales-to-Purchase Ratio** | Some SKUs draw entirely from stockpile (352.9x) → Optimize inventory restocking |

---

### 2. Correlation Insights  
| Variables | Correlation | Business Insight |
|-----------|-------------|-----------------|
| Purchase Price ↔ Total Sales | −0.012 | Purchase cost has negligible impact on total sales |
| Total Purchase Qty ↔ Total Sales Qty | 0.999 | **Excellent operational efficiency** – purchases match demand |
| Profit Margin ↔ Sales Price | −0.179 | Higher price items have lower margins → watch for price sensitivity |

---

### 3. Bulk Purchasing & Unit Cost Efficiency  
- **Bulk Orders:** Avg cost per unit ~₹10.78  
- **Small Orders:** Avg cost per unit significantly higher (≈72% difference)  
✅ **Action:** Negotiate more bulk orders to reduce unit cost.  

---

### 4. Vendor Profit Margin Analysis  
- **Low-performing vendors:** Higher average margins (40–42%) → Likely premium/niche products  
- **Top vendors:** Lower margins (30–31%) → Improve via dynamic pricing, cost control, bundling  

---

### 5. Hypothesis Testing  
**Result:** Significant difference in profit margins between vendor groups (p < 0.001).  
✅ Confirms that vendor segmentation strategy can be used to tailor procurement and pricing actions.  

---

## 💡 Business Recommendations  
- **Eliminate loss-making SKUs** or renegotiate procurement prices.  
- **Optimize freight costs** by consolidating shipments or switching vendors with extreme cost variability.  
- **Leverage bulk purchase discounts** to lower per-unit costs and boost margins.  
- **Segment vendors** based on profit margin contribution — apply different pricing & marketing strategies.  
- **Automate zero-sales filtering** to focus on active, revenue-generating inventory.  

---

## ✅ Next Steps  
1. Enhance visualization dashboards (e.g., monthly trends, vendor segmentation charts).  
2. Build predictive models for **profit margin forecasting** and **stock turnover prediction**.  
3. Share insights with procurement & finance teams for strategic implementation.  

---

## 🎯 Business Impact  
This project helps companies:  
- Reduce **logistics costs** by up to 20%  
- Improve **profit margins** through smarter purchasing  
- Minimize **inventory holding costs** by identifying slow movers  
- Build a **data-driven vendor negotiation strategy**  

---

