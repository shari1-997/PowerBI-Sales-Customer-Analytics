# Project Documentation

## Project Title
**Sales & Customer Analytics Dashboard — Power BI**

## Objective
Build an interactive report that brings together sales performance, profitability, product performance, customer-segment insights, and regional analysis.

## Workflow
1. Load the Excel workbook into Power BI Desktop.
2. Transform and clean the source tables in Power Query.
3. Set appropriate data types.
4. Remove exact duplicate transaction records.
5. Standardize text fields and handle missing values.
6. Create relationships between the transaction table and master tables.
7. Create DAX measures for sales, profit, orders, customers, quantity, margin, and average order value.
8. Build four report pages.
9. Add slicers and verify that report interactions work.
10. Export the report to PDF and capture page screenshots.

## Source Tables
- **Raw Sales Data:** transaction-level sales records.
- **Customer Master:** customer identifiers and customer attributes.
- **Product Master:** product identifiers, categories, prices, and costs.
- **Sales Rep Master:** sales representative identifiers and attributes.

## Power Query Preparation
The documented preparation steps included:
- Promoting headers in tables where required.
- Removing automatic type-conversion steps when they interfered with mixed source values.
- Applying Trim/Clean to text fields.
- Standardizing categorical text capitalization.
- Removing exact duplicate rows from the sales table.
- Converting mixed date representations into a consistent date field.
- Replacing missing payment methods with `Unknown`.
- Replacing missing discount percentages with `0`.
- Assigning text, date, whole-number, and decimal data types as appropriate.

## Data Model
The model contains three active one-to-many relationships:
- `Customer Master[Customer ID]` → `Raw Sales Data[Customer ID]`
- `Product Master[Product ID]` → `Raw Sales Data[Product ID]`
- `Sales Rep Master[Sales Rep ID]` → `Raw Sales Data[Sales Rep ID]`

The master tables filter the sales transaction table.

## Core Measures
The report includes measures for:
- Total Sales
- Total Profit
- Total Orders
- Total Customers
- Total Quantity Sold
- Total Cost
- Total Discount
- Profit Margin
- Average Order Value
- Average Sales per Customer

Additional time-intelligence measures were also present in the model, including sales year-to-date, previous-year sales, and sales growth percentage.

## Report Pages
### Executive Overview
KPI cards, monthly sales trend, sales by region, category, and channel, plus category and region slicers.

### Product Performance & Profitability
Sales by product, quantity sold by category, profit by category, and product/category slicers.

### Customer Insights & Segment Analysis
Sales by customer segment, customer count, average sales per customer, top customers, and region slicer.

### Regional Sales & Profitability Analysis
Sales by region, regional sales contribution, profit by region, and sales by channel.

## Validation Performed
- User confirmed that core calculations were working.
- User confirmed that slicers worked across report pages.
- The saved report was exported to PDF for visual review.
- The PDF contains four report pages.

## Current KPI Snapshot
- Total Sales: **$19.01M**
- Total Profit: **$5.55M**
- Total Orders: **8K**
- Total Customers: **600**
- Profit Margin: **29.18%**
- Average Order Value: **$2.38K**

KPI values can vary when filters are applied. Rounded display values are used here.

## Limitations
- The PDF export is static and does not retain interactive slicer behavior.
- The PBIX file is required to inspect or modify the data model and report.
- Treat the dataset as sample portfolio data.
