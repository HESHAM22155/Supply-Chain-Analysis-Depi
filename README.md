# 📦 Supply Chain End-to-End Analytics
> A comprehensive, multi-layer data analytics solution that transforms fragmented supply chain data into strategic business intelligence — from raw data engineering to executive-level dashboards and predictive insights.

<p align="center">
  <img src="./Suply%20chain/image/Banar.gif" width="100%" alt="Project Banner" />
</p>

---

## 🧠 Business Problem
Modern supply chains generate vast amounts of transactional data across orders, shipments, customers, and products. Without a structured analytical framework, this data remains siloed and underutilized, leaving critical questions unanswered:
- Which markets and customer segments are driving the most revenue?
- Why are more than half of all deliveries arriving late?
- Which product categories yield the highest profit margins?
- Are revenue trends stable, growing, or declining over time?

This project addresses these challenges by building a production-grade analytics pipeline — from a normalized star schema in SQL Server to Python-powered EDA.

---

## 🏗️ Project Architecture
> **Workflow:** Raw Data → SQL Cleaning → Star Schema → Excel Dashboard → Power BI Insights → Python EDA

| Layer | Tool | Audience |
|---|---|---|
| **1. Data Engineering** | SQL Server | Data Engineers / Architects |
| **2. Operational Monitoring** | Excel | Operations Managers |
| **3. Strategic Intelligence** | Power BI | Executives / Leadership |
| **4. Advanced Analytics** | Python | Data Analysts / Scientists |

---

## 🗄️ 1. SQL Data Engineering Layer
<p align="center"> <img src="./Suply%20chain/image/sql.gif" width="85%" /> </p>

**🎯 Objective:** Design a scalable star schema data warehouse optimized for analytical queries.
* **Work Done:** Data Cleaning (NULLs, duplicates), Star Schema Design, and ETL Preparation.
* **📁 Source Code:** [View SQL Queries & Scripts](./Suply%20chain/sql/SQLQuerycode%20projects.sql)

---

## 📊 2. Excel Dashboard Layer
<p align="center"> <img src="./Suply%20chain/image/Dashboard%20Excel.gif" width="90%" /> </p>

**🎯 Objective:** Build an interactive operational dashboard for day-to-day KPI monitoring.
* **Features:** Revenue analysis, Cost vs Profit tracking, and Delivery efficiency with Interactive filters.

---

## 📈 3. Power BI Dashboard Layer
<p align="center">  
  <img src="./Suply%20chain/image/p1.gif" width="85%" />  
  <img src="./Suply%20chain/image/p2.gif" width="45%" />  
  <img src="./Suply%20chain/image/p3.gif" width="45%" />  
</p>

**🎯 Objective:** Deliver an executive-level Power BI report with drill-down capabilities and time intelligence.
* 🔗 **Live Report:** [View Interactive Dashboard](https://app.powerbi.com/groups/me/reports/254e4782-bdef-46ff-a6f3-5f18e4489ad0/50f66f92d057c0501c0e?experience=power-bi)

---

## 🐍 4. Python Analysis (EDA Layer)
**🎯 Objective:** Perform exploratory data analysis to surface hidden trends, correlations, and anomalies.
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

---

## 🧱 Data Model (Star Schema)
<p align="center">  
  <img src="./Suply%20chain/image/Screenshot%202026-04-29%20124541.png" width="80%" />  
</p>

---

## 👥 Project Team & Methodology
This project was delivered collaboratively by our specialized data team:
* **Hesham Lotfy** 
* **Abdallah Hossam Eldin**
* **Fatma Ahmed Ali Fahmy**
* **Nada Abdelghany Abdeltwap**
* **Marim Ibrahim Abdelsalam**
* **Mariam Gamal Abdelgawad**

**Supervised by:** Eng. Sara Besher  
**Program:** Digital Egypt Pioneers Initiative (DEPI)

---

## 🛠️ Tools & Technologies
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat&logo=microsoft-sql-server&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=power-bi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
