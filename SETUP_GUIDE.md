# Power BI Dashboard Setup Guide

## Overview

This guide explains how to download, open, configure, and explore the Power BI Sales & Customer Analytics Dashboard.

## Requirements

- Microsoft Power BI Desktop
- `Sales Customer Analytics Dashboard.pbix`
- `PowerBI_Sales_Customer_Analytics_Raw_Data.xlsx`

## 1. Download the Project

Open the GitHub repository:

[PowerBI Sales & Customer Analytics](https://github.com/shari1-997/PowerBI-Sales-Customer-Analytics)

Download the repository using GitHub's download options, or clone it using Git.

## 2. Locate the Project Files

Locate these two files in the downloaded project folder:

- `Sales Customer Analytics Dashboard.pbix` — the Power BI report.
- `PowerBI_Sales_Customer_Analytics_Raw_Data.xlsx` — the source Excel workbook.

Keep the files together in the same project folder to make source-file management easier.

## 3. Open the Dashboard

1. Install and open Microsoft Power BI Desktop.
2. Open `Sales Customer Analytics Dashboard.pbix`.
3. If Power BI displays a data-source warning, follow the prompts to locate the source workbook.
4. Once the report loads, explore its pages, visuals, KPI cards, and slicers.

## 4. Configure the Data Source

The report may use a file path from the computer on which it was originally created.

If Power BI cannot locate the Excel workbook:

1. Open the PBIX file in Power BI Desktop.
2. Select **Transform data** to open Power Query Editor, if needed.
3. Locate the Excel source in the relevant query's Source step or open **Data source settings**.
4. Update the file path to the downloaded `PowerBI_Sales_Customer_Analytics_Raw_Data.xlsx` workbook.
5. Confirm the changes and select **Close & Apply** when appropriate.

The exact steps may vary depending on the existing Power Query configuration and Power BI Desktop version.

## 5. Refresh the Data

1. Confirm that the source workbook is available at the configured path.
2. Select **Refresh** in Power BI Desktop.
3. Wait for the refresh to finish.
4. Resolve any data-source, data-type, or transformation errors.
5. Check that the report visuals and KPI cards display the expected results.

## 6. Explore the Report Pages

The dashboard contains four report pages:

1. **Executive Overview** — high-level sales and profitability KPIs.
2. **Product Performance & Profitability** — product and category performance.
3. **Customer Insights & Segment Analysis** — customer and segment analysis.
4. **Regional Sales & Profitability Analysis** — regional sales and profitability comparisons.

Use the available slicers and visual interactions to explore different perspectives of the data.

## 7. Troubleshooting

### Source workbook not found

Update the source path to the location of the downloaded Excel workbook.

### Refresh errors

Check the source path, column names, data types, and Power Query transformation steps.

### Blank or unexpected visuals

Check the report filters, relationships, DAX measures, and source data. Confirm that the refresh completed successfully.

### KPI values differ from the documented results

Confirm that you are using the intended source data and that no unintended filters or data changes affect the results.

## Project Notes

- Keep a backup of the original source workbook before making changes.
- Renaming or removing required source columns may break Power Query steps and DAX measures.
- Validate KPI values after changing the source data or calculations.
- This project is designed to demonstrate data preparation, data modeling, DAX calculations, interactive reporting, and business analysis using Power BI.

## Project Repository

[View the Power BI Sales & Customer Analytics project on GitHub](https://github.com/shari1-997/PowerBI-Sales-Customer-Analytics)
