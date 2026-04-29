# 🗄️ SQL Data Engineering Layer  
### Supply Chain Analysis – DEPI Project  

---

## 📌 Project Overview  

This folder contains the **SQL Data Engineering layer** of the Supply Chain Analysis project.  

The main objective is to transform raw logistics data into a **structured Star Schema database**, enabling efficient analytics and reporting in Power BI and Python.

---

## 🎯 Objective  

- Clean and standardize raw data  
- Design a scalable **Star Schema model**  
- Build Fact and Dimension tables  
- Enable data integration for BI tools  

---

## 🧱 Data Modeling (Star Schema)

### ⭐ Fact Table:
- `Fact_Sales`

### 📁 Dimension Tables:
- `Dim_Products`
- `Dim_Customers`
- `Dim_Location`

---

## ⚙️ ETL Process (SQL Pipeline)

### 1️⃣ Data Cleaning
- Removed duplicates  
- Handled missing values  
- Standardized column formats  
- Fixed inconsistent data types  

---

### 2️⃣ Data Transformation
- Normalized raw dataset  
- Split data into Fact & Dimensions  
- Defined relationships between tables  

---

### 3️⃣ Data Loading
- Inserted cleaned data into structured schema  
- Ensured referential integrity using PK/FK  

---

## 📂 Project Structure  

```bash
sql-engineering/
│
├── ddl/
│   └── create_tables.sql
│
├── dml/
│   └── insert_data.sql
│
├── star_schema/
│   ├── fact_sales.sql
│   ├── dim_products.sql
│   ├── dim_customers.sql
│   ├── dim_location.sql
│
├── data/
│   └── cleaned_csv_files/
│
└── README.md
