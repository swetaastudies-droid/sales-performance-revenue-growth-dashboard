# Beginner Workflow Checklist

- [ ] Download/unzip this project folder.
- [ ] Open Power BI Desktop.
- [ ] Get Data > Excel workbook > select `data/Sales_Performance_Revenue_Growth_Dataset.xlsx`.
- [ ] Select only `Sales_Data` for the main report and choose Transform Data.
- [ ] Inspect column names, data types, nulls, and duplicate grain (Date + Sales Executive Name + Product Category).
- [ ] Preserve legitimate blank Growth % values for the first month.
- [ ] Set Date to Date; Year and Units Sold to whole number; monetary columns to decimal/fixed decimal.
- [ ] If source percent fields are percentage points, divide by 100 before percentage formatting.
- [ ] Close & Apply.
- [ ] Create Calendar table and relationship.
- [ ] Add measures from `power_bi/DAX_Reference.md`.
- [ ] Build the four pages using `documentation/Report_Page_Plan.md`.
- [ ] Import `power_bi/Sales_Corporate_Theme.json` from View > Themes > Browse for themes.
- [ ] Validate measures and write insights based on the actual report.
- [ ] Save your `.pbix` file in the `power_bi/` folder.
- [ ] Add screenshots to `screenshots/`.
