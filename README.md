# Coffee Shop Sales Analysis \| Power BI

> An interactive Power BI report for exploring coffee shop sales
> performance across time, product categories, products, and store
> locations.

## 1. Executive Summary

This project uses Power BI to analyze coffee shop sales and present
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

  Source format                       Excel

  Business domain                     Retail / food and beverage sales

  Expected analytical grain           Transaction-level sales records;
                                      verify against the source workbook

  Reporting period                    Not independently verified from the
                                      available project details

  Row count                           Not yet documented

  Currency definition                 Not yet documented; confirm the
                                      source data and report formatting
  -----------------------------------------------------------------------

The report references fields and concepts related to transaction
records, transaction dates, product types, product categories, store
locations, and time-based analysis. Exact column definitions and data
types should be documented after reviewing the source workbook.

## 4. Tools and Technologies

-   **Microsoft Power BI Desktop** --- report development and
    interactive visualizations.
-   **Power Query** --- data import and transformation.
-   **DAX** --- measures and calculated columns.
-   **Excel** --- source data format.
-   **Git and GitHub** --- version control and project documentation.

## 5. Data Cleaning and Transformation

Power Query was used for data preparation. The exact transformation
steps have not yet been documented, so this section intentionally avoids
claiming specific operations such as duplicate removal, null handling,
or type corrections.

For a reproducible portfolio presentation, document the steps that were
actually applied, such as:

-   Checking column names and assigning appropriate data types.
-   Validating date and time fields for time-based analysis.
-   Checking missing values, duplicate records, and inconsistent
    categories.
-   Reviewing numeric sales and quantity fields for invalid values.
-   Confirming that transformed values reconcile with the source data.

> **Before publishing:** Replace or supplement this list with the
> transformations actually performed in Power Query. Do not describe a
> validation step as completed unless you performed it.

## 6. Data Modeling and DAX Calculations

The project uses DAX measures and calculated columns, as confirmed in
the project notes. The report metadata references measures or fields
including **Total Sales**, **Total Orders**, **Total Quantity Sold**,
and month-over-month (MoM) growth/difference calculations.

### KPI and analysis areas

-   **Total Sales** --- overall sales value in the current filter
    context.
-   **Total Orders** --- order count as defined in the report.
-   **Total Quantity Sold** --- total quantity sold.
-   **MoM Sales Growth / Difference** --- month-over-month comparison
    for sales.
-   **MoM Orders Growth / Difference** --- month-over-month comparison
    for orders.
-   **MoM Quantity Growth / Difference** --- month-over-month comparison
    for quantity.
-   **Date, weekday, and hour analysis** --- supports temporal
    comparisons.

The exact DAX expressions and definitions of "order" and
month-over-month growth have not been independently verified. Add the
actual formulas to this section if you want to showcase DAX
implementation in detail.

### Data model note

The project notes describe the model as a single-table model. However,
report metadata references both `Transactions` and `Date Table` names.
Confirm the model view in Power BI Desktop before publishing this claim;
if a separate date table is present, update this section to describe the
actual relationships and model structure.

## 7. Dashboard Screenshots

Screenshots have not yet been added. Capture the report pages in Power
BI Desktop and save the images in the `screenshots/` folder. Then
replace the placeholders below with the corresponding filenames.

### Main sales dashboard

![Coffee Shop Sales dashboard](screenshots/coffee-sales-dashboard.png)

*Add a screenshot of the main dashboard showing the KPI cards, time
trends, and sales breakdowns.*

### Product and category analysis

![Product and category
analysis](screenshots/product-category-analysis.png)

*Add a screenshot that clearly shows product and product-category
comparisons.*

### Time and location analysis

![Sales by time and store
location](screenshots/time-and-location-analysis.png)

*Add a screenshot showing hourly/daily patterns and store-location
performance.*

## 8. Key Insights and Business Recommendations

The following observations are based on the findings provided for this
project. They should be interpreted as descriptive patterns in the
sample data, not proof of causation.

### Findings

1.  **Weekday morning activity:** Sales were observed to peak around
    morning hours on Monday, Tuesday, and Wednesday.
2.  **Within-month pattern:** Sales generally increased from the
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

A quantified business impact, such as increased revenue, reduced waste,
or improved staffing efficiency, has not been measured as part of the
information provided for this project.

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
│   ├── coffee-sales-dashboard.png
│   ├── product-category-analysis.png
│   └── time-and-location-analysis.png
└── data/
    └── README.md
```

The `data/` folder can contain a data dictionary or source attribution
note. Add the original dataset only if its license and sharing terms
permit redistribution. If the dataset cannot be shared, document how it
was obtained and what is required to reproduce the report.

## How to View the Project

1.  Download or clone this repository.
2.  Open `Coffee Shop Sales.pbix` in Microsoft Power BI Desktop.
3.  If Power BI prompts for a data source, update the source path to the
    permitted local Excel file.
4.  Refresh the data if the source file is available and refresh is
    required.
5.  Explore the report visuals and available filters.

The report may not refresh on another machine without the original Excel
source file or a correctly configured data-source path.

## Notes and Limitations

-   This project uses a sample dataset and should not be interpreted as
    a claim about a real coffee shop's current performance.
-   Reported findings depend on the dataset and the active filters used
    in the dashboard.
-   Exact source-data details, transformation steps, DAX formulas, and
    model relationships should be verified and documented before
    treating this README as a complete technical specification.
-   Screenshots are placeholders until actual report captures are
    committed to the repository.

------------------------------------------------------------------------

*Created as a Power BI portfolio project focused on sales analytics and
business intelligence.*
