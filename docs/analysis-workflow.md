# Analysis Workflow

This document records the workflow used to prepare the Bike Buyers workbook and build its PivotTables and dashboard.

## 1. Workbook Setup

1. Keep the original `bike_buyers` data in its own worksheet.
2. Create a `Working Sheet`, a `Pivot Tables` worksheet, and a `Dashboard` worksheet.
3. Copy the raw data into the working sheet before cleaning it.

## 2. Data Cleaning & Preparation

1. Select the working data and enable Excel filters.
2. Use **Data → Remove Duplicates** to remove duplicate records.
3. Use **Find & Replace** to standardize the Marital Status and Gender labels.
4. Review filtered values for misspellings and error values.
5. Add an `Age Brackets` column.
6. Categorize each customer's age with this nested `IF` formula (shown for row 2):

   ```excel
   =IF(L2<35,"Young",IF(L2<60,"Middle-Aged","Old"))
   ```

   - Below 35: `Young`
   - 35 to 59: `Middle-Aged`
   - 60 and above: `Old`

7. Review the cleaned data again before creating the PivotTables.

## 3. PivotTables & Charts

Create the PivotTables using the cleaned data in `Working Sheet`.

### Analysis 1 — Average Income by Gender

- **Rows:** Gender
- **Columns:** Purchased Bike
- **Values:** Income, summarized by Average
- **Chart:** Clustered Column Chart
- **Chart elements:** Axes, axis titles, chart title, data table, gridlines, and legend

### Analysis 2 — Commute Distance

- **Rows:** Commute Distance
- **Columns:** Purchased Bike
- **Values:** Commute Distance, summarized as a count
- **Sort order:** Apply a custom order when needed: `0-1 Miles`, `1-2 Miles`, `2-5 Miles`, `5-10 Miles`, `10+ Miles`
- **Chart:** Line with Markers Chart
- **Chart elements:** Axes, axis titles, chart title, gridlines, and legend

### Analysis 3 — Age Brackets

- **Rows:** Age Brackets
- **Columns:** Purchased Bike
- **Values:** Purchased Bike, summarized as a count
- **Sort order:** `Young`, `Middle-Aged`, `Old`
- **Chart:** Line Chart
- **Chart elements:** Axes, axis titles, chart title, gridlines, and legend

Adjust chart styles and formatting for readability.

## 4. Dashboard

1. Copy the three PivotCharts to the `Dashboard` worksheet.
2. Add a dashboard title.
3. Insert a slicer and connect it to the relevant PivotTables/PivotCharts using **Report Connections** (or **PivotTable Connections**, depending on the Excel version).
4. Arrange the slicer and charts into a clear layout beneath the title.

## 5. Review

Before sharing the workbook, check that:

- The cleaned data and age-bracket formula cover all records.
- The PivotTables use the cleaned working data.
- The commute-distance and age-bracket categories appear in the intended custom order.
- The slicer filters all intended dashboard charts.
- Chart titles, labels, and number formats are clear and consistent.
