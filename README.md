# bishakhadey_2511726_part4_tableau_dashboard
# Part 4: Tableau Executive Dashboard & Data Storytelling

**Student Name:** Bishakha Dey  
**Student ID:** 2511726  
**Repository:** bishakhadey_2511726_part4_tableau_dashboard  

---

## 1. Business Problem Summary

A retail leadership team needs an executive dashboard to monitor and make decisions on:
- Sales performance trends over time
- Regional and geographic performance
- Product category and sub-category profitability
- Customer segment behavior
- Shipping and delivery performance
- Discount impact on profit
- Return patterns and risk areas

The goal is to build a Tableau dashboard that tells a clear business story — not just a collection of charts — and helps leadership identify **business opportunities and risks** quickly.

---

## 2. Dataset Description

| Field | Description |
|-------|-------------|
| **File Name** | `dashboard_sales_data.xlsx` |
| **Total Records** | 4,200 orders |
| **Time Period** | January 2024 – December 2025 |
| **Location** | `data/dashboard_sales_data.xlsx` |

**Key Columns:**

| Column | Type | Description |
|--------|------|-------------|
| order_id | Text | Unique order identifier |
| order_date | Date | Date the order was placed |
| ship_date | Date | Date the order was shipped |
| customer_id | Text | Unique customer identifier |
| customer_segment | Categorical | Consumer, Corporate, Home Office |
| region | Categorical | North, South, East, West |
| state | Categorical | Indian state name |
| city | Categorical | City name |
| category | Categorical | Furniture, Office Supplies, Technology |
| sub_category | Categorical | 13 sub-categories |
| product_name | Text | Product name |
| ship_mode | Categorical | Same Day, First Class, Second Class, Standard Class |
| sales | Numeric | Order sales value (₹) |
| quantity | Numeric | Number of units ordered |
| discount | Numeric | Discount applied (0 to 1 scale) |
| profit | Numeric | Order profit (₹), can be negative |
| return_flag | Binary | 1 = returned, 0 = not returned |
| delivery_days | Numeric | Days from order to ship |
| customer_rating | Numeric | Customer satisfaction rating (1–5) |
| campaign_channel | Categorical | Organic, Social, Paid, Email, Referral |

---

## 3. Tableau Workbook Description

**File:** `tableau/executive_dashboard.twbx`  
**Type:** Tableau Packaged Workbook (includes embedded data)

The workbook contains:
- 7 individual analysis sheets (views)
- 1 executive dashboard combining key views with filters and interactions
- 5 calculated fields created in Tableau

**Sheets in Workbook:**
1. Sales Trend View — Line chart showing monthly sales and profit over time
2. Regional Performance View — Bar chart comparing regions by sales and profit
3. Category Profitability View — bar chart for category and sub-category profit
4. Customer Segment View — Bar chart comparing segments by sales, profit, and orders
5. Shipping Performance View — Bar chart showing delivery days and sales by ship mode
6. Discount vs Profit View — Scatter plot showing relationship between discount and profit
7. Return Analysis View — Bar chart showing return rate by category and segment

---

## 4. Calculated Fields Created in Tableau

| Calculated Field | Formula | Purpose |
|-----------------|---------|---------|
| **Profit Margin** | `SUM([Profit]) / SUM([Sales])` | Shows what % of sales becomes profit |
| **Cost** | `SUM([Sales]) - SUM([Profit])` | Estimates cost of goods/operations |
| **Average Order Value** | `SUM([Sales]) / COUNTD([Order ID])` | Average revenue per unique order |
| **Return Rate** | `SUM([Return Flag]) / COUNT([Order ID])` | % of orders that were returned |
| **Shipping Delay Bucket** | `IF [Delivery Days] = 0 THEN "Same Day" ELSEIF [Delivery Days] <= 2 THEN "Fast (1-2 days)" ELSEIF [Delivery Days] <= 4 THEN "Standard (3-4 days)" ELSE "Slow (5+ days)" END` | Groups delivery speed into meaningful business buckets |

---

## 5. Dashboard Components

The Executive Dashboard (`executive_dashboard.twbx`) includes:

**Charts/Views Included:**
1. Sales Trend Line Chart (monthly, 2024–2025)
2. Regional Performance Bar Chart
3. Category Profitability Bar Chart
4. Customer Segment Comparison Bar Chart
5. Discount vs Profit Scatter Plot (with trend line and reference line at profit = 0)

**KPI Summary Cards (at the top of dashboard):**
- Total Sales: ₹21.70 Crore
- Total Profit: ₹3.33 Crore
- Overall Profit Margin: 15.3%
- Total Orders: 4,200
- Return Rate: 4.55%

