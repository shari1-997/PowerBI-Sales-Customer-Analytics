# Sales & Customer Analytics Dashboard — Power BI

An end-to-end Power BI portfolio project exploring sales performance, profitability, product performance, customer segments, and regional results. The report combines Power Query data preparation, a relational data model, DAX measures, and interactive report pages.

## Dashboard Preview

![Power BI Executive Overview](Dashboard_Screenshots/Executive%20Overview.png)

The exported PDF contains all four report pages:
- Executive Overview
- Product Performance & Profitability
- Customer Insights & Segment Analysis
- Regional Sales & Profitability Analysis

Open `Sales Customer Analytics Dashboard.pdf` locally to review the full report. Individual page screenshots can be found in `Dashboard_Screenshots/`.

## Key Performance Indicators

Values shown in the exported report:
- **Total Sales:** $19.01M
- **Total Profit:** $5.55M
- **Total Orders:** 8K
- **Total Customers:** 600
- **Profit Margin:** 29.18%
- **Average Order Value:** $2.38K

These figures reflect the report's current saved state and may change when report filters are applied.

## Report Pages

### 1. Executive Overview
Summarizes sales, profit, orders, customers, profit margin, and average order value. Includes a monthly sales trend and breakdowns by region, category, and sales channel. Category and region slicers support interactive exploration.

### 2. Product Performance & Profitability
Compares product sales, quantity sold by category, and profit by category. Product and category slicers allow users to narrow the analysis.

### 3. Customer Insights & Segment Analysis
Explores sales by customer segment, customer count, average sales per customer, and top customers by sales. A region slicer supports regional customer analysis.

### 4. Regional Sales & Profitability Analysis
Compares sales and profit by region, regional contribution to sales, and sales by channel.

## Data Model & Preparation

The project uses four source tables:
- `Raw Sales Data`
- `Customer Master`
- `Product Master`
- `Sales Rep Master`

Power Query preparation included promoting headers where needed, trimming and cleaning text, standardizing categorical values, removing duplicate transaction rows, handling missing payment methods and discounts, parsing mixed date formats, and setting appropriate data types.

The model uses customer, product, and sales-representative master tables related to the sales transaction table through their respective IDs.

## Tools & Skills Demonstrated

- Microsoft Power BI Desktop
- Power Query data cleaning and transformation
- Data modeling and table relationships
- DAX measures and KPI calculations
- Interactive report pages and slicers
- Sales, customer, product, and regional analysis
- Business-focused data visualization

## Project Files

Recommended repository contents:
- `Sales Customer Analytics Dashboard.pbix` — editable Power BI report
- `PowerBI_Sales_Customer_Analytics_Raw_Data.xlsx` — source workbook
- `Sales Customer Analytics Dashboard.pdf` — four-page report export
- `Dashboard_Screenshots/` — individual report-page images
- `PROJECT_DOCUMENTATION.md`
- `DATA_DICTIONARY.md`
- `DATA_QUALITY.md`
- `BUSINESS_INSIGHTS.md`

## Important Notes

This is a portfolio demonstration built from a prepared dataset. Treat customer names and other records as sample data, not verified real-world business information. The PDF is a static export; use the PBIX file to explore interactive behavior.

## Author

Created as a Power BI portfolio project demonstrating data preparation, modeling, DAX, KPI reporting, and interactive analytics.
