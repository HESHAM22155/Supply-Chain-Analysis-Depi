# Supply Chain End-to-End Analytics

> A comprehensive, multi-layer data analytics solution that transforms fragmented supply chain data into strategic business intelligence — from raw data engineering to executive-level dashboards and predictive insights.

---

## Business Problem

Modern supply chains generate vast amounts of transactional data across orders, shipments, customers, and products. Without a structured analytical framework, this data remains siloed and underutilized, leaving critical questions unanswered:

- Which markets and customer segments are driving the most revenue?
- Why are more than half of all deliveries arriving late?
- Which product categories yield the highest profit margins?
- Are revenue trends stable, growing, or declining over time?

This project addresses these challenges by building a production-grade analytics pipeline — from a normalized star schema in SQL Server to Python-powered EDA — enabling data-driven decisions across operations, sales, and executive leadership.

---

## Project Architecture

```
Raw Data
    └── SQL Server (Star Schema / Data Warehouse)
            └── Excel Dashboard (Operational KPIs)
                    └── Power BI Report (Strategic Insights)
                            └── Python EDA (Deep-Dive Analytics)
```

The pipeline follows four layers, each serving a distinct analytical audience:

| Layer | Tool | Audience |
|---|---|---|
| Data Engineering | SQL Server | Data Engineers / Architects |
| Operational Monitoring | Excel | Operations Managers |
| Strategic Intelligence | Power BI | Executives / Leadership |
| Advanced Analytics | Python (Pandas, Matplotlib, Seaborn) | Data Analysts / Scientists |

---

## Objectives

- Design a scalable star schema data warehouse optimized for analytical queries
- Build an interactive operational dashboard for day-to-day KPI monitoring
- Deliver an executive-level Power BI report with drill-down capabilities and time intelligence
- Perform exploratory data analysis (EDA) to surface hidden trends, correlations, and anomalies
- Quantify the business impact of late deliveries, discount strategies, and product mix

---

## Tools & Technologies

| Category | Technology |
|---|---|
| Database & Modeling | SQL Server, T-SQL, Star Schema Design |
| Data Transformation | ETL via SQL (DDL, DML, INSERT/SELECT pipelines) |
| Operational Reporting | Microsoft Excel (PivotTables, Slicers, Dynamic Charts) |
| Business Intelligence | Microsoft Power BI (DAX, Time Intelligence, Drill-through) |
| Advanced Analytics | Python — Pandas, NumPy, Matplotlib, Seaborn |
| Development Environment | Jupyter Notebook |
| Version Control | Git / GitHub |

---

## Data Model — Star Schema

The data warehouse is structured as a **star schema** centered on a `Fact_Sales` table linked to five dimension tables, enabling fast, flexible analytical querying:

```
                    Dim_Date
                       │
Dim_Customer ──── Fact_Sales ──── Dim_Product
                       │               │
                 Dim_Location     Dim_Category
```

### Fact Table: `Fact_Sales`
Contains all measurable transactional data per order line item, including sales amounts, discounts, profit, shipping schedules, and payment type.

Key metrics stored: `Sales`, `Order_Item_Total`, `Order_Profit_Per_Order`, `Order_Item_Discount_Rate`, `Days_Shipping_Real`, `Days_Shipment_Scheduled`

### Dimension Tables

| Table | Grain | Key Attributes |
|---|---|---|
| `Dim_Customer` | One row per customer | Segment, City, State, Country |
| `Dim_Product` | One row per product | Name, Price, Category, Department |
| `Dim_Location` | One row per delivery location | City, State, Region, Market |
| `Dim_Date` | One row per calendar date | Day, Month, Quarter, Year, Week |
| `Dim_Category` | One row per product category | Category Name, Department |

---

## Data Processing Steps

**1. Data Cleaning & Validation**
- Identified and resolved NULL values across all dimension and fact staging tables
- Removed duplicates using `DISTINCT` in INSERT pipelines
- Validated referential integrity with LEFT JOIN null checks across all foreign key relationships
- Confirmed row counts and business totals (Sales, Quantity, Profit) post-load

**2. Star Schema Construction**
- Designed surrogate key strategy (`_SK` columns) for all dimension tables
- Built DDL scripts with proper PRIMARY KEY and FOREIGN KEY constraints
- Implemented ETL logic to populate dimensions from staging (`_0` suffix) tables, then loaded the fact table

