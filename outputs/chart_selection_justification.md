# Chart Selection Justification
**Student:** Bishakha Dey | **Student ID:** 2511726 | **Part 4:** Tableau Executive Dashboard & Data Storytelling

---

## Chart 1: Sales Trend Over Time — Line Chart

**1. What question does this chart answer?**  
How are total sales and profit changing month by month and year over year from 2024 to 2025?

**2. Why is the line chart type appropriate?**  
A line chart is the best choice for showing continuous data over time. Sales data has a natural time sequence — each month connects to the next. The line chart allows viewers to immediately see upward or downward trends, peaks, and dips. A bar chart could show individual months but would make the trend harder to see. A pie chart would be completely wrong here because it does not show time.

**3. What fields are used for color, size, label, or filter?**  
- **X-axis (Columns):** Order Date (Month/Year)  
- **Y-axis (Rows):** SUM(Sales) and SUM(Profit) as dual axis  
- **Color:** Two separate marks — one color for Sales, one for Profit (e.g., blue for Sales, green for Profit)  
- **Label:** Values shown at the end of each line  
- **Filter:** Year filter (2024, 2025) applied as an interactive filter

**4. What design principle did I apply?**  
I used a dual-axis line chart to show both Sales and Profit on the same view without cluttering separate sheets. I kept gridlines minimal and used direct labeling instead of a legend wherever possible. Both axes are clearly labeled with currency units.

**5. What mistake did I avoid?**  
I avoided using a bar chart for this time series because bars would imply discrete, independent data points rather than a continuous trend. I also avoided adding too many lines (e.g., by segment or region) on a single trend chart, which would create visual clutter. I kept the view focused on the overall trend.

---

## Chart 2: Regional Performance — Bar Chart

**1. What question does this chart answer?**  
Which geographic region generates the most sales and profit? How do the four regions (North, South, East, West) compare?

**2. Why is the bar chart type appropriate?**  
A bar chart is ideal for comparing discrete categories (in this case, four regions). Each bar has a fixed length that the eye can easily compare against other bars. This makes it instantly clear which region is performing best. A map could also work for geographic data, but since we have only four regions (not individual states), a bar chart delivers a cleaner comparison.

**3. What fields are used for color, size, label, or filter?**  
- **X-axis (Columns):** SUM(Sales)  
- **Y-axis (Rows):** Region  
- **Color:** Region (each region gets a distinct color)  
- **Label:** Sales value shown at the end of each bar  
- **Sort:** Sorted descending by Sales so the top region appears first  
- **Filter:** Customer Segment filter allows drill-down by segment

**4. What design principle did I apply?**  
I sorted bars from highest to lowest sales to immediately direct the viewer's attention to the best-performing region. I used a consistent color palette where each region has a unique but professional color. I kept horizontal bars because region names are text labels — horizontal bars avoid the need to rotate axis labels.

**5. What mistake did I avoid?**  
I avoided using a pie chart, which would make it nearly impossible to accurately compare regions that are close in value (like East and West). I also avoided using a 3D bar chart, which distorts proportions and confuses viewers.

---

## Chart 3: Category Profitability — Horizontal Bar Chart / Treemap

**1. What question does this chart answer?**  
Which product categories and sub-categories generate the most and least profit? Where is the business making money and where is it losing it?

**2. Why is the bar chart / treemap appropriate?**  
For category-level comparison, a horizontal bar chart lets the viewer compare profit values across 3 categories and 13 sub-categories at a glance. A treemap is used for sub-category level to show both size (sales) and color (profit margin) simultaneously, which communicates two dimensions of data in a compact space. This is more information-dense than a simple bar chart while remaining easy to interpret.

**3. What fields are used for color, size, label, or filter?**  
- **Size:** SUM(Sales) — larger boxes represent higher sales  
- **Color:** SUM(Profit) — green for high profit, red for low/negative profit  
- **Label:** Sub-category name and profit value  
- **Filter:** Category filter (Furniture, Office Supplies, Technology)

**4. What design principle did I apply?**  
I used a diverging color scheme (red to green) for profit so that negative profit sub-categories immediately stand out in red without needing to read the numbers. This follows the principle of using color to convey meaning, not just decoration.

**5. What mistake did I avoid?**  
I avoided stacking all sub-categories into a single bar chart, which would have been too crowded with 13 sub-categories. I also avoided using a line chart, which implies a time sequence that does not apply to product categories.

---

## Chart 4: Customer Segment View — Bar Chart with Dual Measure

**1. What question does this chart answer?**  
How do Consumer, Corporate, and Home Office segments compare in total sales, profit, and number of orders?

