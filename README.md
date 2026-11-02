# Adidas Sales & Revenue Performance Analysis

An interactive **Power BI sales analytics dashboard** exploring Adidas sales performance across 2020–2021. The report brings together headline KPIs, monthly revenue trends, regional contribution, retailer performance, product-level sales and operating profit, and sales-channel mix.

![Adidas Sales & Revenue Performance Dashboard](assets/Adidas-Sales-Analysis-Dashboard.png)


## Project Overview

This project uses Microsoft Power BI to turn Adidas sales records into an interactive business intelligence report. It is designed to help users explore where revenue is generated, which products and retailers contribute most, how sales are distributed across regions and channels, and how revenue changes over time.

The report covers the 2020–2021 reporting period and contains interactive filters for year, region, and sales method.

## Business Objectives

1. Monitor overall revenue, operating profit, units sold, and operating margin.
2. Understand monthly revenue movement across the reporting period.
3. Compare revenue contribution across regions.
4. Identify leading product categories by sales and operating profit.
5. Compare retailer-level revenue performance.
6. Understand the contribution of in-store, outlet, and online sales.
7. Provide an interactive report that supports further business questions.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Microsoft Power BI Desktop | Report development and interactive visualisation |
| Power Query | Data import, preparation, and transformation |
| DAX | Measures and analytical calculations |
| Microsoft Excel | Source dataset |

## Dataset Overview

The source workbook is **Adidas Sales Datasets.xlsx**. The imported sales table contains 9,648 records and 13 fields.

| Field | Description |
|---|---|
| Retailer | Retail business associated with the sale |
| Retailer ID | Retailer identifier |
| Invoice Date | Date associated with the sales record |
| Region | sales region |
| State | State in which the sale was recorded |
| City | City in which the sale was recorded |
| Product | Adidas product category |
| Price per Unit | Unit selling price |
| Units Sold | Quantity sold |
| Total Sales | Recorded sales value |
| Operating Profit | Recorded operating profit |
| Operating Margin | Recorded operating margin |
| Sales Method | In-store, outlet, or online |

**Reporting period:** 2020–2021  
**Record count:** 9,648  
**Field count:** 13

## Dashboard Walkthrough

The report is arranged as a single-page overview. Filters are positioned in the left panel, headline KPIs run across the top, and the main analytical visuals fill the report canvas.

### 1. KPI cards

The KPI cards provide a quick summary of the selected data:

