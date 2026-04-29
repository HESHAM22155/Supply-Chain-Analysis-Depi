# 🗄️ 1. SQL DATA ENGINEERING LAYER  

## 📌 Objective  
Transform raw messy data into a structured relational database.

## ⚙️ Work Done  
- Data Cleaning (NULL handling, duplicates removal)  
- Star Schema Design  
- Fact & Dimension Tables creation  
- Primary & Foreign Keys relationships  
- ETL preparation for BI tools  

## 📁 Files  
- star_schema.sql  
- ddl.sql  
- dml.sql  

---

# 🐍 2. PYTHON ANALYSIS (EDA LAYER)

<p align="center">
  <img src="./Suply%20chain/image/p1.gif" width="85%" />
</p>

## 📌 Objective  
Exploratory Data Analysis to extract business insights.

## 📊 Analyses Performed  
- Univariate Analysis  
- Bivariate Analysis  
- Correlation Analysis  
- Trend Analysis  
- Profitability Analysis  
- Shipping Performance Analysis  

## 📁 Files  
- ecommerce_analysis.ipynb  
- p1.gif → Top Products Analysis  
- p2.gif → Trend Analysis  
- p3.gif → Profitability Analysis  

---

# 📊 3. EXCEL DASHBOARD LAYER  

<p align="center">
  <img src="./Suply%20chain/image/Dashboard%20Excel.gif" width="90%" />
</p>

## 📌 Objective  
Create a business-friendly interactive dashboard.

## 📊 Features  
- Revenue Analysis  
- Cost vs Profit Tracking  
- Product Performance KPIs  
- Delivery Efficiency Metrics  
- Interactive Filtering  

## 📁 File  
- Dashboard.xlsx  

---

# 📈 4. POWER BI DASHBOARD LAYER  

<p align="center">
  <img src="./Suply%20chain/image/p2.gif" width="85%" />
</p>

<p align="center">
  <img src="./Suply%20chain/image/p3.gif" width="85%" />
</p>

## 📌 Objective  
Advanced interactive Business Intelligence dashboard.

## ⚡ Features  
- Dynamic KPI cards  
- Drill-down analysis  
- Time intelligence (YTD / MTD)  
- Category performance analysis  
- Profitability insights  

## 📁 File  
- Report.pbix  

---

# 🧱 DATA MODEL (STAR SCHEMA)

<p align="center">
  <img src="./Suply%20chain/image/Screenshot%202026-04-29%20124541.png" width="90%" />
</p>

## 📌 Structure  

### ⭐ Fact Table:
- Fact_Sales  

### 📁 Dimension Tables:
- Dim_Products  
- Dim_Customers  
- Dim_Location  

---

# 📁 PROJECT STRUCTURE  

```bash id="structure_clean"
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
