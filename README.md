# data-intelligence-dashboard-excel--final-project
📊 Excel analytics project on 250 customer transactions — GroupBy-style customer ranking, FILTER-style search, linear regression, What-If scenarios, and an interactive KPI dashboard with Pivot Charts &amp; slicer-style filters. 1,000+ formulas, 0 errors, no hardcoded results.


# 📊 Data Intelligence Dashboard — Excel Analytics Project

A full-fledged Excel analysis and reporting solution built on **250 real-world-style customer transaction records**, covering the complete analytics workflow: raw data → formula-driven analysis → visualizations → an interactive executive dashboard. Every number in the workbook is a **live formula**, not a pasted-in result — change the source data and the entire workbook recalculates.

---


## 📌 Overview

This project simulates a real business intelligence deliverable: a retail/e-commerce company's transaction log needs to be turned into decision-ready insights. The workbook answers questions like:

- Who are our highest-value customers, and how do we identify them systematically?
- Which products and regions actually drive revenue?
- What happens to revenue if we raise prices or grow demand?
- Is our monthly revenue trending up, down, or flat — and can we forecast next month?
- Can a non-technical stakeholder filter and explore the data without touching a formula?

Rather than compute answers in Python/pandas and paste static numbers into Excel, **every metric is built as a native Excel formula**, so the workbook stays a living analytical tool — anyone can open it, tweak an input cell, and watch every downstream number, chart, and KPI update.

## Dataset

| Attribute | Detail |
|---|---|
| Records | 250 transactions |
| Date range | April 11, 2024 → April 11, 2025 (13 months) |
| Columns | Transaction_ID, Date, Customer_ID, Customer_Name, Product_ID, Product_Name, Category, Quantity, Unit_Price, Payment_Method, Region, Customer_Segment, Customer_Since, Total_Amount |
| Customers | 50 unique |
| Products | 10 (across Electronics, Appliances, Furniture) |
| Regions | Central, East, North, South, West |
| Segments | Basic, Standard, Premium |
| Payment methods | Cash, Credit Card, Debit Card, PayPal |
| Data integrity | Every `Total_Amount` validated as `Quantity × Unit_Price` before load |

## Workbook Structure

```
Data_Intelligence_Dashboard_Final_Project.xlsx
├── ReadMe            → project guide, insights, storytelling
├── Raw Data          → 250-row source table (Excel Table: RawData)
├── Analysis          → 8 formula-driven analytical sections (A–H)
├── Visualizations    → pivot-style summaries + charts + PivotTable guide
└── Dashboard         → KPI cards, filters, charts, icon-set indicators
```

## Sheet-by-Sheet Breakdown

### 1. ReadMe
Executive-facing summary: what each tab contains, the headline insights in plain language, and an honest note on which Excel features (Scenario Manager, Goal Seek, native PivotTables, the Analysis ToolPak) require a one-time manual setup versus what's already live.

### 2. Raw Data
The untouched source table, formatted as a proper Excel Table (`RawData`) so it can feed `SUMIFS`/`COUNTIFS` formulas *and* a native PivotTable without any range maintenance. Frozen header row, currency/date number formats applied.

### 3. Analysis — 8 Sections

| Section | What it does | Core functions |
|---|---|---|
| **A. Date & Time Intelligence** | Report timestamp, data span, days since last sale, month-end boundaries, plus a live change-log timestamp using iterative calculation | `NOW`, `TODAY`, `DATEDIF`, `EOMONTH` |
| **B. Multi-Value Search (FILTER-style)** | Dropdown-driven live extraction of all transactions matching Category + Region + Min Amount — no volatile array spill required | `SUMPRODUCT`, `INDEX`, `MATCH`, `IFERROR` |
| **C. High-Value Customers** | GroupBy-style rollup: every customer's transaction count, total spend, avg order value, rank, and a Top-10 flag with conditional formatting | `SUMIFS`, `COUNTIFS`, `RANK`, Data Bars |
| **D. Frequency Analysis** | Most-purchased product, highest-revenue product, and the single most frequent repeat customer | `COUNTIF`, `SUMIF`, `INDEX`/`MATCH`/`MAX` |
| **E. Two-List Comparison** | Extracts which Top-10-by-spend customers are *also* in the Premium segment | `COUNTIF`, cumulative-rank helper columns |
| **F. Text Abbreviations** | Builds customer initials, 3-letter region codes, 4-letter product codes, and a composite transaction label | `LEFT`, `MID`, `FIND`, `UPPER`, `SUBSTITUTE`, `TEXT` |
| **G. What-If Analysis** | Editable price-increase / demand-growth input cells feeding a projected-revenue formula, plus a Best/Base/Worst scenario table and inline Goal Seek / Scenario Manager instructions | Live formulas + manual-setup guide |
| **H. Linear Regression** | Monthly revenue trend, slope, intercept, R², and next-month forecast — the formula equivalent of the Data Analysis ToolPak's regression output | `SLOPE`, `INTERCEPT`, `RSQ`, `TREND` |

