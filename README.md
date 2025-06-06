## 📊 Accounting Reports Dashboard
This project presents a comprehensive financial overview through two interactive Power BI pages:

● Balance Sheet ![Image](https://github.com/user-attachments/assets/6fab2bec-fed7-4cd4-afa1-f98d677e5a12)
--
● Income Statement ![Image](https://github.com/user-attachments/assets/c4d41eed-08d9-419a-8dec-9e9b2259bd58)

## 1. 🛠️ SQL Treatments
All data transformations and aggregations prior to loading into Power BI were handled via SQL, including:

Standardization of date formats and creation of date dimension (DimDate) -  [DimCalendar](https://github.com/Angelo-77/AccountingReports/blob/main/DimCalendar)

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

# Data Model:
# Star schema format:
> 📷 ![Image](https://github.com/user-attachments/assets/2e746b22-9e78-4dc2-8450-77fa6476caec)

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

# Measures divided in folders: 
> 📷 ![Image](https://github.com/user-attachments/assets/d1c21b73-0bba-4f3a-a1fa-3fd55a286d75)
________

> 🛠 To see some measures you can click in this folder [DaxMeasures](https://github.com/Angelo-77/AccountingReports/blob/3abb17219ab13573b99813746d97a9f4bb0beeb8/DaxMeasures)

## 4. 🎨 Layout & Design (via Figma)
Designed wireframes and color palette in Figma

Focused on clean, corporate-friendly layout:

Two pages with consistent headers, navigation buttons, and card summaries

Use of blue and grey tones for professionalism

Icons and tooltips added for better UX

Exported assets and implemented them directly into Power BI

> ![Image](https://github.com/user-attachments/assets/5a4ccefa-74ad-43b3-8201-d5974a3a9602)


## 5. 📈 Business Analysis Report
# 5.1 Balance Sheet
Asset Growth: Total assets increased 16.82% YoY, mainly driven by a 29.83% increase in Property, Plant and Equipment. This signals significant investment in fixed assets.

Liabilities: Increased moderately, particularly in Salary and Other Payables, which require closer tracking to avoid short-term liquidity issues.

# 5.2 Income Statement
Operating Profit: Although we saw an 11.52% YoY increase, its vertical contribution decreased by 8.15%, indicating reduced lucrativity.

Revenue & Cost: Net Sales grew 21.41%, but Cost of Sales grew 27.29%, shrinking the gross margin.

Operating Expenses: Increased 23.73%, which is aligned with revenue growth and within expectations.

Depreciation: Significant increase of 55.09% YoY and 27.73% in vertical analysis, driven by investments in fixed assets.

Discounts: A positive highlight — decreased 46.25% YoY and 55.73% vertically, boosting net sales.

## ⚠️ Key Takeaways:
Review Cost of Sales drivers to improve margins.


## 🔗 Dashboard Access  
📊[Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNmQ0ZDRjZWQtOTA1My00YjgzLWE4ZDItZDhmNGJmZmYyN2FmIiwidCI6IjA1Y2JhZTNmLTc3YTAtNGVlMS05NGUzLTM5M2VhNWY1NmMwNyJ9)


## 👤 About Me

I’m a results-driven **Data Analyst and Business Intelligence professional** with a strong foundation in **Power BI, SQL, Excel (including VBA), and KPI Management**. With experience spanning engineering, tax, and commercial sectors, I bring a unique blend of technical expertise and business strategy to every project I take on.

My career journey includes working at industry-leading companies like **Deloitte** and **Ambev**, where I automated processes, built dashboards, and translated complex data into meaningful insights. At **Deloitte**, I specialized in **Direct and Indirect Tax**, developing critical control workpapers and delivering the firm’s **first Power BI dashboard for Direct Taxes**. At **Ambev**, part of **AB InBev** (the world’s largest brewery), I created automated controls and VBA tools to evaluate sales and product performance.

Most recently, at **Draft Solutions**, an engineering consulting firm, I served as a **Senior Planning Analyst**. I managed engineering contracts, developed dashboards to monitor project KPIs, and designed macros for revenue forecasting and goal tracking. I also conducted **CAPEX calculations for Conceptual Engineering Projects**.

I hold a degree in **Accounting from PUC Minas**—recognized as the **largest Catholic university in the world**. While there, I received an academic award for developing a VBA tool to analyze the J150 block of the ECD, representing a company’s **Income Statement structure**.

I’m passionate about creating powerful BI solutions that improve decision-making, automate workflows, and drive measurable results.

**🔧 Technical Skills**:  
Power BI | SQL | Excel | VBA | ETL | Business Intelligence | KPI Development  

---