**3. Dimension Enrichment**
- Added `Category_SK` to `Dim_Product` via `ALTER TABLE` and populated it with a correlated `UPDATE` from the source staging table
- Linked `Dim_Category` to departments via `Department_SK` for hierarchical analysis

**4. Python EDA Pipeline**
- Loaded the warehouse data into a Jupyter Notebook environment
- Performed univariate and bivariate distribution analysis on all key numeric variables
- Engineered a `Late_Delivery_Risk` binary flag and analyzed its drivers
- Generated 13 publication-quality charts across revenue, profitability, shipping, and customer segments

---

## Key Insights & Findings

### Revenue & Market Performance
- Total revenue is distributed across three customer segments: Consumer ($19.1M), Corporate ($11.2M), and Home Office ($6.5M) — with Consumer accounting for the majority share
- Geographically, Europe ($10.9M) and LATAM ($10.3M) are the top two markets, together representing approximately 58% of total revenue
- Revenue remained stable between 2015 ($12.3M) and 2016 ($12.3M), declined modestly in 2017 ($11.8M, -4.0% YoY), and dropped sharply in 2018 ($0.3M, -97.2% YoY), indicating either data truncation for that year or a significant business disruption

### Product & Department Performance
- The top-revenue product is the Field & Stream Sportsman 16 Gun Fire Safe at $6.93M — more than 1.5x the second-ranked product
- Fan Shop is the highest-revenue department at ~$17M, while Fitness achieves the highest profit margin percentage (~12.7%) despite lower absolute revenue
- Technology has the lowest profit margin among mid-revenue departments (~8.6%), suggesting pricing or cost structure issues

### Shipping & Delivery
- The average actual shipping time is 3.5 days, against a scheduled benchmark skewed toward 4 days — indicating many orders ship faster than scheduled
- Late delivery rate is persistently high across all markets, averaging 54.8%, with a narrow range of 54.4% (LATAM) to 55.2% (Europe) — suggesting a systemic operational issue rather than a market-specific one
- The `Late_Delivery_Risk` feature has a moderate positive correlation (0.40) with `Days_Shipping_Real`, confirming that actual shipping duration is a primary driver of lateness

### Profitability
- Profit per order follows a right-skewed distribution with a mean of $23.3 and median of $31.5, indicating that a subset of high-discount or high-cost orders pulls the average down significantly
- A notable proportion of orders yield negative profit, visible in the left tail of the distribution extending to -$400+
- Discount rate shows a weak negative correlation (-0.12) with `Order_Item_Total`, suggesting discounts are not systematically applied to high-value orders

### Customer & Payment Behavior
- Consumer segment accounts for 93,504 orders vs. 54,789 for Corporate and 32,226 for Home Office
- Debit is the dominant payment method (38.4%), followed by Transfer (27.6%), Payment (23.1%), and Cash (10.9%)
- COMPLETE is the most frequent order status (59,491 orders), while PAYMENT_REVIEW (1,893) and CANCELED (3,692) together represent under 3% of total orders

### Correlation Structure
- `Sales` and `Order_Item_Total` have a near-perfect correlation (0.99), as expected
- No strong correlations exist between financial metrics and operational metrics (shipping days, discount rate), suggesting these are largely independent levers

---

## Business Impact

| Finding | Recommended Action |
|---|---|
| 54.8% average late delivery rate across all markets | Investigate logistics partners and fulfillment center capacity; implement SLA-based carrier scoring |
| Technology department has the lowest profit margin | Review supplier contracts and product pricing strategy for tech SKUs |
| Fitness achieves the highest margin despite low revenue | Prioritize Fitness category marketing and inventory expansion |
| Negative-profit orders in left-tail distribution | Implement minimum discount floor rules and review return/cancellation cost attribution |
| Revenue decline trend from 2015–2017 | Conduct cohort analysis on customer retention and order frequency to identify churn drivers |
| Consumer segment is 60%+ of order volume | Develop targeted loyalty programs to reduce dependency on a single segment |

---

## Project Structure

```
Supply-Chain-Analytics/
├── sql/
│   └── SQLQuerycode_projects.sql      # DDL, DML, ETL pipeline, validation queries
├── excel/
│   └── Dashboard.xlsx                 # Interactive KPI dashboard
├── power-bi/
│   └── SupplyChain_Report.pbix        # Executive BI report (live: Power BI Service)
├── python/
│   └── ecommerce_analysis.ipynb       # Full EDA notebook (13 charts)
├── charts/
│   ├── chart_top_products.png
│   ├── chart_profit_dist.png
│   ├── chart_trend.png
│   ├── chart_yoy.png
│   ├── chart_correlation.png
│   ├── chart_heatmap.png
│   ├── chart_shipping.png
│   ├── chart_late_delivery.png
│   ├── chart_bivariate.png
│   ├── chart_univariate.png
│   ├── chart_departments.png
│   ├── chart_payment.png
│   └── chart_categoricals.png
└── README.md
```

