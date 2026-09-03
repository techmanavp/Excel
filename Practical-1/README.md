# 📊 Excel Fundamentals Booster

<div align="center">

![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

**A hands-on practice workbook covering essential Excel formulas & functions — from lookups and conditional logic to date math and text manipulation.**

</div>

---

## 📌 Overview

This project is a self-contained Excel practical built to strengthen core spreadsheet skills used every day in data analysis, reporting, and business operations. It uses three realistic mini-datasets — **student marks**, **sales transactions**, and **employee records** — and applies a broad range of formulas to solve practical problems on each one.

> 🎯 **Goal:** Practice and demonstrate fluency in Excel's most important formula families: logical, lookup/reference, aggregation, date, and text functions.

---

## 🗂️ Workbook Structure

| # | Sheet Name | Dataset | Rows |
|---|---|---|---|
| 1 | `Student Marks` | Student exam scores across 3 subjects | 20 students |
| 2 | `Sales Data` | Regional sales transactions | 20 records |
| 3 | `Sheet3` | Employee HR records | 20 employees |

---

## 🧠 Skills & Functions Demonstrated

### 1️⃣ Student Marks

| Task | Formula Used |
|---|---|
| Calculate average score across subjects | `AVERAGE` |
| Assign a letter grade (A/B/C) based on average | Nested `IF` |
| Flag students scoring above 80 in two subjects | `IF` + `AND` |
| Count students scoring above 50 in Maths | `COUNTIFS` |
| Average English score for students scoring above 60 | `AVERAGEIFS` |
| Look up a result by student ID (with error handling) | `VLOOKUP` + `IFERROR` |
| Dynamically sum a range from a text reference | `INDIRECT` |
| Extract rows matching a condition | `FILTER` |

### 2️⃣ Sales Data

| Task | Formula Used |
|---|---|
| Determine discount eligibility (high amount OR East region) | `IF` + `OR` |
| Calculate years since sale date | `DATEDIF` |
| Find the sales amount for a given salesperson | `INDEX` + `MATCH` |
| Sum sales for a specific region & product | `SUMIFS` |
| Look up sale price by Sales ID (with error handling) | `VLOOKUP` + `IFERROR` |
| Locate the position of an item in a list | `XMATCH` |
| Offset a reference to pull a related value | `OFFSET` |
| Modern flexible lookup with a "not found" fallback | `XLOOKUP` |

### 3️⃣ Employee Records (Sheet3)

| Task | Formula Used |
|---|---|
| Calculate tenure in days from joining date | `DATEDIF` + `MIN`/`MAX` |
| Retrieve employee name & department by ID | `INDEX` + `MATCH` |
| Extract the department code (first 4 characters) | `LEFT` |
| Find the position of a space in a name | `FIND` |
| Convert text to uppercase / lowercase | `UPPER` / `LOWER` |
| Flexible salary lookup by Employee ID | `XLOOKUP` |
| Round, round up, and round down numeric values | `ROUND`, `CEILING`, `FLOOR` |

---

## 🙋 Author

**Manav Patel**
📧 manavpatel.tech@gmail.com
🔗 [GitHub](https://github.com/techmanavp) 
