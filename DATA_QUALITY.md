# Data Quality & Preparation

## Known Source Issues

The project source was prepared with the following intended data-quality issues:
- Exact duplicate transaction records.
- Missing payment methods.
- Missing discount percentages.
- Inconsistent capitalization in region values.
- Mixed date formats.

The source workbook also contains customer, product, and sales-representative master tables for the model.

## Actions Applied in Power Query

| Issue / preparation need | Action |
|---|---|
| Header rows stored as first-row values in some tables | Promoted first row to headers where required |
| Inconsistent spaces or non-printing characters in text | Applied Trim/Clean to relevant text fields |
| Inconsistent categorical capitalization | Standardized text capitalization for categorical fields |
| Duplicate transaction rows | Removed exact duplicates from Raw Sales Data |
| Mixed date representations | Created a consistently parsed Order Date field and set it to Date type |
| Missing Payment Method | Replaced with `Unknown` |
| Missing Discount % | Replaced with `0` |
| Inconsistent data types | Set identifiers and categorical fields to Text, Order Date to Date, Quantity to Whole Number, and numeric price/discount fields to Decimal Number |

## Data Model Checks

The model contains active one-to-many relationships from:
- Customer Master to Raw Sales Data by Customer ID.
- Product Master to Raw Sales Data by Product ID.
- Sales Rep Master to Raw Sales Data by Sales Rep ID.

## Validation Notes

The project owner confirmed that calculations were working and that slicers interacted across report pages. The report was exported to PDF for visual review.

## Important Caveats

- Replacing a missing discount with `0` assumes no discount was recorded for that transaction; it does not prove that no discount was actually applied.
- Replacing a missing payment method with `Unknown` preserves the record without inventing a value.
- Removing exact duplicates is appropriate for the intentional duplicate rows in this practice dataset. In a live business dataset, duplicate-looking transactions should be investigated before deletion.
- This document records the steps known to have been applied; it does not claim that every possible data-quality issue has been ruled out.
