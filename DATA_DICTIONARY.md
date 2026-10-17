# Data Dictionary

This dictionary describes the four source tables and their known fields. Field names below are based on the project workbook structure. Where a field's exact business definition was not explicitly documented, the description is kept general.

## Raw Sales Data

| Field | Description | Expected type |
|---|---|---|
| Order ID | Transaction/order identifier | Text |
| Order Date | Date of the order | Date |
| Customer ID | Identifier linking to Customer Master | Text |
| Product ID | Identifier linking to Product Master | Text |
| Sales Rep ID | Identifier linking to Sales Rep Master | Text |
| Region | Sales region recorded for the transaction | Text |
| Sales Channel | Channel through which the sale was made | Text |
| Payment Method | Recorded payment method; missing values were replaced with `Unknown` | Text |
| Quantity | Quantity recorded for the order line | Whole number |
| Unit Price | Unit price recorded for the transaction | Decimal number |
| Discount % | Discount percentage; missing values were replaced with `0` | Decimal number |

## Customer Master

| Field | Description | Expected type |
|---|---|---|
| Customer ID | Unique customer identifier used in relationships | Text |
| Customer Name | Customer name | Text |
| Customer Segment | Customer segment classification | Text |
| City | Customer city | Text |
| Region | Customer region | Text |
| Email | Customer email field | Text |
| Customer Status | Status recorded for the customer | Text |

## Product Master

| Field | Description | Expected type |
|---|---|---|
| Product ID | Unique product identifier used in relationships | Text |
| Product Name | Product name | Text |
| Category | Product category | Text |
| Subcategory | Product subcategory | Text |
| Unit Cost | Cost per product unit | Decimal number |
| Unit Price | Listed unit price | Decimal number |
| Supplier | Supplier associated with the product | Text |

## Sales Rep Master

| Field | Description | Expected type |
|---|---|---|
| Sales Rep ID | Sales representative identifier used in relationships | Text |
| Sales Rep Name | Sales representative name | Text |
| Region | Region associated with the sales representative | Text |
| Team | Sales team name or classification | Text |

## Measures

| Measure | Purpose |
|---|---|
| Total Sales | Sales value after applying the transaction discount logic |
| Total Profit | Total Sales less Total Cost |
| Total Orders | Distinct count of Order ID |
| Total Customers | Distinct count of customers in the sales data context |
| Total Quantity Sold | Sum of Quantity |
| Total Cost | Quantity multiplied by the related product unit cost, aggregated over sales rows |
| Total Discount | Sum of discount value calculated from quantity, unit price, and discount percentage |
| Profit Margin | Total Profit divided by Total Sales |
| Average Order Value | Total Sales divided by Total Orders |
| Average Sales per Customer | Total Sales divided by the customer count used by the measure |

**Note:** Measure results respond to report filter context. Descriptions summarize the intended calculations and should be checked against the DAX in the PBIX if the model is changed.
