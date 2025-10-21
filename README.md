# CAC–LTV Model Analysis (Power BI) — SaaS Business Insights

## **Project Summary**
This project analyzes a **synthetic dataset** modeling **Customer Acquisition Cost (CAC)**, **Lifetime Value (LTV)**, and **retention dynamics** for a fictional SaaS business operating across six global regions.  
The analysis explores:
- CAC calculations by acquisition channel  
- LTV calculations based on ARPU, gross margin, and churn rate  
- LTV:CAC ratios  
- ARPU & Revenue by region  
- Cohort analysis and retention trends  

Visualizations include KPI cards, column & line charts, cohort heatmaps, and ARPU matrices by region.

> **Note:** This is a synthetic dataset. CAC values are **lower than real-world benchmarks** due to randomized marketing spend in a narrow range.  
> In practice, CAC can be **3–10× higher**, depending on industry, region, and product type.

---

## **Key Objective**
- Quantify **LTV** and **LTV:CAC ratio**  
- Evaluate **customer acquisition efficiency** and **cohort retention patterns** to support data-driven business decisions

---

## **About the CAC–LTV Model**
**Customer Lifetime Value (LTV)** estimates the **total revenue a customer generates over their relationship** with a company.  
It accounts for both revenue per customer and the associated costs of acquiring and serving that customer.

For SaaS companies, understanding LTV is critical because it drives decisions on **marketing investment, pricing, product development,** and **growth strategy.**

The **LTV:CAC ratio** provides a quick view of **unit-economic health**:
- **High ratio (>3×)** → efficient growth and good scalability  
- **Low ratio (<2×)** → acquisition costs are too high or retention too weak  

### **LTV Formula**
```
LTV = (Average Revenue per User (ARPU) × Gross Margin %) / Average Churn Rate
```

### **LTV:CAC Ratio**
```
LTV:CAC = Lifetime Value (LTV) ÷ Customer Acquisition Cost (CAC)
```

To optimize this ratio, a SaaS business must:
- **Increase LTV** (raise ARPU, improve gross margin, lower churn)  
- **Reduce CAC** (improve targeting efficiency and channel mix)  
- **Sustain retention**, ensuring churn does not offset efficiency gains  

---

## **Business Questions**
1. Which acquisition channels are **cost-effective** and bring in the most valuable customers (**highest LTV**)?  
2. Which regions contribute the most **Revenue**, and how do **ARPU** and **LTV** differ by region?  
3. How does **user retention** change over time, and where should we **intervene to reduce churn**?

---

## **Dataset Overview**
**Rows:** 7,057  **Columns:** 15  
**Source:** Synthetic data for internal modeling and visualization only.  

### **Table Schema**

| Column | Data Type | Description |
|:--|:--|:--|
| **year** | Whole Number | Year of customer signup or activity. |
| **month** | Whole Number | Month of signup or activity (1–12). |
| **customer_id** | Whole Number | Unique identifier for each customer. |
| **acquisition_channel** | Text | Channel used to acquire customers (e.g., Google Ads, Meta Ads, Outbound Sales, Organic Search). |
| **signup_source** | Text | Source or method by which a customer signed up (e.g., website, referral, outbound campaign). |
| **region** | Text | Customer’s geographic region (e.g., North America, Europe, APAC, LatAm, Middle East, Africa). |
| **customer_tier** | Text | Subscription tier (Basic, Pro, Enterprise). |
| **plan_price** | Decimal | Standard monthly plan price before discounts. |
| **discount_rate** | Decimal | Discount fraction applied to plan (0–1). |
| **arpu** | Decimal | Average Revenue Per User – monthly revenue per active customer. |
| **gross_margin** | Decimal | Gross profit margin fraction (0–1) after direct costs. |
| **churn_rate** | Decimal | Monthly churn probability – proportion of users who cancel. |
| **contract_length_month** | Whole Number | Subscription term length (1 or 12 months). |
| **marketing_spend** | Decimal | Marketing acquisition cost per customer. |

---

## **Usage & Visualization**
The analysis is performed using **Power BI**.  
Core report pages include:
1. **Executive Overview** — KPI cards, CAC vs. LTV, LTV:CAC ratio.  
2. **By Channel** — CAC, LTV, Churn, and ROI comparisons.  
3. **By Region** — Revenue, ARPU, and LTV breakdowns.  
4. **Retention Analysis** — Cohort heatmap, retention trends, churn intervention points.

---

## **Key Insights Summary**
- **Organic Search** is the most cost-efficient channel (lowest CAC, highest LTV:CAC ratio).  
- **North America & Europe** dominate revenue via scale; **Africa** and **LatAm** offer high ARPU and LTV potential despite smaller bases.  
- **Retention stability** averages ~94.7% monthly, with strongest performance in **mid-2024 cohorts** (70–80% retained by month 6).  
- Focus retention improvements on **months 2–4** (steepest churn drop) and **renewal months 6–9** for greatest LTV impact.

---

## **License**
MIT License
