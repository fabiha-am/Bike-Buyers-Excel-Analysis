# Bike Buyers Analysis | Excel Dashboard

An end-to-end **Microsoft Excel data analysis project** exploring customer demographics, income, commuting habits, and bike-purchasing behaviour. The workbook combines data cleaning, calculated categories, PivotTables, charts, and an interactive dashboard with a slicer.

## Project Overview

The goal of this project is to explore which customer groups are more likely to purchase a bike and how purchasing behaviour varies across income, age, and commute distance.

The workbook contains an original dataset and a cleaned analysis sheet. The cleaned dataset contains **1,000 customer records** after duplicate removal and data preparation.

## Workbook Contents

| Worksheet | Description |
|---|---|
| `bike_buyers` | Original bike buyers dataset. |
| `Working Sheet` | Prepared dataset with standardized Marital Status and Gender values, duplicate removal, and an `Age Brackets` category. |
| `Pivot Tables` | Three PivotTables and their supporting charts. |
| `Dashboard` | Consolidated dashboard with charts and an interactive slicer. |

## Analysis & Key Findings

The project focuses on three comparisons:

1. **Average income by gender and bike-purchase status** — compares the average income of customers who purchased a bike with those who did not.
2. **Bike purchases by commute distance** — compares purchase counts across five commute-distance groups.
3. **Bike purchases by age bracket** — compares purchase counts across Young, Middle-Aged, and Old customer groups.

Selected observations from the cleaned 1,000-record worksheet:

- **Overall:** 481 customers (48.1%) purchased a bike.
- **Age:** the Middle-Aged group has the highest purchase rate at **52.8%** (351 of 665 customers), followed by Young at 42.3% and Old at 32.2%.
- **Commute distance:** the 2–5 Miles group has the highest purchase rate at **58.6%** (95 of 162 customers). The 10+ Miles group has the lowest at 29.7%.
- **Income:** average income is higher among bike purchasers than non-purchasers for both female and male customers in this dataset.

These are descriptive findings from this dataset; they do not establish that age, commute distance, or income causes a customer to purchase a bike.

## Data Preparation

The working sheet was prepared using Excel tools and formulas:

- Applied filters to inspect the dataset.
- Removed duplicate records.
- Standardized Marital Status and Gender labels using Find & Replace.
- Checked categorical fields for spelling inconsistencies and error values.
- Added an `Age Brackets` column using a nested `IF` formula.

The age groups are defined as:

| Age condition | Age Bracket |
|---|---|
| Age below 35 | Young |
| Age from 35 to 59 | Middle-Aged |
| Age 60 or above | Old |

Formula used in the working sheet (for row 2):

```excel
=IF(L2<35,"Young",IF(L2<60,"Middle-Aged","Old"))
```

## Excel Features Used

- Sort and Filter
- Remove Duplicates
- Find & Replace
- Nested `IF` formula
- PivotTables and custom sorting
- Clustered Column Chart
- Line Chart and Line with Markers Chart
- Dashboard layout and Slicer

## Getting Started

1. Download or clone this repository.
2. Open `Bike_Buyers_Analysis.xlsx` in Microsoft Excel.
3. Open the `Dashboard` worksheet to explore the charts.
4. Use the slicer to interact with the dashboard. You can also inspect the `Working Sheet` and `Pivot Tables` worksheets to follow the analysis.

For the detailed step-by-step workflow, see [`docs/analysis-workflow.md`](docs/analysis-workflow.md).

## Repository Structure

```text
bike-buyers-excel-analysis/
├── README.md
├── Bike_Buyers_Analysis.xlsx
├── .gitignore
└── docs/
    └── analysis-workflow.md
```

## Dataset & Attribution

The workbook includes the original `bike_buyers` worksheet as well as the cleaned working data. The dataset's original source and usage license were not included in the project materials. **Before making this repository public, verify that you have permission to redistribute the dataset.** If required, add the original dataset's source and license information here, or publish a version of the workbook that does not redistribute the raw data.

## Project Notes

This repository documents an Excel-based analysis. The calculations and visualizations are contained in the `.xlsx` workbook; no separate Python or SQL analysis is included.