---

## EDA Visualization Gallery

<table>
  <tr>
    <td><b>Top 10 Products by Revenue</b><br><img src="charts/chart_top_products.png" width="380"/></td>
    <td><b>Profit Distribution by Segment</b><br><img src="charts/chart_profit_dist.png" width="380"/></td>
  </tr>
  <tr>
    <td><b>Monthly Sales & Profit Trend</b><br><img src="charts/chart_trend.png" width="380"/></td>
    <td><b>Annual Revenue — Year-over-Year</b><br><img src="charts/chart_yoy.png" width="380"/></td>
  </tr>
  <tr>
    <td><b>Correlation Matrix</b><br><img src="charts/chart_correlation.png" width="380"/></td>
    <td><b>Monthly Revenue Heatmap</b><br><img src="charts/chart_heatmap.png" width="380"/></td>
  </tr>
  <tr>
    <td><b>Scheduled vs Actual Shipping Days</b><br><img src="charts/chart_shipping.png" width="380"/></td>
    <td><b>Late Delivery Rate by Market</b><br><img src="charts/chart_late_delivery.png" width="380"/></td>
  </tr>
  <tr>
    <td><b>Revenue & Profit Margin by Department</b><br><img src="charts/chart_departments.png" width="380"/></td>
    <td><b>Payment Type Distribution</b><br><img src="charts/chart_payment.png" width="380"/></td>
  </tr>
  <tr>
    <td><b>Sales Breakdown by Segment & Market</b><br><img src="charts/chart_bivariate.png" width="380"/></td>
    <td><b>Distribution of Key Numeric Variables</b><br><img src="charts/chart_univariate.png" width="380"/></td>
  </tr>
  <tr>
    <td colspan="2" align="center"><b>Categorical Variable Distributions</b><br><img src="charts/chart_categoricals.png" width="500"/></td>
  </tr>
</table>

---

## Team Methodology

This project was delivered collaboratively by a specialized data team following a structured pipeline approach:

**Step 1 — Data Architecture Design**
Designed the star schema from scratch: identified fact and dimension grain, defined surrogate key strategy, and mapped source-to-target field lineage before writing a single line of SQL.

**Step 2 — SQL Engineering & ETL**
Built the complete DDL (table creation with constraints), DML (INSERT/SELECT pipelines from staging tables), and validation queries. Applied data quality checks for NULLs, duplicates, and referential integrity post-load.

**Step 3 — Operational Dashboard (Excel)**
Developed an interactive Excel dashboard with PivotTables and slicers for real-time revenue, cost, and delivery efficiency tracking — designed for operational managers who need daily insights without a BI tool.

**Step 4 — Strategic BI Report (Power BI)**
Built an executive-facing Power BI report with DAX measures for YTD/MTD time intelligence, drill-through analysis by market and product category, and KPI cards aligned to business targets.

**Step 5 — Python EDA**
Conducted a systematic exploratory data analysis in Jupyter Notebook — univariate distributions, bivariate scatter analysis, correlation matrices, time series decomposition, and shipping performance profiling — generating 13 charts that informed the final recommendations.

---

## Live Resources

- **Power BI Dashboard:** [View Interactive Report](https://app.powerbi.com/groups/me/reports/254e4782-bdef-46ff-a6f3-5f18e4489ad0/50f66f92d057c0501c0e?experience=power-bi)

---

## Conclusion

This project demonstrates a complete, production-aligned data analytics workflow — from raw transactional data to boardroom-ready intelligence. The most critical finding is that over half of all orders are delivered late regardless of market or region, pointing to a systemic logistics challenge with significant customer satisfaction and cost implications. Equally, the profit distribution analysis reveals meaningful margin leakage from unstructured discounting and high-cost SKUs.

By building this pipeline on a properly engineered star schema, every insight produced is traceable, reproducible, and scalable — providing a reliable foundation for future predictive modeling, demand forecasting, or logistics optimization initiatives.

---

*DEPI Graduation Project | Digital Egypt Pioneers Initiative*
