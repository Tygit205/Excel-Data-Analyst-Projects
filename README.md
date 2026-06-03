# Project 5 — Excel Capstone: Q1 2026 Board Performance Report

## Scenario
The CEO needed a full Q1 2026 business performance report 
ready for a board presentation. Raw data was pulled from 
3 internal systems — messy, incomplete, and spread across 
multiple tables. I cleaned it, enriched it using XLOOKUP, 
built calculated columns, and delivered a board-ready report.

## Dataset
- 80 transactions across January, February and March 2026
- 10 sales reps across 4 branches
- 12 products across 3 categories
- Q1 total revenue: R499,030

## What I Did

### 1. Data Cleaning (10 issues resolved)
- Removed duplicate transactions
- Standardised Branch, Region and Status columns
- Fixed mixed date formats
- Removed extra spaces using TRIM()
- Flagged missing customer names
- Replaced N/A and TBC in revenue column
- Corrected 4 wrong revenue calculations
- Flagged negative quantities (returns)
- Added Revenue Check column (Qty × Unit Price)
- Wrapped formulas in IFERROR()

### 2. XLOOKUP (2 reference tables)
- Pulled Rep Name, Branch, Region and Commission Rate 
  from Staff Table using EmpID
- Pulled Product Name, Category and Cost Price 
  from Product Catalogue using ProductID
- Used absolute references ($) throughout to prevent 
  range drift

### 3. Calculated Columns
- Revenue Check = Quantity × Unit Price
- Profit = Total Revenue − Cost Price
- Profit Margin % = Profit ÷ Total Revenue
- Commission Earned = Total Revenue × Commission Rate
- Performance Flag = IF(Revenue > R20,000, "Star", "Standard")

### 4. PivotTables & Report
- Revenue by Branch
- Revenue by Product Category  
- Top Sales Reps by Revenue
- Monthly Revenue Trend (Jan–Mar)
- Executive Summary for board presentation
- Investigation log for 9 flagged transactions

## Key Findings
| Metric | Result |
|---|---|
| Total Q1 Revenue | R499,030 |
| Best Branch | Sandton Branch (R171,720) |
| Top Sales Rep | Kefilwe Sithole (R90,300) |
| Best Category | Electronics (69% of revenue) |
| Total Profit | R335,345 |
| Avg Profit Margin | 67.2% |
| Feb → Mar Change | -35.9% (flagged for review) |

## Skills Applied
XLOOKUP · Data Cleaning · IF Statements · IFERROR · 
Calculated Columns · PivotTables · Charts · 
Board Reporting · Data Validation

## Tools Used
Microsoft Excel

# Project 4 — Data Cleaning: Monthly Orders Report

## Scenario
The operations team dumped a month's worth of raw customer 
orders from three different systems into one spreadsheet. 
The data was messy, inconsistent, and unusable. My job was 
to clean it and deliver a summary report to the manager.

## Dataset
- 50 rows of raw transaction data
- 6 sales reps across 4 regions (Gauteng, KZN, Western Cape, Limpopo)
- 8 products across 3 categories

## Problems Found & Fixed
| # | Issue | Fix Applied |
|---|---|---|
| 1 | Duplicate order (ORD001 appeared twice) | Removed Duplicates |
| 2 | Inconsistent region names (gauteng/GAUTENG/Gauteng) | Find & Replace + TRIM() |
| 3 | Inconsistent status casing (completed/COMPLETED) | Find & Replace + PROPER() |
| 4 | Mixed date formats (2026-04-01 vs 01/04/2026) | Text to Columns |
| 5 | Trailing spaces in customer names and regions | TRIM() |
| 6 | Missing customer names (3 rows) | Flagged for investigation |
| 7 | Text in revenue column (N/A, TBC) | Replaced with correct values |
| 8 | Wrong revenue calculations (2 rows) | Corrected using Revenue Check formula |
| 9 | Negative quantities (returns) | Flagged for manager sign-off |
| 10 | Missing revenue verification | Added Revenue Check column =Qty*UnitPrice |

## Skills Applied
- Data Cleaning: TRIM(), PROPER(), Find & Replace
- Remove Duplicates
- Text to Columns (date format fix)
- IFERROR() for broken formulas
- Revenue verification formula
- PivotTables (Revenue by Region, Category, Top Products)
- Manager summary report with investigation flags

## Key Findings
- Total verified revenue: R237,660
- Top region: Gauteng (R66,630)
- Top category: Electronics (R176,700)
- 9 orders flagged for investigation

## Tools Used
Microsoft Excel

# Excel Data Analyst Projects

A collection of Excel projects built while learning data analysis.
Each project simulates a real workplace scenario.


## Project 3 — Regional Sales Analysis

Scenario: Sales manager requested a full monthly report
for the directors showing regional performance, category
breakdown and top sales reps.

Skills used:
- XLOOKUP across multiple reference tables
- Calculated columns (Qty × Unit Price)
- PivotTables (Revenue by Region, Category, Rep)
- Charts (Bar & Pie)

Tools: Microsoft Excel


## Project 2 — Sales Commission Tracker

Scenario: HR needed a commission report matching
transactions to reps and calculating earnings.

Skills used: XLOOKUP, Commission formulas, PivotTables


## Project 1 — Product Revenue Lookup

Scenario: First XLOOKUP project matching product IDs
to prices and calculating revenue.

Skills used: XLOOKUP, Basic formulas, PivotTables
