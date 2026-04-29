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

## 🏗️ Data Pipeline Architecture
> **Workflow:** Raw Data → SQL Cleaning → Star Schema → Excel Dashboard → Power BI Insights → Python EDA

### 🗄️ 1. SQL Data Engineering Layer
<p align="center"> <img src="./Suply%20chain/image/sql.gif" width="85%" /> </p>

**🎯 Objective:** Build a structured relational database optimized for analytics.
* **Work Done:** Data Cleaning, Star Schema Design, and ETL Preparation.
* **📁 Source Code:** [Click here to view SQL Queries](./Suply%20chain/sql/SQLQuerycode%20projects.sql)

**🎯 Objective:** Build a structured relational database optimized for analytics.
* **Work Done:** Data Cleaning (NULLs, duplicates), Star Schema Design (Fact & Dimension Tables), Primary & Foreign Keys, and ETL Preparation.
* **Files:** `sql/star_schema.sql`, `sql/ddl.sql`, `sql/dml.sql`

### 📊 2. Excel Dashboard Layer
<p align="center"> <img src="./Suply%20chain/image/Dashboard%20Excel.gif" width="90%" /> </p>

**🎯 Objective:** Create an interactive business-friendly KPI dashboard for operational monitoring.
* **Features:** Revenue analysis, Cost vs Profit tracking, Product performance, and Delivery efficiency with Interactive filters.
* **File:** `excel/Dashboard.xlsx`

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
* **Analyses:** Univariate/Bivariate analysis, Pearson correlation for profit drivers, and Trend Analysis.
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn.
* **📂 Source Code:** [View Jupyter Notebook (Python Code)](./Suply%20chain/Python/ecommerce_analysis.ipynb)

---

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
