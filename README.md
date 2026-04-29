# 📦 Supply Chain End-to-End Analytics Project  
### 🎓 DEPI Graduation Project | Digital Egypt Pioneers Initiative  

<p align="center">
  <img src="./Suply%20chain/image/Banar.gif" width="100%" alt="Project Banner" />
</p>

---

## 🧠 Project Overview
This project delivers a **comprehensive Data Analytics solution** designed to transform fragmented supply chain data into actionable business intelligence. It covers the entire data lifecycle—from engineering and modeling to executive reporting and deep-dive analysis.

### 🚀 The Multi-Layer Architecture:
1.  **Engineering Layer (SQL):** Structuring raw data into a high-performance Star Schema.
2.  **Operational Layer (Excel):** Dynamic dashboard for day-to-day KPI tracking.
3.  **Strategic Layer (Power BI):** Interactive BI report for executive decision-making.
4.  **In-depth Analysis Layer (Python):** Deep-dive EDA to uncover hidden trends and correlations.

---

## 👥 Team Collaboration & Methodology 
As a specialized data team, we followed a structured **Data Pipeline** approach to ensure accuracy and scalability:

* **Data Architecture:** We designed a robust **Star Schema** in SQL Server to act as our "Single Source of Truth."
* **Operational Excellence:** Built automated Excel workflows for real-time tracking of costs and delivery efficiency.
* **Strategic Visualization:** Translated datasets into interactive Power BI stories for executive drill-down analysis.
* **Advanced Analytics:** Utilized Python to identify key drivers behind profitability and shipping delays.

---

## 🏗️ Data Pipeline Architecture
> **Workflow:** Raw Data → SQL Cleaning → Star Schema → Excel Dashboard → Power BI Insights → Python EDA

### 🗄️ 1. SQL Data Engineering Layer
<p align="center"> <img src="./Suply%20chain/image/sql.gif" width="85%" /> </p>

**🎯 Objective:** Build a structured relational database optimized for analytics.
* **Work Done:** Data Cleaning (NULLs, duplicates), Star Schema Design, Primary & Foreign Keys, and ETL Preparation.
* **📁 Source Code:** [Click here to view SQL Queries](./Suply%20chain/sql/SQLQuerycode%20projects.sql)
* **Files:** `sql/star_schema.sql`, `sql/ddl.sql`, `sql/dml.sql`

### 📊 2. Excel Dashboard Layer
<p align="center"> <img src="./Suply%20chain/image/Dashboard%20Excel.gif" width="90%" /> </p>

**🎯 Objective:** Create an interactive business-friendly KPI dashboard for operational monitoring.
* **Features:** Revenue analysis, Cost vs Profit tracking, and Delivery efficiency with Interactive filters.
* **File:** [Dashboard.xlsx](./excel/Dashboard.xlsx)

### 📈 3. Power BI Dashboard Layer
<p align="center">  
  <img src="./Suply%20chain/image/p1.gif" width="85%" />  
  <img src="./Suply%20chain/image/p2.gif" width="45%" />  
  <img src="./Suply%20chain/image/p3.gif" width="45%" />  
</p>

**🎯 Objective:** Build an executive-level BI dashboard for strategic decision-making.
* **Features:** Advanced KPI Cards, Drill-down analysis, Time Intelligence (YTD / MTD), and Category performance.
* 🔗 **Live Report:** [View Interactive Dashboard](https://app.powerbi.com/groups/me/reports/254e4782-bdef-46ff-a6f3-5f18e4489ad0/50f66f92d057c0501c0e?experience=power-bi)

### 🐍 4. Python Analysis (EDA Layer)
**🎯 Objective:** Extract deep statistical insights and business drivers using data science libraries.
* **Analyses:** Univariate/Bivariate analysis, Pearson correlation, Heatmaps, and Time-series (YoY) trends.
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn.
* **📂 Source Code:** [View Jupyter Notebook (Python Code)](./Suply%20chain/Python/ecommerce_analysis.ipynb)

#### 📊 EDA Visualization Gallery
<details>
  <summary><b>Click to expand and view Analysis Charts (13 Charts)</b></summary>
  <br>
  <table align="center">
    <tr>
      <td><b>Top Products</b><br><img src="Suply%20chain/Python/chart_top_products.png" width="300"/></td>
      <td><b>Profit Distribution</b><br><img src="Suply%20chain/Python/chart_profit_dist.png" width="300"/></td>
    </tr>
    <tr>
      <td><b>Trend Analysis</b><br><img src="Suply%20chain/Python/chart_trend.png" width="300"/></td>
      <td><b>Year-over-Year (YoY)</b><br><img src="Suply%20chain/Python/chart_yoy.png" width="300"/></td>
    </tr>
    <tr>
      <td><b>Correlation Matrix</b><br><img src="Suply%20chain/Python/chart_correlation.png" width="300"/></td>
      <td><b>Heatmap Analysis</b><br><img src="Suply%20chain/Python/chart_heatmap.png" width="300"/></td>
    </tr>
    <tr>
      <td><b>Shipping Performance</b><br><img src="Suply%20chain/Python/chart_shipping.png" width="300"/></td>
      <td><b>Late Delivery Risk</b><br><img src="Suply%20chain/Python/chart_late_delivery.png" width="300"/></td>
    </tr>
    <tr>
      <td><b>Bivariate Analysis</b><br><img src="Suply%20chain/Python/chart_bivariate.png" width="300"/></td>
      <td><b>Univariate Analysis</b><br><img src="Suply%20chain/Python/chart_univariate.png" width="300"/></td>
    </tr>
    <tr>
      <td><b>Department Performance</b><br><img src="Suply%20chain/Python/chart_departments.png" width="300"/></td>
      <td><b>Payment Methods</b><br><img src="Suply%20chain/Python/chart_payment.png" width="300"/></td>
    </tr>
    <tr>
      <td colspan="2" align="center"><b>Categorical Features</b><br><img src="Suply%20chain/Python/chart_categoricals.png" width="400"/></td>
    </tr>
  </table>
</details>

## 🧱 Data Model (Star Schema)
<p align="center">  
  <img src="./Suply%20chain/image/Screenshot%202026-04-29%20124541.png" width="80%" />  
</p>

---

## 📁 Project Structure
```text
Supply-Chain-Analysis/
├── 🗄️ sql/             # DDL, DML, and Star Schema scripts
├── 📊 excel/           # Interactive Excel Dashboard
├── 📈 power-bi/        # PBIX Report file
├── 🐍 python/          # Jupyter Notebook for EDA
├── 📂 Suply chain/     # Assets and Images
└── README.md           # Project documentation
