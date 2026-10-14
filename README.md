# Walmart Business Dashboard (Excel)

Executive sales summary and interactive dashboard for Walmart's commercial team, built in Excel from ~96K weekly sales records across 45 stores, to guide budget and inventory decisions.

## Business Objective

The commercial team needed to decide where to adjust budget and inventory. The analysis answers two questions:

- Which stores make the most of their floor space? (sales per square meter)
- Which departments contribute most to total sales, and which are below their potential? (department share)

## Dashboard Preview

![Walmart Dashboard](dashboard.png)

## Key Findings

- **The most space-efficient stores are consistent over time.** In 2012, stores 10, 23 and 3 led sales per square meter (top 25%, $575.48/m²) and generated 13.48% of total sales. Stores 10 and 23 were also in the top group in 2010, so their efficiency is not a one-off.
- **Sales are concentrated in three departments.** Pantry & Staples, Fresh Food and Household & Paper generated 36.46% of 2012 sales.
- **Three departments are clearly underperforming.** Toys & Games; Office, School & Crafts; and Garden & Outdoor together contributed only 6.79% of 2012 sales.

## Recommendations

1. Prioritize inventory and budget for stores 10, 23 and 3, and study their practices as a reference for other stores and for expansion decisions.
2. Increase inventory and promotional investment in the three leading departments.
3. For the three underperforming departments, test bundles and promotions, and review slow-moving items that could be replaced with trending products.

## Data Quality Checks

Before building the KPIs, the data was validated:

- **27 negative weekly sales values**: flagged as possible chargebacks or pipeline errors, to be confirmed with the data owner.
- **1 department code without a name** (dept 16): reassigned to "uncategorized" so it does not distort the other departments.
- **No zero store sizes and no nulls** in the fields used for the KPI divisions.

## KPIs

- **Sales per square meter** = total weekly sales / store size. Higher means more efficient use of floor space.
- **Department share** = department sales / total sales.

## Approach

1. Joined weekly sales with the store and department lookup tables into a single clean sheet.
2. Standardized week formats and department names.
3. Ran the data quality checks above.
4. Built the KPIs with pivot tables.
5. Built an interactive dashboard with a department drop-down and charts ranked from highest to lowest.
6. Wrote the executive summary using Context → Finding → Implication.

## Tools

Excel: pivot tables, lookup tables, data validation, dashboard design

## Project Files

- [`walmart_sales_executive_summary.xlsx`](walmart_sales_executive_summary.xlsx): raw and clean data, pivot tables, dashboard and executive summary
- [`dashboard.png`](dashboard.png): dashboard screenshot
