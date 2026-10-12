# Coffee Shop Sales Analysis \| Power BI

> An interactive Power BI report for exploring Coffee Shop Sales
> performance across time, product categories, products, and store
> locations.

## 1. Executive Summary

This project uses Power BI to analyze Coffee Shop Sales and present
business performance through an interactive dashboard. The report is
designed to help store management review key sales KPIs, identify
temporal sales patterns, and compare performance across products,
categories, and locations.

The analysis highlights reported patterns in weekday morning sales and a
rise in sales from the beginning toward the middle of the month,
followed by a decline toward month-end. The report also supports
comparison of monthly sales, orders, and quantities sold.

**Project type:** Business Intelligence / Sales Analytics\
**Primary tool:** Microsoft Power BI\
**Data source:** Excel sample dataset\
**Data preparation:** Power Query\
**Audience:** Store management

## 2. Business Problem and Objectives

Coffee shop managers need a clear view of when sales occur, which
products and categories contribute most to sales, and how performance
differs by store location. Reviewing raw transaction data alone can make
these patterns harder to identify.

### Objectives

-   Monitor overall sales performance using KPI cards.
-   Analyze sales trends over time, including month-level and day-level
    patterns.
-   Compare sales by product and product category.
-   Compare performance across store locations.
-   Explore sales by day of week and hour of day.
-   Present findings in an interactive report that can support
    operational decisions.

## 3. Dataset Overview

The report uses a provided sample dataset imported from Excel.

  -----------------------------------------------------------------------
  Item                                Details
  ----------------------------------- -----------------------------------
  Dataset type                        Sample coffee shop sales data

  Source format                       Excel (.xlsx)

  Business domain                     Coffee Shop Sales

  Currency                            Dollar ($)
  
  -----------------------------------------------------------------------

The dataset was used to analyze sales trends, product performance, order volume, and location-level performance.

## 4. Tools and Technologies

-   **Microsoft Power BI Desktop** --- Report Development and
    Interactive Visualizations.
-   **Power Query** --- Data import and transformation.
-   **DAX** --- Measures and calculated columns.
-   **Excel** --- Source data format.
-   **Git and GitHub** --- Version control and project documentation.

## 5. Data Cleaning and Transformation

Data preparation was performed using Power Query in Power BI.

The transformation process included the following steps, where applicable:

Reviewed column names and data types.
Checked for missing or null values.
Checked for duplicate records.
Verified date and time fields for sales analysis.
Ensured numeric sales and quantity fields were suitable for aggregation.
Prepared the data for product, category, date, time, and store-level analysis.

## 6. Data Modeling and DAX Calculations

The project uses DAX measures and calculated columns, as confirmed in
the project notes. The report metadata references measures or fields
including **Total Sales**, **Total Orders**, **Total Quantity Sold**,
and month-over-month (MoM) growth/difference calculations.

### KPI and analysis areas

-   **Total Sales** --- Overall Sales value in the current filter
    context.
-   **Total Orders** --- Order count as defined in the report.
-   **Total Quantity Sold** --- Total quantity sold.
-   **MoM Sales Growth / Difference** --- Month-over-month comparison
    for sales.
-   **MoM Orders Growth / Difference** --- Month-over-month comparison
    for orders.
-   **MoM Quantity Growth / Difference** --- Month-over-month comparison
    for quantity.
-   **Date, weekday, and hour analysis** --- Supports temporal
    comparisons.

1 MoM Growth & Diff Sales = 
    VAR month_diff = [CM Sales] - [PM Sales]
    VAR mom = ([CM Sales] - [PM Sales]) / [PM Sales]
    VAR _sign = IF(month_diff > 0, "+", "")
    VAR _sign_trend = IF(month_diff > 0,"▲", "▼")
    RETURN
    IF(
    ISBLANK([PM Sales]) || [PM Sales] = 0,
    "No Previous Sales",_sign_trend & " " & _sign & FORMAT(mom, "#0.0%" & " | " & _sign & FORMAT(month_diff/1000, "0.0K")) & " " & "vs LM")

### Data model note

The project has mainly two tables `Transactions` and `Date Table` names. All the columns & DAX calculations are done in `Transactions` table and date related columns are generated in `Date Table`. The transaction date column of `Transactions` table has Many to one (*:1) relationship with Date column of `Date Table`

