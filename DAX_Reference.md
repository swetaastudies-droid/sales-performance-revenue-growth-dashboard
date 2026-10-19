# Power BI DAX Reference
Create these measures after loading the `Sales_Data` table. Confirm column names in Power BI before pasting.

```DAX
Total Revenue = SUM(Sales_Data[Revenue])

Total Cost = SUM(Sales_Data[Cost])

Total Profit = SUM(Sales_Data[Profit])

Total Units Sold = SUM(Sales_Data[Units Sold])

Total Target Sales = SUM(Sales_Data[Target Sales])

Total Actual Sales = SUM(Sales_Data[Actual Sales])

Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)

Achievement % = DIVIDE([Total Actual Sales], [Total Target Sales], 0)

Target Variance = [Total Actual Sales] - [Total Target Sales]

Previous Month Revenue =
CALCULATE(
    [Total Revenue],
    DATEADD('Calendar'[Date], -1, MONTH)
)

MoM Growth % =
DIVIDE(
    [Total Revenue] - [Previous Month Revenue],
    [Previous Month Revenue]
)

Previous Year Revenue =
CALCULATE(
    [Total Revenue],
    SAMEPERIODLASTYEAR('Calendar'[Date])
)

YoY Growth % =
DIVIDE(
    [Total Revenue] - [Previous Year Revenue],
    [Previous Year Revenue]
)
```

## Calendar table

```DAX
Calendar =
ADDCOLUMNS(
    CALENDAR(MIN(Sales_Data[Date]), MAX(Sales_Data[Date])),
    "Year", YEAR([Date]),
    "Month Number", MONTH([Date]),
    "Month", FORMAT([Date], "MMMM"),
    "Month Year", FORMAT([Date], "MMM yyyy"),
    "Year Month Sort", YEAR([Date]) * 100 + MONTH([Date]),
    "Quarter", "Q" & FORMAT([Date], "Q")
)
```

After creating Calendar:
1. Sort `Calendar[Month Year]` by `Calendar[Year Month Sort]`.
2. Mark `Calendar` as the date table using `Calendar[Date]`.
3. Create an active one-to-many relationship from `Calendar[Date]` to `Sales_Data[Date]`.

## Formatting
- Currency measures: format as INR/currency with appropriate decimal places.
- `Profit Margin %`, `Achievement %`, `MoM Growth %`, and `YoY Growth %`: format as Percentage.
- Do not sum or average the source row-level `Growth %` to represent overall growth.