**Interactive Filters Applied:**
- Region (North, South, East, West)
- Category (Furniture, Office Supplies, Technology)
- Customer Segment (Consumer, Corporate, Home Office)
- Order Date Range (Year / Quarter)
- Ship Mode
- Campaign Channel

**Dashboard Layout:**
- Title bar at top with KPI cards
- Sales trend line across the full width
- Regional and Category charts side by side in the middle
- Segment and Discount charts at the bottom
- All filters on a side panel (right)

---

## 6. Filters and Interactions Used

| Filter | Type | Applied To |
|--------|------|-----------|
| Region | Dropdown | All sheets |
| Category | Multi-select | All sheets |
| Customer Segment | Multi-select | All sheets |
| Order Date | Date range slider | Sales Trend, all views |
| Ship Mode | Multi-select | Shipping view, dashboard |
| Campaign Channel | Dropdown | Sales trend, segment view |

**Actions Used:**
- Click on a region bar → filters all other charts to show only that region's data
- Click on a category → filters all charts to show only that category
- Hover tooltip on scatter plot → shows Order ID, Discount %, Profit, Category

---

## 7. Key Business Insights

1. **Sales grew 4.3% YoY** (₹10.62 Cr in 2024 → ₹11.08 Cr in 2025) but profit growth was slower at 2.2%, indicating margin compression.
2. **South region leads** with ₹6.47 Cr sales and ₹99.88 Lakh profit — the strongest geographic market.
3. **Technology dominates profit** — 84% of total profit comes from Technology (18.2% margin vs Furniture's 6.9%).
4. **Discounts above 30% create losses** — average profit turns negative (–₹1,601/order) at that level.
5. **Furniture returns are alarming** — 7.67% return rate vs Technology's 3.03%, raising quality and cost concerns.
6. **Home Office segment is most profitable** despite three segments being close in total sales.
7. **Standard Class shipping is slow** (4.71 days avg) — Same Day generates highest avg order value (₹60,428).
8. **Copiers, Accessories, and Phones** are the three most profitable sub-categories.

*(Full details in `outputs/business_insights.md`)*

---

## 8. Dashboard Story Summary

The dashboard tells this narrative:
> "Our business is growing — South is our strongest region and Technology is our profit engine. However, deep discounts and Furniture's low margins are holding back overall profitability. If leadership addresses the discount cap issue and improves East/West regional performance, we could see 15–20% growth in profit within the next fiscal year."

*(Full story in `outputs/dashboard_story.md`)*

---

## 9. Assumptions Made

- `order_date` was stored as serial numbers in Excel; converted to proper date format in Tableau using date parsing.
- `return_flag` values are binary (0 = not returned, 1 = returned). Return rate was calculated as SUM(return_flag) / COUNT(orders).
- `delivery_days` is calculated as the difference between `ship_date` and `order_date`. Orders with 0 delivery days are assumed to be Same Day delivery.
- `discount` column is on a 0–1 scale (e.g., 0.25 = 25% discount), not 0–100.
- All monetary values (sales, profit) are in Indian Rupees (₹).
- The dataset was used as-is without any data cleaning modifications, as instructed. Only Tableau-level calculated fields were added.

---

## 10. Known Limitations

- Dashboard does not calculate marketing ROI because campaign spend data is not available in the dataset.
- Customer-level lifetime value analysis was not included due to scope of the assignment.
- City-level geographic breakdown was available but not included in the executive dashboard to keep it clean and executive-appropriate.
- Customer rating column was not prominently featured as rating scale context was not available.
- Only 2 years of data is available — seasonal patterns over a longer period (3–5 years) would provide more reliable trend insights.

---

## Screenshots

All dashboard screenshots are available in the `screenshots/` folder:

| File | Shows |
|------|-------|
| `screenshots/full_dashboard.png` | Complete executive dashboard |
| `screenshots/sales_trend_view.png` | Sales trend line chart |
| `screenshots/regional_performance_view.png` | Regional performance bar chart |
| `screenshots/category_profitability_view.png` | Category profitability bar chart |
| `screenshots/filter_interaction_view.png` | Dashboard with filters applied (interaction evidence) |

---

## Repository Structure

```
bishakhadey_2511726_part4_tableau_dashboard/
├── data/
│   └── dashboard_sales_data.xlsx
├── tableau/
│   └── executive_dashboard.twbx
├── outputs/
│   ├── dashboard_story.md
│   ├── business_insights.md
│   └── chart_selection_justification.md
├── screenshots/
│   ├── full_dashboard.png
│   ├── sales_trend_view.png
│   ├── regional_performance_view.png
│   ├── category_profitability_view.png
│   └── filter_interaction_view.png
└── README.md
```
Note: Github automatically sorts the files alphabetically.
---