- **Total Revenue** – sum of the `Total Sales` field.
- **Total Orders** – the value displayed in the current report. See [Important Metric Definition](#important-metric-definition) before interpreting this as a count of orders.
- **Operating Profit** – sum of the `Operating Profit` field.
- **Total Units Sold** – sum of the `Units Sold` field.
- **Profit Margin** – operating profit divided by total sales, formatted as a percentage.

These cards respond to the report filters when the visual interactions are configured accordingly.

### 2. Revenue Contribution by Region — Donut chart

**Question answered:** How is total revenue distributed across the five regions?

- **Legend/category:** Region
- **Value:** Total Sales
- **Reading the chart:** Each segment represents a region's share of total revenue. Larger segments indicate a higher revenue contribution within the current filter selection.

The displayed distribution is:
- West — 30.00%
- Northeast — 20.70%
- Southeast — 18.13%
- South — 16.08%
- Midwest — 15.09%

### 3. Retailer-wise Sales Performance — Column chart

**Question answered:** Which retailers contribute the most revenue?

- **Category axis:** Retailer
- **Value axis:** Total Sales
- **Reading the chart:** Taller columns represent higher recorded sales for a retailer.

The visible ranking is:
1. West Gear — approximately 243M
2. Foot Locker — approximately 220M
3. Sports Direct — approximately 182M
4. Kohl's — approximately 102M
5. Amazon — approximately 78M
6. Walmart — approximately 75M

Values are shown in the dashboard's abbreviated display units.

### 4. Revenue by Sales Channel — Pie chart

**Question answered:** What proportion of revenue comes from each sales method?

- **Legend/category:** Sales Method
- **Value:** Total Sales
- **Reading the chart:** Each slice represents the channel's share of revenue.

The displayed distribution is:
- In-store — 39.63%
- Outlet — 32.85%
- Online — 27.52%

### 5. Monthly Revenue Trend — Area/line chart

**Question answered:** How does revenue change from month to month?

- **X-axis:** Invoice month, displayed chronologically
- **Y-axis:** Total Sales
- **Reading the chart:** The line shows the direction of monthly revenue, while the filled area emphasises the scale of sales over time. Peaks indicate stronger revenue months; dips indicate comparatively lower revenue months.

Use the Year slicer to compare the periods and inspect the monthly pattern for the selected year. Ensure the month field is sorted by a numeric year-month key rather than alphabetically.

### 6. Product-wise Sales & Profit Analysis — Clustered horizontal bar chart

**Question answered:** Which product categories generate the most sales, and how does operating profit compare?

- **Category axis:** Product
- **Values:** Total Sales and Operating Profit
- **Reading the chart:** The longer bar represents total sales and the shorter comparison bar represents operating profit for each product category.

The visible product values are approximately:

| Product | Total Sales | Operating Profit |
|---|---:|---:|
| Men's Street Footwear | 209M | 83M |
| Women's Apparel | 179M | 69M |
| Men's Athletic Footwear | 154M | 52M |
| Women's Street Footwear | 128M | 45M |
| Men's Apparel | 124M | 45M |
| Women's Athletic Footwear | 107M | 39M |

The chart supports comparison of both sales scale and operating profit across product categories.

## Headline Metrics

The KPI cards currently display the following values:

| KPI | Displayed value |
|---|---:|
| Total Revenue | 899.9M |
| Operating Profit | 332.13M |
| Total Units Sold | 2.48M |
| Profit Margin | 36.91% |
| Total Orders | 724 |

Values are transcribed from the dashboard screenshot and may be affected by report filters or display-unit rounding.

## Key Findings

Based on the dashboard's displayed results:

- **West** is the largest regional contributor, accounting for 30.00% of revenue.
- **In-store** is the largest sales channel by revenue share at 39.63%, followed by outlet and online.
- **West Gear** leads the retailer comparison with approximately 243M in sales.
- **Men's Street Footwear** is the leading product category in the displayed product comparison, with approximately 209M in sales and 83M in operating profit.
- **Women's Apparel** is the second-largest product category in the displayed comparison.
- The monthly trend shows variation over time, with visible higher-revenue months during 2021.

These observations describe the values visible in the report. They are descriptive findings, not explanations of why the results occurred.

## Interactivity

The report includes slicers for:

- **Year** – filter the report by reporting year.
- **Region** – focus on a selected region.
- **Sales Method** – focus on in-store, outlet, or online sales.

When slicers and visual interactions are enabled, the KPI cards and charts update to reflect the selected context. Selecting a data point in a chart may also cross-filter or highlight other visuals, depending on the report's Edit interactions settings.

## Analytical Approach

The project workflow includes:

1. Importing the Excel workbook into Power BI.
2. Preparing the sales table in Power Query.
3. Checking column names and assigning suitable data types.
4. Building measures for sales, operating profit, units sold, and profit margin.
5. Creating report visuals to compare performance across time, products, retailers, regions, and sales methods.
6. Arranging the visuals into a single-page dashboard.
7. Adding slicers and configuring visual interactions.
8. Reviewing displayed values and formatting for presentation.

Example measure definitions used for common calculations:

```dax
Total Sales =
SUM(Adidas_Sales[Total Sales])

Operating Profit =
SUM(Adidas_Sales[Operating Profit])

Units Sold =
SUM(Adidas_Sales[Units Sold])

Profit Margin =
DIVIDE(
    [Operating Profit],
    [Total Sales],
    0
)
```

If the model uses a dedicated calendar table, time-intelligence measures can also be added for prior-year sales and year-over-year growth.

## Conclusion

The Adidas Sales & Revenue Performance Analysis project successfully transformed raw sales data into an interactive Power BI dashboard. By analyzing 9,648 sales records across 2020 and 2021, the dashboard provides a clear understanding of revenue trends, operating profit, product performance, retailer contributions, regional sales distribution, and sales channel performance.

The analysis identified Men's Street Footwear as the leading product category, West Gear as the top-performing retailer, and the West region as the largest contributor to revenue. It also highlighted the contribution of in-store, outlet, and online sales channels.

Through Power Query, DAX, and interactive visualizations, this project demonstrates how business data can be converted into meaningful insights to support data-driven decision-making and sales performance monitoring.

## How to Use the Project

1. Download or clone this repository.
2. Open the `.pbix` file in Power BI Desktop (once added to the repository).
3. If prompted, update the source workbook path to the local location of the Excel dataset.
4. Refresh the data if the source workbook is available.
5. Use the Year, Region, and Sales Method slicers to explore the report.
6. Select chart elements to inspect cross-filtering between visuals.

```

## Limitations and Next Steps

- The dataset does not provide a unique order identifier, so order counts require a verified transaction key.
- The dashboard is descriptive; it does not establish causes behind sales changes.
- The source workbook should accompany the Power BI file only when its sharing terms permit redistribution.
- Future improvements could include year-over-year growth, profit by region, state-level drill-down, retailer and product drill-through pages, and report tooltips.

---

**Project:** Adidas Sales & Revenue Performance Analysis  
**Category:** Data Analytics | Business Intelligence  
**Platform:** Microsoft Power BI  
**Reporting Period:** 2020–2021
