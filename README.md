# Sales Performance & Revenue Growth Dashboard

An interactive **Microsoft Power BI** project for analyzing sales performance, revenue growth, profitability, regional performance, and sales target achievement.

## Project Overview

This project transforms sales data into an interactive business intelligence dashboard. It helps users monitor key performance indicators (KPIs), compare sales across regions and product categories, evaluate sales targets, and identify opportunities for business growth.

## Objective

The main objectives of this project are to:

- Track total revenue, profit, units sold, and profit margin.
- Compare revenue and profitability across regions and product categories.
- Evaluate actual sales against sales targets.
- Analyze monthly revenue and profit trends.
- Compare sales channel performance.
- Identify areas where sales performance and profitability can be improved.

## Tools Used

- **Microsoft Power BI Desktop** — Dashboard development and visualization.
- **Power Query** — Data cleaning and transformation.
- **DAX (Data Analysis Expressions)** — Measures and business calculations.
- **Data Modeling** — Calendar table and relationships.
- **GitHub** — Project documentation and version control.

## Dataset Description

The project uses a synthetic sales dataset containing monthly sales records across sales executives, product categories, regions, and sales channels.

The dataset includes fields relating to:

- Date and time period
- Region
- Product category and product
- Sales executive
- Sales channel
- Revenue and cost
- Profit and units sold
- Actual sales and target sales

The dataset is intended for learning and portfolio demonstration. It does not represent verified transactions from a real company.

**Currency note:** The report currently displays amounts using the `$` symbol. A currency symbol change in Power BI does not convert the underlying values into USD. Confirm the source currency or convert the data before publishing financial figures as US dollars.

## Power Query Steps

The data preparation process included:

1. Imported the sales dataset into Power BI Desktop.
2. Inspected column names and data types.
3. Checked for blank values and data quality issues.
4. Verified date, numeric, and categorical column types.
5. Reviewed the dataset for consistency before creating visuals.
6. Loaded the cleaned data into the Power BI data model.

## Data Modeling

A separate Calendar table was created to support time-based analysis.

The Calendar table was related to the sales data using the date field. Month-Year sorting was configured to display months in chronological order.

## DAX Measures

The dashboard includes measures for core business KPIs and time-based comparisons.

| Measure | Purpose |
|---|---|
| Total Revenue | Calculates total revenue |
| Total Cost | Calculates total cost |
| Total Profit | Calculates total profit |
| Total Units Sold | Calculates units sold |
| Total Target Sales | Calculates total sales target |
| Total Actual Sales | Calculates actual sales |
| Profit Margin Measure % | Calculates profit as a percentage of revenue |
| Achievement Measure % | Measures actual sales against target sales |
| Target Variance | Calculates actual sales minus target sales |
| Previous Month Revenue | Retrieves revenue for the previous month |
| MoM Growth % | Calculates month-over-month revenue growth |
| Previous Year Revenue | Retrieves revenue for the comparable previous-year period |
| YoY Growth % | Calculates year-over-year revenue growth |

## Dashboard Features

### 1. Executive Sales Overview
- KPI cards for revenue, profit, units sold, profit margin, target achievement, and growth.
- Monthly revenue trend.
- Revenue comparison by region.
- Interactive slicers for region, product category, sales channel, sales executive, and month.

### 2. Regional & Product Performance
- Revenue comparison across regions.
- Profit comparison across product categories.
- Regional performance matrix.
- Filters for exploring regional and product performance.

### 3. Revenue Growth Analysis
- Monthly revenue trend.
- Monthly profit trend.
- Month-over-month and year-over-year growth indicators.
- Date and category filters for time-based analysis.

### 4. Sales Target & Performance
- Actual sales versus target sales.
- Sales target achievement KPI.
- Target variance KPI.
- Regional target performance comparison.

*The page descriptions above represent the planned report structure. Publish screenshots only for pages and visuals completed in your final `.pbix` file.*

## Key Business Insights

The dashboard supports the following business observations based on the current dataset:

- **Regional performance:** South is the leading revenue region, closely followed by West. East is the lowest-revenue region among the four regions.
- **Product profitability:** Office Supplies contributes the highest total profit among the product categories.
- **Target achievement:** Overall sales achievement is approximately 102.35%, indicating that actual sales exceed the combined target.
- **Sales trends:** Monthly revenue and profit trends help identify peaks, declines, and changes in performance over time.
- **Sales channels:** Online generates more revenue than Offline in the current dataset.
- **Growth opportunities:** The business can investigate lower-revenue regions, improve lower-profit product categories, and use target achievement and monthly trends to guide sales strategies.

These insights describe the supplied dataset and should not be interpreted as findings about a real business.

## Screenshots

Dashboard screenshots will be added here to demonstrate the report's layout, KPIs, charts, and interactive analysis.

### Executive Sales Overview
![Executive Sales Overview](screenshots/executive-sales-overview.png)

### Regional & Product Performance
![Regional & Product Performance](screenshots/regional-product-performance.png)

### Revenue Growth Analysis
![Revenue Growth Analysis](screenshots/revenue-growth-analysis.png)

### Sales Target & Performance
![Sales Target & Performance](screenshots/sales-target-performance.png)

> Replace the image paths above with the exact filenames of the screenshots you upload. Remove any image entry for a page that is not yet completed.

## How to Use This Project

1. Download or clone this repository.
2. Open `Sales_Performance_Revenue_Growth.pbix` using Microsoft Power BI Desktop.
3. If Power BI requests a data source, point it to the dataset included in the `data` folder.
4. Refresh the data if required.
5. Explore the report pages and use the slicers to filter the analysis.

## Conclusion

This project demonstrates practical skills in data preparation, data modeling, DAX calculations, KPI monitoring, and interactive Power BI dashboard design. It shows how sales data can be transformed into useful insights for evaluating business performance and identifying opportunities for improvement.

## Author

K B SWETAA
