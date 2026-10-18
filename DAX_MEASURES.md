# DAX Measures Reference

## Overview

This document explains key DAX measures used for sales performance, profitability, customer analysis, and time-based reporting in the Power BI Sales & Customer Analytics Dashboard.

> Note: Confirm table names, column names, and existing measure definitions in Power BI Desktop before treating these as the exact formulas used in the published report.

## 1. Total Sales

**Purpose:** Calculates total sales revenue.

```dax
Total Sales = 
SUMX(
    'Raw Sales Data',
    'Raw Sales Data'[Quantity]
        * 'Raw Sales Data'[Unit Price]
        * (1 - 'Raw Sales Data'[Discount %])
)
```

## 2. Total Orders

**Purpose:** Counts distinct order identifiers.

```dax
Total Orders =
DISTINCTCOUNT('Raw Sales Data'[Order ID])
```

## 3. Total Quantity Sold

**Purpose:** Calculates the total quantity sold.

```dax
Total Quantity Sold =
SUM('Raw Sales Data'[Quantity])
```

## 4. Total Cost

**Purpose:** Calculates the total cost of sold items.

```dax
Total Cost = 
SUMX(
    'Raw Sales Data',
    'Raw Sales Data'[Quantity]
        * RELATED('Product Master'[Unit Cost])
)
```

## 5. Total Profit

**Purpose:** Calculates profit after deducting costs from sales.

```dax
Total Profit =
[Total Sales] - [Total Cost]
```

## 6. Profit Margin

**Purpose:** Calculates profit as a percentage of sales.

```dax
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)
```

## 7. Average Order Value

**Purpose:** Calculates average sales value per order.

```dax
Average Order Value =
DIVIDE(
    [Total Sales],
    [Total Orders],
    0
)
```

## 8. Total Customers

**Purpose:** Counts distinct customers represented in the sales data.

```dax
Total Customers =
DISTINCTCOUNT('Customer Master'[Customer ID])
```

## 9. Average Sales per Customer

**Purpose:** Calculates average sales per distinct customer.

```dax
Average Sales per Customer =
DIVIDE(
    [Total Sales],
    [Total Customers],
    0
)
```

## 10. Sales Year to Date

**Purpose:** Calculates sales from the beginning of the current year through the selected date.

```dax
Sales YTD =
TOTALYTD(
    [Total Sales],
    'Date Table'[Date]
)
```

## 11. Previous-Year Sales

**Purpose:** Calculates sales for the comparable period in the previous year.

```dax
Previous Year Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Date Table'[Date])
)
```

## 12. Sales Growth Percentage

**Purpose:** Measures the percentage change in sales compared with the previous year.

```dax
Sales Growth % =
DIVIDE(
    [Total Sales] - [Previous Year Sales],
    [Previous Year Sales],
    0
)
```
