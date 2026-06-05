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

<p>
  <img width="50%" alt="snowflake-schema" src="https://github.com/user-attachments/assets/28600c4f-79cc-46c8-aae5-ee7c31a5c531" />
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

<table>
  <tr>
    <td align="center">
      <img width="576" height="611" alt="Extract" src="https://github.com/user-attachments/assets/ff19f2d6-925f-4a40-a2f3-76baa5c9fce4" /><br>
      <sub><b>Extract Phase</b>: Data is extracted from Excel, text files, and SQL sources.</sub>
    </td>
    <td align="center">
      <img width="603" height="559" alt="Transform-Load" src="https://github.com/user-attachments/assets/fb8f6c75-fc8d-4d88-89a1-8e1f60190536" /><br>
      <sub><b>Transform & Load Phase</b>: Data is cleaned, transformed, and loaded into the warehouse.</sub>
    </td>
  </tr>
</table>

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

<p>
  <img width="50%" alt="cube-hierarchy" src="https://github.com/user-attachments/assets/e8cd66d8-ec68-47fe-b2ba-1c76be1c0a8a" />
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

### 📌 Report 1 – Matrix Analysis

- Product-wise sales by year  
- Performance comparison  

### 📌 Report 2 – Geographic Analysis

- Cascading slicers (Country → City → Address)
- Map visualization
- Line chart trends
- Donut chart distribution

### 📌 Report 3 – Drill-Down Analysis

- Category → Product → Time hierarchy
- Interactive exploration

## 📌 Report 4 – Drill-Through Dashboard

Deep-dive analytics view

<p>
  <img width="50%" alt="powerbi-dashboard" src="https://github.com/user-attachments/assets/3405f228-ccae-4b98-8ed4-48e490e184ff" />
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