## 7. Dashboard Screenshots

Screenshots have not yet been added. Capture the report pages in Power
BI Desktop and save the images in the `screenshots/` folder. Then
replace the placeholders below with the corresponding filenames.

### Main Sales Dashboard

![Coffee Shop Sales dashboard](https://github.com/Prajyot-Palimkar/coffee-shop-sales-power-bi/blob/77b3dcd845cb11829a807d4b18c37ebceeee2440/Coffee%20Shop%20Sales%20Dashboard.png)

### Product and Category Analysis

![Product and category
analysis](https://github.com/Prajyot-Palimkar/coffee-shop-sales-power-bi/blob/77b3dcd845cb11829a807d4b18c37ebceeee2440/Product%20and%20category%20analysis.png)

### Daily Hourly Analysis

![Sales by Days - Hours.png](https://github.com/Prajyot-Palimkar/coffee-shop-sales-power-bi/blob/77b3dcd845cb11829a807d4b18c37ebceeee2440/Sales%20by%20Days%20-%20Hours.png)

## 8. Key Insights and Business Recommendations

The following observations are based on the data present on the dashboard.

### Findings

1.  **Weekday Morning activity:** Sales were observed to peak around
    morning hours on Monday, Tuesday, and Wednesday.
2.  **Within-Month pattern:** Sales generally increased from the
    beginning of the month toward the middle, then declined toward the
    end of the month.
3.  **Highest reported month:** June recorded approximately **166K in
    total sales**.
4.  **Reported KPI totals:** The dashboard showed **35,352 total
    orders** and **50,942 units sold** for the selected reporting
    context. Confirm the date/filter context and definitions before
    presenting these as full-period totals.
5.  **Top reported location:** Hell's Kitchen.
6.  **Top reported product:** Barista Espresso.
7.  **Top reported category:** Coffee.

### Recommendations for store management

-   **Plan for morning demand:** Review staffing and preparation levels
    for Monday--Wednesday mornings. Validate the pattern across
    additional periods before making permanent schedule changes.
-   **Align inventory with demand:** Use product-level and
    category-level views to review stock availability for
    high-performing products, especially Barista Espresso and the Coffee
    category.
-   **Investigate month-end softness:** Compare promotions, operating
    days, product availability, and customer traffic across the month to
    understand whether the observed decline is recurring.
-   **Review location performance:** Investigate what contributes to
    Hell's Kitchen's reported leading performance and assess whether
    relevant practices can be applied to other locations.
-   **Track trends consistently:** Monitor monthly sales, order counts,
    and quantities over time to distinguish recurring patterns from
    one-off fluctuations.

These recommendations are potential actions for further investigation;
the dashboard alone does not establish their financial impact.

## 9. Project Outcomes

The report brings multiple views of sales performance into one
interactive Power BI experience. It supports exploration of:

-   Sales KPIs and monthly trends.
-   Daily and hourly sales patterns.
-   Product and product-category performance.
-   Store-location comparisons.
-   Order and quantity metrics alongside sales value.

## 10. Skills Demonstrated

-   Power BI report design and data visualization.
-   KPI reporting and sales performance analysis.
-   Power Query data preparation.
-   DAX measures and calculated columns.
-   Time-based analysis by month, weekday, day, and hour.
-   Product, category, and location comparisons.
-   Translating descriptive findings into practical business
    recommendations.
-   Technical documentation using GitHub-compatible Markdown.

## Repository Structure

A suggested structure for this repository is:

``` text
coffee-shop-sales-power-bi/
├── README.md
├── Coffee Shop Sales.pbix
├── screenshots/
│   ├── Coffee Shop Sales Dashboard.png
│   ├── Product and category analysis.png
│   └── Sales by Days - Hours.png
└── LICENSE                 # Optional
```

## Notes and Limitations

-   This project uses a sample dataset and should not be interpreted as
    a claim about a real coffee shop's current performance.
-   Reported findings depend on the dataset and the active filters used
    in the dashboard.
-   Exact source-data details, transformation steps, DAX formulas, and
    model relationships are present in Power BI file.
-   Screenshots are placeholders until actual report captures are
    committed to the repository.
