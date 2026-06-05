<div align="center">
  <img src="images/coffee_logo.png" alt="Coffee DWBI Logo" width="160" />
</div>

<h1 align="center">☕ Coffee Orders Data Warehouse & Business Intelligence Solution</h1>

<p align="center">
  <strong>End-to-End Data Warehousing, ETL, OLAP & Power BI Analytics Solution</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/SQL%20Server-DW%20Design-CC2927?style=flat-square&logo=microsoft-sql-server&logoColor=white" />
  <img src="https://img.shields.io/badge/SSIS-ETL-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/SSAS-OLAP-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Power%20BI-Dashboards-F2C811?style=flat-square&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Excel-Pivot%20OLAP-217346?style=flat-square&logo=microsoft-excel&logoColor=white" />
</p>

---

## 📌 Project Overview

This project is a complete **Data Warehousing and Business Intelligence (DWBI)** solution built using a real-world **Coffee Orders dataset (Kaggle)**.

It demonstrates the full lifecycle of a BI system:

- Data Warehouse Design
- ETL Development using SSIS
- Slowly Changing Dimensions (SCD)
- Accumulating Fact Tables
- SSAS OLAP Cube Development
- Excel OLAP Analysis
- Interactive Power BI Dashboards

---

## 📊 Business Objectives

The solution enables analysis of:

- Sales performance trends
- Customer behavior patterns
- Product category performance
- Profitability analysis
- Geographic sales distribution
- Time-based business insights

---

## 🏗️ Solution Architecture

The system follows a standard DWBI architecture:

1. Data Sources  
2. Staging Area (ETL Processing)  
3. Data Warehouse  
4. SSAS OLAP Cube  
5. Reporting & Visualization (Power BI / Excel)

---

## 📂 Data Sources

| Source Type | Description |
|------------|-------------|
| Excel Files | Customers, Orders, Products, Categories |
| Text File | Customer Address Data |
| SQL Database | CoffeeOrders_SourceDB |

---

## 🗄️ Data Warehouse Design

A **Snowflake Schema** was used to support hierarchical product analysis and reduce redundancy.

### ⭐ Fact Table
- FactSales

### ⭐ Dimension Tables
- DimDate  
- DimCustomer  
- DimProduct  
- DimProductSubCategory  
- DimProductCategory  

<p align="center">
  <img src="images/snowflake-schema.png" width="900"/>
</p>

### Key Features
- Slowly Changing Dimensions (SCD Type 1 & 2)
- Surrogate Keys
- Date Dimension
- Product Hierarchies
- Historical Data Tracking
- Accumulating Fact Table

---

## 🔄 ETL Development (SSIS)

ETL was implemented using **SQL Server Integration Services (SSIS)**.

### Extraction Sources
- Excel Files  
- Text Files  
- SQL Server Database  

### Staging Tables
- StgCustomers  
- StgOrders  
- StgProducts  
- StgProductCategory  
- StgProductSubCategory  
- StgCustomerAddress  

### Transformations
- Data cleansing  
- Data profiling  
- Data mapping  
- Lookup transformations  
- SCD implementation  
- Surrogate key generation  

### Loading
Data is loaded into:
- Dimension Tables  
- FactSales Table  

<p align="center">
  <img src="images/ssis-etl.png" width="900"/>
</p>

---

## 📈 Data Profiling

Data profiling was performed to ensure data quality by analyzing:

- Null values
- Duplicate records
- Data distributions
- Min/Max values
- Distinct counts
- Data patterns

---

## ⚙️ Accumulating Fact Table

The FactSales table was enhanced with lifecycle tracking:

| Column | Description |
|--------|-------------|
| accm_txn_create_time | Order creation time |
| accm_txn_complete_time | Order completion time |
| txn_process_time_hours | Processing duration |

### Benefits
- Order lifecycle tracking
- Process efficiency analysis
- Operational performance insights

---

# 🧊 SSAS OLAP Cube

An OLAP cube was built using **SQL Server Analysis Services (SSAS)**.

### Cube Components
- Measure Group: FactSales  
- Dimensions: Date, Customer, Product  

### Hierarchies

**Date Hierarchy:**  
Year → Quarter → Month → Date  

**Product Hierarchy:**  
Category → SubCategory → Product  

**Customer Hierarchy:**  
Country → City → Address  

<p align="center">
  <img src="images/cube-hierarchy.png" width="900"/>
</p>

---

## 🎯 KPIs

### 💰 Total Sales Revenue
Measures overall revenue performance against targets.

### 📊 Average Order Value
Tracks customer spending behavior per order.

---

# 🔍 OLAP Operations

Connected via **Excel Pivot Tables**.

### Operations Demonstrated:

- **Roll-Up** → Category-level aggregation  
- **Drill-Down** → Category → Product level  
- **Slice** → Filter by Loyalty Customers  
- **Dice** → Multi-dimensional filtering  
- **Pivot** → Dimension rotation  

---

# 📊 Power BI Dashboards

The data warehouse was connected to **Power BI Desktop** and published to Power BI Service.

---

## 📌 Report 1 – Matrix Analysis

- Product-wise sales by year  
- Performance comparison  

<p align="center">
  <img src="images/powerbi-report1.png" width="900"/>
</p>

---

## 📌 Report 2 – Geographic Analysis

Features:
- Cascading slicers (Country → City → Address)
- Map visualization
- Line chart trends
- Donut chart distribution

<p align="center">
  <img src="images/powerbi-report2.png" width="900"/>
</p>

---

## 📌 Report 3 – Drill-Down Analysis

- Category → Product → Time hierarchy
- Interactive exploration

<p align="center">
  <img src="images/powerbi-report3.png" width="900"/>
</p>

---

## 📌 Report 4 – Drill-Through Dashboard

Deep-dive analytics view

<p align="center">
  <img src="images/powerbi-dashboard.png" width="900"/>
</p>

<p align="center">
  <img src="images/drillthrough-page.png" width="900"/>
</p>

---

# 🛠️ Technologies Used

| Tool | Purpose |
|------|--------|
| SQL Server | Data Warehouse |
| SSIS | ETL Process |
| SSAS | OLAP Cube |
| Excel | Pivot Analysis |
| Power BI | Visualization |
| SQL | Data Processing |

---

# 📈 Key Insights Enabled

- Sales trend analysis over time  
- Customer loyalty impact  
- Product performance ranking  
- Geographic sales distribution  
- Profitability insights  
- Operational efficiency tracking  

---

# 🎓 Academic Context

This project was developed as part of:

**IT3021 – Data Warehousing and Business Intelligence**  
Sri Lanka Institute of Information Technology (SLIIT)

### 👤 Student
**P. M. R. D. Karunarathna**  
BSc (Hons) IT – Data Science Specialization

---

<div align="center">

⭐ If you like this project, consider giving it a star!

</div>
