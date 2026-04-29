# 📦 Supply Chain Analytics Project – DEPI Graduation  

<p align="center">
  <img src="./Suply%20chain/image/Banar.gif" width="100%" />
</p>

---

## 🧠 Project Summary  

This project is an **end-to-end Data Analytics solution** built as part of the **DEPI Graduation Program**.

It transforms raw supply chain data into a full analytical system using:

- 🗄️ SQL (Data Engineering Layer)  
- 🐍 Python (EDA & Insights Layer)  
- 📊 Excel (Analytical Dashboard Layer)  
- 📈 Power BI (Interactive BI Layer)  

---

# 🏗️ Data Pipeline Architecture  

```text id="pipeline"
Raw Data → SQL Cleaning → Star Schema → Python EDA → Excel Dashboard → Power BI Insights

🗄️ 1. SQL DATA ENGINEERING LAYER
📌 Purpose:

Transform raw data into structured relational model.

📁 Files:
Star Schema creation scripts
Fact table (Fact_Sales)
Dimension tables:
Dim_Products
Dim_Customers
Dim_Location
⚙️ What was done:
Data Cleaning (NULLs, duplicates)
Schema Design (Star Schema)
PK / FK Relationships
ETL Preparation
🐍 2. PYTHON ANALYSIS (EDA LAYER)
<p align="center"> <img src="./Suply%20chain/image/p1.gif" width="85%" /> </p>
📌 Purpose:

Exploratory Data Analysis + Insights generation

📊 Key Analyses:
Univariate analysis
Bivariate analysis
Correlation analysis
Trend analysis
Profitability distribution
Shipping performance
📁 Files:
ecommerce_analysis.ipynb
Charts folder:
p1.gif → Top Products Analysis
p2.gif → Trends Analysis
p3.gif → Profitability Analysis
📊 3. EXCEL DASHBOARD LAYER
<p align="center"> <img src="./Suply%20chain/image/Dashboard%20Excel.gif" width="90%" /> </p>
📌 Purpose:

Business-friendly KPI dashboard

📊 Features:
Revenue analysis
Cost & Profit tracking
Product performance
Delivery efficiency
Interactive filters
📁 File:
Dashboard Excel file (.xlsx)
📈 4. POWER BI DASHBOARD LAYER
<p align="center"> <img src="./Suply%20chain/image/p2.gif" width="85%" /> </p> <p align="center"> <img src="./Suply%20chain/image/p3.gif" width="85%" /> </p>
📌 Purpose:

Advanced Business Intelligence Dashboard

⚡ Features:
Dynamic KPIs
Drill-down analysis
Time Intelligence (YTD / MTD)
Category performance
Profitability insights
🧱 DATA MODEL (STAR SCHEMA)
<p align="center"> <img src="./Suply%20chain/image/Screenshot%202026-04-29%20124541.png" width="90%" /> </p>
📌 Structure:
Fact Table:
Fact_Sales
Dimension Tables:
Dim_Products
Dim_Customers
Dim_Location


Supply-Chain-Analysis/
│
├── sql/
│   ├── star_schema.sql
│   ├── ddl.sql
│   ├── dml.sql
│
├── python/
│   └── ecommerce_analysis.ipynb
│
├── excel/
│   └── dashboard.xlsx
│
├── power-bi/
│   └── report.pbix
│
├── Suply chain/
│   └── image/
│       ├── Banar.gif
│       ├── Dashboard Excel.gif
│       ├── p1.gif
│       ├── p2.gif
│       ├── p3.gif
│       ├── Screenshot 2026-04-29 124541.png
│
└── README.md

🔥 KEY ACHIEVEMENTS

✔ End-to-End Data Pipeline
✔ Star Schema Data Modeling
✔ Multi-tool Analytics System
✔ Python + SQL + BI Integration
✔ Business Insight Generation

💡 BUSINESS IMPACT
Improved supply chain visibility
Identified inefficiencies in delivery
Enhanced decision-making
Optimized product performance tracking
🛠️ TOOLS USED
SQL Server
Python (Pandas, Matplotlib, Seaborn)
Excel (Power Query, Pivot Tables)
Power BI
Kaggle Dataset
🚀 FINAL NOTE

This project demonstrates a real-world Data Analytics lifecycle, from raw data ingestion to actionable business intelligence dashboards.