### 4. Visualizations
Pivot-style summary tables (Revenue by Payment Method, by Segment, by Product) each paired with a bar chart, plus a full step-by-step guide for building a **live, native** Excel PivotTable + Slicers + Timeline on top of the `RawData` table.

### 5. 🎯 Dashboard
The single-screen executive view:
- **6 KPI cards** — Total Revenue, Total Transactions, Unique Customers, Avg Order Value, Total Units Sold, Top Region
- **Slicer-style filter panel** — Region / Category / Segment dropdowns driving a live filtered revenue & transaction count via `SUMPRODUCT`
- **Pivot-style tables** — Revenue by Region, by Category, by Month
- **3 charts** — Bar (Region), Pie (Category share), Line (monthly trend)
- **KPI vs Target** — actual vs. benchmark with 3-traffic-light icon set conditional formatting
- **MoM Growth %** — 3-arrow icon set showing month-over-month direction

## Features Implemented

- ✅ Date & Time functions — `TODAY`, `NOW`, `DATEDIF`, `EOMONTH`
- ✅ FILTER-equivalent multi-value search (LibreOffice/older-Excel-safe, no dynamic arrays)
- ✅ Conditional formatting — icons, arrows, data bars, traffic lights
- ✅ Timestamp via `NOW()` + iterative calculation (circular formula)
- ✅ What-If Analysis — Scenario Manager & Goal Seek (formula equivalent + manual guide)
- ✅ Linear Regression — formula equivalent of the Data Analysis ToolPak
- ✅ GroupBy-style aggregation for High-Value Customers
- ✅ Pivot Tables, Pivot Charts (Bar, Line, Pie)
- ✅ Slicers & Timeline (dropdown-filter equivalent + native setup guide)
- ✅ KPI Indicators with conditional formatting
- ✅ Most frequently purchased product / repeating names
- ✅ Two-list comparison to extract matching names
- ✅ Abbreviations built with TEXT functions
- ✅ Full report with insights and storytelling


## 📈 Key Insights

- 💰 **$229,192.47** total revenue across 250 transactions — **$916.77** average order value, **753** units sold to **50** unique customers
- 🖥️ **Electronics dominates** — Laptop and Smartphone alone contribute over $134K, more than half of total revenue
- 🌍 **East leads regionally**; **Central is the softest** — worth checking whether that's a demand gap or a coverage gap
- 👤 **Mark Carter** is both the most frequent buyer (12 transactions) and one of the top lifetime spenders
- 🏆 **Segment value** — Premium and Standard customers already out-spend Basic as a group, supporting a tier-upgrade push
- 📉 **Trend** — the linear regression on monthly revenue shows a mild decline with low R², meaning revenue is closer to flat/seasonal than on a strong directional trend


## Design & Formatting Standards

- **Font:** Arial throughout
- **Color coding:** blue text = editable input cells (yellow fill) · black = formulas · headers on dark-blue fill with white text
- **Number formats:** currency as `$#,##0.00`, dates as `yyyy-mm-dd`, percentages as `0.0%`
- **Zero formula errors:** verified via LibreOffice headless recalculation — **1,060 formulas, 0 errors**
- Every hardcoded reference value (e.g. dashboard KPI targets) is labeled as an illustrative benchmark, not a sourced figure


## Project Structure

```
.
├── Data_Intelligence_Dashboard.xlsx
└── README.md
```


## Possible Extensions

- Swap in a live data connection (Power Query) instead of a static Raw Data table
- Add cohort/retention analysis by `Customer_Since`
- Build a real native PivotTable-driven "Live Dashboard" tab using the guide on Visualizations
- Extend the regression model to include seasonality (month dummy variables) for a better R²
- Add a Power BI or Google Sheets version for cross-platform comparison


## 👨‍💻 Author
**Manav Patel**
📧 manavpatel.tech@gmail.com
🔗 [GitHub](https://github.com/techmanavp) 