**2. Why is the bar chart appropriate?**  
With only three segments to compare, a grouped bar chart clearly shows the difference between segments across two measures (Sales and Profit) side by side. The viewer can immediately spot which segment leads and which lags.

**3. What fields are used for color, size, label, or filter?**  
- **X-axis:** Customer Segment  
- **Y-axis:** SUM(Sales) and SUM(Profit)  
- **Color:** Measure (Sales vs Profit) differentiated by color  
- **Label:** Values shown on bars  
- **Filter:** Region and Year filters for cross-segment drill-down

**4. What design principle did I apply?**  
I used a consistent color for the same measure across segments so the viewer's brain does not have to decode multiple meanings. I added reference lines at the average to help viewers see whether each segment is above or below average.

**5. What mistake did I avoid?**  
I avoided using a pie chart for segment comparison because three segments with similar sizes would look nearly equal on a pie chart, making differences nearly invisible. The bar chart makes differences immediately obvious.

---

## Chart 5: Discount vs Profit — Scatter Plot

**1. What question does this chart answer?**  
Is there a relationship between discount percentage and profit? Do higher discounts lead to lower profit?

**2. Why is the scatter plot appropriate?**  
A scatter plot is the only chart type that directly shows the relationship (correlation) between two continuous numeric variables — in this case, Discount (%) and Profit (₹). Each dot represents one order. The trend line overlaid on the scatter plot visually confirms the direction of the relationship.

**3. What fields are used for color, size, label, or filter?**  
- **X-axis:** Discount  
- **Y-axis:** Profit  
- **Color:** Category (Furniture, Office Supplies, Technology) — to see if the discount-profit relationship differs by category  
- **Trend Line:** Linear regression trend line added to show direction  
- **Filter:** Category and Region filters

**4. What design principle did I apply?**  
I added a reference line at Profit = 0 (the break-even line) so the viewer can immediately identify which orders are loss-making. This makes the business risk of high discounts visually undeniable.

**5. What mistake did I avoid?**  
I avoided using a bar chart for this analysis, which would only show averages and hide the spread of individual data points. The scatter plot shows every single order, making outliers and patterns visible. I also avoided using too many colors that would make it hard to identify category-level patterns.

---

## Chart 6: Shipping Performance — Bar Chart

**1. What question does this chart answer?**  
Which shipping mode causes the longest delays? How does each shipping mode affect delivery time and average sales?

**2. Why is the bar chart appropriate?**  
A bar chart clearly compares four discrete shipping modes on average delivery days. Since we are comparing a numeric measure (days) across categories (ship modes), a bar chart is the most natural and readable choice.

**3. What fields are used for color, size, label, or filter?**  
- **X-axis:** Ship Mode  
- **Y-axis:** AVG(Delivery Days)  
- **Color:** Ship Mode  
- **Label:** Average delivery days shown on each bar  
- **Filter:** Region filter to check if shipping delays vary by region

**4. What design principle did I apply?**  
I sorted the bars from fastest to slowest delivery so the viewer can immediately see the spectrum from Same Day to Standard Class. I used a single consistent color family with varying shades to reinforce that these are variations of the same concept (shipping).

**5. What mistake did I avoid?**  
I avoided using a line chart, which would falsely imply that shipping modes exist on a continuum where one flows into another. They are distinct categories, so bars are correct. I also avoided adding unnecessary gridlines or decorative elements that would distract from the message.

---

## Chart 7: Return Analysis — Bar Chart

**1. What question does this chart answer?**  
Which categories and segments have the highest return rates? Where is product return creating the most business risk?

**2. Why is the bar chart appropriate?**  
Return rate is a percentage value compared across discrete categories. A bar chart makes it easy to compare rates side by side and immediately identify the category with the highest return rate (Furniture at 7.67%).

**3. What fields are used for color, size, label, or filter?**  
- **X-axis:** Category (or Sub-Category)  
- **Y-axis:** Return Rate (calculated field: SUM(return_flag) / COUNT(order_id))  
- **Color:** Return flag indicator — red for high return rate categories  
- **Label:** Return rate percentage shown on bars  
- **Filter:** Region and Segment filters

**4. What design principle did I apply?**  
I used red color for high-return categories to signal risk without requiring the viewer to read labels. This follows the principle of using color purposefully to convey business meaning.

**5. What mistake did I avoid?**  
I avoided showing raw return counts instead of return rates, because raw counts would be misleading — a category with more orders would naturally have more returns. Using the return rate (percentage) normalizes for volume and gives a fair comparison.

---

*Chart justifications prepared by Bishakha Dey (Student ID: 2511726) for Masai School Business Analytics Assignment, Part 4.*
