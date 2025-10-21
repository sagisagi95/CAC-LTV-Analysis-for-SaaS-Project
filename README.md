# [Power BI] CAC–LTV Model Analysis for SaaS Business

## 📝 **Project Summary**
This project analyzes a synthetic dataset modeling **Customer Acquisition Cost (CAC)**, **Lifetime Value (LTV)**, and **retention dynamics** for a fictional SaaS business operating across six global regions.  
The analysis explores:
- CAC calculations by acquisition channel  
- LTV calculations based on ARPU, gross margin, and churn rate  
- LTV:CAC ratios  
- ARPU & Revenue by region  
- Cohort analysis and retention trends  

Visualizations include KPI cards, column & line charts, cohort heatmaps, and ARPU matrix by region.

> **Note:** This is a synthetic dataset. CAC values are lower than real-world benchmarks due to randomized marketing spend in a narrow range. In practice, CAC can be 3–10× higher, depending on industry, region, and product type.

---

## 🎯 **Key Objective**
- Quantify **LTV** and **LTV:CAC ratio**  
- Evaluate **customer acquisition efficiency** and **cohort retention patterns** to support data-driven business decisions

## ⚠️ **About the CAC–LTV Model**
**Customer Lifetime Value (LTV)** estimates *the total revenue a customer generates over their relationship with a company*.  
It takes into account the generated revenue per customer and the associated costs of acquiring and serving that customer.

For SaaS companies, LTV is critical because it drives decisions on marketing investment, pricing, product development, and growth strategy. 

The LTV:CAC ratio can also provide insight into the unit-economic health. To optimize the LTV:CAC ratio, a SaaS company must maximize lifetime value (LTV) and minimize customer acquisition costs (CAC), while ensuring the impact on the retention rate is marginal (i.e. customer churn does not offset the benefits).

### **LTV Formula**
```
LTV = (Average Revenue per User (ARPU) × Gross Margin %) / Average Churn Rate
```

### **LTV:CAC Ratio**
```
LTV:CAC = Lifetime Value (LTV) ÷ Customer Acquisition Cost (CAC)
```

## ❓ **Business Questions**
1. Which acquisition channels are cost-effective and bring in the most valuable customers (highest LTV)?  
2. Which regions contribute the most **Revenue**, and how do ARPU and LTV differ by region?  
3. How does user retention change over time, and where should we intervene to reduce churn?

---

## 🗂️ **Dataset Overview**
**Name:** CAC-LTV Model Analysis for SaaS Business Insights
**Source:** https://www.kaggle.com/datasets/ameernassar/cac-ltv-model?select=cac_ltv_model.csv

### **Table Schema**
Rows: 7057; Columns: 15
| Column | Data Type | Description |
|:--|:--|:--|
| **year** | INT | Year of customer signup or activity. |
| **month** | INT | Month of signup or activity (1–12). |
| **customer_id** | INT | Unique identifier for each customer. |
| **acquisition_channel** | TEXT | Channel used to acquire customers (e.g., Google Ads, Meta Ads, Outbound Sales, Organic Search). |
| **signup_source** | TEXT | Source or method by which a customer signed up (e.g., website, referral, outbound campaign). |
| **region** | TEXT | Customer’s geographic region (e.g., North America, Europe, APAC, LatAm, Middle East, Africa). |
| **customer_tier** | TEXT | Subscription tier (Basic, Pro, Enterprise). |
| **plan_price** | FLOAT | Standard monthly plan price before discounts. |
| **discount_rate** | FLOAT | Discount fraction applied to plan (0–1). |
| **arpu** | FLOAT | Average Revenue Per User – monthly revenue per active customer. |
| **gross_margin** | FLOAT | Gross profit margin fraction (0–1) after direct costs. |
| **churn_rate** | FLOAT | Monthly churn probability – proportion of users who cancel. |
| **contract_length_month** | INT | Subscription term length (1 or 12 months). |
| **marketing_spend** | FLOAT | Marketing acquisition cost per customer. |

---

## 📊 **Usage & Visualization**
The analysis is performed using **Power BI**.  
[View Dashboard Report (Power BI PDF)](dashboard_cac_ltv_analysis.pdf)
Report pages include:
1. **Overview** — Total Revenue & MKT Spend, ARPU, LTV, LTV:CAC ratio
2. **Acquisition Efficacy** — Spend allocation, CAC, Churn rate, Retention cohorts
3. **LTV Analysis** — ARPU and LTV breakdowns

<img width="988" height="555" alt="image" src="https://github.com/user-attachments/assets/54144ef8-3517-4fc9-8eea-cef599b544a1" />
<img width="983" height="552" alt="image" src="https://github.com/user-attachments/assets/f10c925c-8fc7-47b9-ae5b-3673c59a0287" />
<img width="984" height="550" alt="image" src="https://github.com/user-attachments/assets/ffb0f516-bfd8-4149-87c3-0f6c281dfe54" />

---

## 💡 **Key Insights Summary**
- **Organic Search** is the most cost-efficient channel (lowest CAC, highest LTV:CAC ratio).  
- **North America & Europe** dominate revenue via scale; Prioritize scaling acquisition in **Africa & LatAm** with potential high-value customers
- Healthy retention (churn ~5%), focus retention improvements on **months 2–4** (steepest churn drop) and **renewal months 6–9** for greatest LTV impact.

[View Detailed Analysis PDF](ExecutiveSummary.pdf)

---

