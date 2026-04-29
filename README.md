# 📦 Supply Chain End-to-End Analytics Project  
### 🎓 DEPI Graduation Project | Digital Egypt Pioneers Initiative  

<p align="center">
  <img src="./Suply%20chain/image/Banar.gif" width="100%" alt="Project Banner" />
</p>

---

## 🧠 Project Overview
This project delivers a **comprehensive Data Analytics solution** designed to transform fragmented supply chain data into actionable business intelligence. It covers the entire data lifecycle—from engineering and modeling to exploratory analysis and executive reporting.

### 🚀 The Multi-Layer Architecture:
1.  **Engineering Layer (SQL):** Structuring raw data into a high-performance Star Schema.
2.  **Analysis Layer (Python):** Deep-dive EDA to uncover hidden trends and correlations.
3.  **Operational Layer (Excel):** Dynamic dashboard for day-to-day KPI tracking.
4.  **Strategic Layer (Power BI):** Interactive BI report for executive decision-making.

---

## 🏗️ Data Pipeline & Technical Workflow

### 🗄️ 1. SQL Data Engineering (The Foundation)
**Objective:** Cleanse and architect a relational database optimized for analytical queries.
* **Star Schema Design:** Created central `Fact_Sales` linked to `Dim_Products`, `Dim_Customers`, and `Dim_Location`.
* **Data Integrity:** Implemented Primary/Foreign Key constraints and handled NULL values/duplicates.
* **Files:** `sql/star_schema.sql`, `sql/ddl.sql`, `sql/dml.sql`

### 🐍 2. Python EDA (The Insight Layer)
<p align="center"> <img src="./Suply%20chain/image/p1.gif" width="85%" /> </p>
**Objective:** Use statistical computing to understand business drivers.
* **Analysis:** Univariate/Bivariate analysis, Pearson correlation for profit drivers, and shipping lead-time trends.
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn.
* **File:** `python/ecommerce_analysis.ipynb`

### 📊 3. Interactive Dashboards (The Visual Layer)
#### **Excel Operational Tools**
<p align="center"> <img src="./Suply%20chain/image/Dashboard%20Excel.gif" width="90%" /> </p>
* **Focus:** Revenue, Cost vs. Profit, and Delivery efficiency.
* **Tech:** Power Query, Pivot Tables, Dynamic Slicers.

#### **Power BI Strategic Insights**
<p align="center"> <img src="./Suply%20chain/image/p2.gif" width="45%" /> <img src="./Suply%20chain/image/p3.gif" width="45%" /> </p>
* **Advanced DAX:** Time Intelligence (YTD, MTD) and Profit Margin calculations.
* **UX/UI:** Drill-down features and cross-filtering for granular analysis.
* 🔗 **[Live Power BI Dashboard Link Here]**

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
├── 🐍 python/          # Jupyter Notebook for EDA
├── 📊 excel/           # Interactive Excel Dashboard
├── 📈 power-bi/        # PBIX Report file
├── 📂 assets/          # Project images and GIFs
└── README.md           # Project documentation
