## 📊 Accounting Reports Dashboard
This project presents a comprehensive financial overview through two interactive Power BI pages:

> Balance Sheet
> Income Statement

## 1. 🛠️ SQL Treatments
All data transformations and aggregations prior to loading into Power BI were handled via SQL, including:

Standardization of date formats and creation of date dimension (DimDate)

Categorization of GL accounts into Assets, Liabilities, Revenues, Expenses, etc.

Pre-calculated account balances by period for both the Balance Sheet and Income Statement

Currency adjustments and FX treatments (if applicable)

Historical calculations for YoY and vertical/horizontal analysis

Cleaning and standardizing naming conventions across financial accounts

## 2. 🔄 Power BI Treatments – ETL & Data Modeling
ETL (Extract, Transform, Load):
All SQL outputs were imported using Power Query (M language).

Applied transformations:

Removal of null values

Change of data types

Filtering of fiscal years

Merge operations for enhanced context (e.g., Account Descriptions, Departments)

Data Model:
Star schema format

Key relationships:

FactBalances ↔ DimDate

FactBalances ↔ DimAccount

FactBalances ↔ DimDepartment

Proper use of surrogate keys and indexing to improve performance and slicer usability

## 3. 📐 DAX Measures
Calculated measures include (not exhaustive):

YoY Growth %: ([Current Year] - [Previous Year]) / [Previous Year]

Vertical Analysis %: Account Amount / Total Revenue (Income Statement) or Account Amount / Total Assets (Balance Sheet)

Operating Profit, Gross Margin, Depreciation Breakdown

Cumulative Measures and Rolling 12-Month Averages

Dynamic titles and KPI cards for enhanced interactivity

## 4. 🎨 Layout & Design (via Figma)
Designed wireframes and color palette in Figma

Focused on clean, corporate-friendly layout:

Two pages with consistent headers, navigation buttons, and card summaries

Use of blue and grey tones for professionalism

Icons and tooltips added for better UX

Exported assets and implemented them directly into Power BI

## 5. 📈 Business Analysis Report
# 5.1 Balance Sheet
Asset Growth: Total assets increased 16.82% YoY, mainly driven by a 29.83% increase in Property, Plant and Equipment. This signals significant investment in fixed assets.

Liabilities: Increased moderately, particularly in Salary and Other Payables, which require closer tracking to avoid short-term liquidity issues.

# 5.2 Income Statement
Operating Profit: Although we saw an 11.52% YoY increase, its vertical contribution decreased by 8.15%, indicating reduced lucrativity.

Revenue & Cost:

Net Sales grew 21.41%, but Cost of Sales grew 27.29%, shrinking the gross margin.

Operating Expenses: Increased 23.73%, which is aligned with revenue growth and within expectations.

Depreciation: Significant increase of 55.09% YoY and 27.73% in vertical analysis, driven by investments in fixed assets.

Discounts: A positive highlight — decreased 46.25% YoY and 55.73% vertically, boosting net sales.

⚠️ Key Takeaways:
Review Cost of Sales drivers to improve margins.

Reassess CapEx strategy to ensure fixed asset investments are necessary and productive.

Keep monitoring the balance between Operating Expenses and Revenue Growth to protect profitability.
