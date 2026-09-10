# DAX Measures – Sales Insight Dashboard

This document records the main analytical measures used/recommended for the Sales Insight Dashboard.

> **Important:** DAX below is a documentation/template layer. If your PBIX uses different table or column names, keep the measure names from your actual model and document the exact formulas from Power BI.

## Core Measures

### Revenue

```DAX
Revenue =
SUMX(
    Sales,
    Sales[Quantity] * Sales[Unit_Price]
)
```

### Sales Quantity

```DAX
Sales Qty =
SUM(Sales[Quantity])
```

### Profit

If the source contains a profit column:

```DAX
Total Profit =
SUM(Sales[Profit])
```

### Profit Margin %

```DAX
Profit Margin % =
DIVIDE(
    [Total Profit],
    [Revenue],
    0
)
```

### Revenue Contribution %

```DAX
Revenue Contribution % =
DIVIDE(
    [Revenue],
    CALCULATE(
        [Revenue],
        ALL(Sales[Market])
    ),
    0
)
```

### Previous Year Revenue

With a proper Date table:

```DAX
Revenue LY =
CALCULATE(
    [Revenue],
    SAMEPERIODLASTYEAR('Date'[Date])
)
```

### Year-over-Year Revenue Growth %

```DAX
Revenue YoY % =
DIVIDE(
    [Revenue] - [Revenue LY],
    [Revenue LY],
    0
)
```

## Top-N Analysis

Top 5 customers/products can be created using Power BI's Top N filter or a ranking measure.

Example:

```DAX
Customer Rank =
RANKX(
    ALL(Sales[Customer]),
    [Revenue],
    ,
    DESC,
    DENSE
)
```

## Formatting Recommendations

- Revenue: currency/number format with thousands separators.
- Sales Qty: whole number.
- Profit Margin %: percentage with 1–2 decimal places.
- Contribution %: percentage with 1–2 decimal places.
- YoY %: percentage with 1–2 decimal places.

## DAX Skills Demonstrated

- `SUM`
- `SUMX`
- `CALCULATE`
- `DIVIDE`
- `ALL`
- `SAMEPERIODLASTYEAR`
- `RANKX`
- Time-intelligence concepts
- KPI calculations
- Contribution analysis
