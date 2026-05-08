**1 About the Project**

Project name is Sales Analysis | Amazon Products, built in Microsoft Power BI Desktop (file: Amazon dash.pbix).
There is 1 dashboard page with a black background theme and the Amazon logo placed at the top-left for branding.
It uses 2 data tables — Amazon_Data (all sales records) and a Date table (for time-based calculations).
The dashboard has 4 KPI cards at the top: Total YTD, Total QTD, YTD Products Sold, and YTD Reviews.
There are 4 charts: Sales by Month, Sales by Week, YTD Sales by Product, and Reviews by Product.
Two interactive slicers are available — one for Product Category and one for Quarter (Q1, Q2, Q3, Q4).
8 product categories are covered: Audio Video, Camera, Car Accessories, Laptop, Men Clothes, Men Shoes, Mobile & Accessories, and Toys.

**2 Key Insights**

Laptop in Q4 has the highest sales — $840.21K YTD. Top product: OnePlus Pad 11.61" at $35.0K.
Men Shoes in Q4 generated $325.09K — top products: Cutter & Buck Men's ($2,875), FALKE Men's Shadow ($2,835), Vertx Cutback Mens ($2,666).
Camera in Q4 made $188.38K — led by Nikon Wide Angle ($16.8K), Hasselblad 907X ($14.0K), Sony VPL-XW6000ES ($12.0K).
Men Shoes in Q2 = $142.20K — top: adidas Men's Running ($8.1K), Solid Gear ($5.1K).
Audio Video is the most inconsistent category — Q1 = $4.55K, Q2 = $37.36K, Q3 = $35.60K, Q4 = $38.72K.
Mobile & Accessories has 6.39M YTD reviews but only $39.18K in sales — very high engagement, low price-point products.
Toys peak in Q4 — $30.38K, led by Playmobil Adventure ($1,347) and Brio Disney ($1,065).
Sales by Week chart shows a heavy spike in weeks 40–52 across all categories — clear year-end holiday effect.
Sales by Month chart consistently peaks in the last month of each selected quarter across every category.

**3 Business Problem**

The main problem is inconsistent sales — revenue varies hugely across categories and quarters with no way to see it clearly.
Laptop Q4 earns $840K while Audio Video Q1 earns only $4.55K — this massive gap was invisible without a dashboard.
Q4 always dominates while Q1 and Q2 stay very low — this seasonal imbalance was never clearly seen before.
Some products like Mobile & Accessories get millions of reviews but very little revenue — misleading teams about what's actually profitable.
There was no single place to compare how each category performed quarter by quarter or find the top products quickly.
Without this visibility, teams could not plan inventory, budgets, or marketing campaigns accurately.

**4 Reasons Causing the Problem**

No Date Table was set up — without a date dimension, Power BI cannot calculate YTD or QTD values automatically.
No DAX time-intelligence measures existed — there were no formulas written to sum up sales by year or quarter, so all comparisons had to be done manually.
Raw flat transaction data only — the Amazon_Data table had individual rows with no weekly, monthly, or quarterly grouping, making trend analysis impossible.
No product category filter — products were stored individually with no way to group or slice them by category at a click.
No KPI summary view — teams had no quick-look numbers to spot which category was performing well or poorly at any given time.
Heavy Q4 dependency — most categories rely on holiday season sales, creating huge gaps between quarters that were never reported clearly.

**5 Solution**

A Date Table was created and connected to Amazon_Data — enabling Power BI to understand weeks, months, quarters, and years.
DAX formulas (TOTALYTD, TOTALQTD) were written to automatically calculate total sales for any selected year-to-date or quarter-to-date period.
4 KPI Cards placed at the top — Total YTD, Total QTD, YTD Products Sold, and YTD Reviews — all update live when filters change.
A Product Category Slicer (dropdown) was added — one click on any category instantly filters all 4 cards and all 4 charts together.
A Quarter Slicer (Q1–Q4) was added — allowing easy comparison of any quarter's performance across all categories.
Sales by Month (line chart) — shows whether sales went up or down each month within the selected quarter.
Sales by Week (bar chart) — highlights which weeks had the highest sales, clearly showing the holiday-season spike in weeks 40–52.
Top Products by Sales & by Reviews (horizontal bar charts) — shows the top 5 revenue products and top 5 reviewed products side by side for each filter selection.

**6 Concepts Used**

Data Modeling — Two tables (Amazon_Data + Date) connected with a date key, forming a star schema (fact + dimension table).
DAX Time Intelligence — TOTALYTD() and TOTALQTD() functions used to calculate automatic rolling period totals.
KPI Card Visual — 4 card visuals showing Total YTD, Total QTD, YTD Products Sold, and YTD Reviews as big headline numbers.
Slicers — Product Category (dropdown) and Quarter (Q1–Q4 dropdown) slicers for full interactive filtering.
Line / Area Chart — "Sales by Month" chart to show monthly growth or decline within each selected quarter.
Bar Charts — Clustered bar chart for "Sales by Week" (vertical) and horizontal bars for top product rankings by sales and reviews.
Cross-filtering — All visuals and KPI cards update simultaneously when any slicer is changed — no manual refresh needed.
Drill-through — Drill-through configured with "quarter" as the field (confirmed visible in the Visualizations panel) for deeper product-level analysis.
Dashboard Design — Black background, salmon/pink colored bars, white bold text for KPI values, and Amazon logo image for professional branding.

<img width="1269" height="698" alt="amazon" src="https://github.com/user-attachments/assets/4a6ff4b7-4cb7-4a0d-afc0-48f29113467c" />

