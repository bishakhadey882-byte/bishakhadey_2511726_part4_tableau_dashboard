# Dashboard Story — Retail Sales Executive Report
**Student:** Bishakha Dey | **Student ID:** 2511726 | **Part 4:** Tableau Executive Dashboard & Data Storytelling  
**Prepared for:** Retail Leadership Team  
**Period Covered:** January 2024 – December 2025  
**Dataset:** dashboard_sales_data.xlsx (4,200 orders)

---

## 1. Executive Summary

Our retail business generated total sales of ₹21.7 Crore and profit of ₹3.33 Crore across 4,200 orders over two years (2024–2025). Sales grew by 4.3% from 2024 to 2025, and profit also improved slightly by 2.2%. The business is stable and growing, but several critical risks — particularly around discounting practices, Furniture profitability, and high return rates — need immediate leadership attention.

The dashboard tells a clear story: **Technology is our engine, the South is our strongest market, and discounts above 30% are silently eating into our profit.** This report walks through that story chart by chart.

---

## 2. What Is Performing Well

**a) Technology Category is a Profit Powerhouse**  
Technology accounts for ₹15.39 Crore in sales (71% of total) and ₹2.80 Crore in profit (84% of total profit). Sub-categories like Copiers, Accessories, and Phones are generating strong margins consistently. This is our most reliable revenue and profit engine.

**b) South Region is the Top Market**  
The South region leads all four regions with ₹6.47 Crore in sales and ₹99.88 Lakh in profit. Key states in the South are delivering strong results, and the region's performance has remained consistent across both 2024 and 2025.

**c) Sales Are Growing Year-Over-Year**  
The business moved from ₹10.62 Crore in sales in 2024 to ₹11.08 Crore in 2025. This 4.3% growth confirms the business is expanding, with new customers being acquired through multiple campaign channels including Organic, Social, and Referral.

**d) Home Office Segment Delivers Best Profitability**  
Despite all three segments being close in sales, Home Office customers consistently generate the highest profit (₹1.16 Crore), suggesting they purchase higher-margin products and are less price-sensitive than Corporate buyers.

---

## 3. What Is Underperforming

**a) Furniture Category Has Low Profit Margins**  
Furniture generates ₹5.16 Crore in sales but only ₹35.58 Lakh in profit — a profit margin of just 6.9% compared to Technology's 18.2%. Sub-categories like Tables and Bookcases frequently generate negative profit when discounts are applied, indicating a broken pricing or cost structure.

**b) East and West Regions Are Lagging**  
East (₹4.89 Cr) and West (₹4.89 Cr) regions have nearly identical and the lowest sales figures. They are significantly behind the South (₹6.47 Cr) despite having similar market sizes. This indicates untapped potential and underperforming sales strategies in these regions.

**c) Office Supplies Contribute Minimally to Profit**  
Office Supplies represents only ₹1.15 Crore in sales and ₹17.05 Lakh in profit — the smallest category by far. Sub-categories like Binders, Paper, and Art are low-ticket items with thin margins, and no high-value opportunities appear in this category.

**d) Standard Class Shipping Creates Slow Delivery Experience**  
With an average delivery time of 4.71 days, Standard Class — the most commonly used shipping mode — creates the slowest customer experience. This may be contributing to lower customer satisfaction scores and higher return rates.

---

## 4. What Risks Are Visible

**a) High Discounts Are Creating Losses**  
Orders with discounts above 30% generate an **average loss of ₹1,601 per order**. This is the single most dangerous pattern identified in the data. These loss-making orders are hidden in aggregate figures but are silently reducing overall profitability.

**b) Furniture Has an Alarming Return Rate of 7.67%**  
Furniture items are returned at more than double the rate of Technology products (3.03%). High return rates mean lost revenue, higher logistics costs, and potential customer dissatisfaction. If unchecked, this can significantly damage the brand.

**c) Profit Growth is Slower Than Sales Growth**  
Sales grew by 4.3% but profit only grew by 2.2% from 2024 to 2025. This margin compression is a warning signal. It could mean rising costs, increasing discounts, or a product mix shift toward lower-margin items.

**d) Corporate Segment Has the Lowest Profitability**  
Despite being a significant sales channel, the Corporate segment generates the lowest profit among the three segments. This likely indicates corporate customers are receiving disproportionately large discounts.

---

## 5. What Opportunities Are Visible

**a) Scale Technology — It Drives the Business**  
Since Technology has both the highest sales and the highest profit margins, increasing inventory, marketing, and cross-selling in this category is the highest-ROI opportunity available.

**b) Grow East and West Regions Using South Region Playbook**  
The South region's success can be studied and replicated. By applying similar campaign strategies (Organic, Referral channels), pricing discipline, and customer service models to East and West, the business could grow by 15–20% in those regions.

**c) Upsell Faster Shipping to High-Value Customers**  
Same Day shipping generates the highest average order value (₹60,428). Promoting premium shipping to customers who already spend above a threshold can increase both revenue and customer satisfaction.

**d) Fix Discount Policy to Recover Margin**  
Capping discounts at 25% and introducing a manager approval system for higher discounts could recover significant profit on thousands of orders annually.

---

## 6. Recommended Business Actions

| Priority | Action | Expected Impact |
|----------|--------|----------------|
| 🔴 High | Cap maximum discount at 25%; require approval above this | Recover ₹15–20 Lakh in annual profit |
| 🔴 High | Investigate and fix Furniture return rate (currently 7.67%) | Reduce logistics costs, improve customer satisfaction |
| 🟡 Medium | Replicate South region strategy in East and West regions | Potential 15–20% revenue uplift in those regions |
| 🟡 Medium | Review Furniture pricing and remove unprofitable SKUs | Improve Furniture margin from 6.9% toward 12%+ |
| 🟢 Low | Promote Same Day and First Class shipping for high-value orders | Increase average order value and customer satisfaction |
| 🟢 Low | Bundle Office Supplies with Technology purchases | Increase basket size without major marketing spend |

---

## 7. Limitations of the Dashboard

- The dataset covers only 2024–2025. Longer historical data (3–5 years) would allow more reliable trend detection and seasonal pattern analysis.
- Customer-level data is present but not fully exploited. Repeat purchase rates and customer lifetime value analysis were not included in this dashboard.
- The `customer_rating` column was collected but not prominently featured in the dashboard due to limited contextual metadata about what each rating represents.
- Geographic drill-down is available at state and city level, but city-level analysis was not fully explored due to the large number of unique cities.
- The `campaign_channel` field shows which channel brought the order, but ROI per channel (spend vs revenue) cannot be calculated without marketing spend data.

---

## 8. Suggested Next Analysis

1. **Customer Cohort Analysis** — Track how long each customer stays active, and calculate customer lifetime value by segment.
2. **Product-Level Profitability Analysis** — Identify the top 20 and bottom 20 products by profit margin to guide inventory decisions.
3. **Seasonal Trend Deep Dive** — Analyze month-by-month patterns to identify peak and low seasons for each category and plan promotions accordingly.
4. **Campaign Channel ROI** — Pair campaign channel data with marketing spend data to calculate which acquisition channels deliver the best return.
5. **Return Driver Analysis** — Survey customers who returned Furniture items to understand the top 3 reasons and address root causes directly.

---


