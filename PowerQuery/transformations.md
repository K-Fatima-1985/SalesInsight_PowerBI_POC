# Power Query – Data Preparation

## Purpose

Power Query is used to prepare source data before it reaches the Power BI data model.

## Recommended Transformation Checklist

1. Load the source data.
2. Inspect column names and data types.
3. Set numeric fields to appropriate numeric data types.
4. Set date fields to Date/DateTime.
5. Trim and clean text fields.
6. Check for null/blank values.
7. Check for duplicate records.
8. Standardize category/market names.
9. Remove unnecessary columns.
10. Rename columns clearly.
11. Apply transformations in a logical order.
12. Close & Apply and validate the model.

## Example M Pattern

```powerquery
let
    Source = Excel.Workbook(File.Contents("source.xlsx"), null, true),
    SalesTable = Source{[Item="Sales",Kind="Table"]}[Data],
    ChangedTypes = Table.TransformColumnTypes(
        SalesTable,
        {
            {"Quantity", Int64.Type},
            {"Unit_Price", type number},
            {"Order_Date", type date}
        }
    ),
    CleanText = Table.TransformColumns(
        ChangedTypes,
        {
            {"Product", Text.Trim, type text},
            {"Market", Text.Trim, type text}
        }
    )
in
    CleanText
```

> Replace the source/table/column names with the actual names in your model.

## Data Quality Checks

Before publishing a report, verify:

- No unexpected duplicate transactions.
- No invalid dates.
- Numeric columns are numeric.
- Revenue calculations reconcile with the source.
- Blank categories are investigated.
- Slicers filter all relevant visuals.
- KPI totals match detailed tables.

## Power Query Skills

- Data type management
- Text cleaning
- Null handling
- Duplicate checking
- Column transformation
- Data validation
- Query organization
