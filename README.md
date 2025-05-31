# SQL Data Warehouse & Analytics Project 🚀

Welcome to the **Data Warehouse and Analytics Project** repository!

This project demonstrates a comprehensive data warehousing and analytics solution—from building a data warehouse to generating actionable insights. Designed as a portfolio project, it highlights industry best practices in data engineering and analytics.

---

## 🏗️ Data Architecture

The data architecture follows the **Medallion Architecture** with three core layers:
![image](https://github.com/user-attachments/assets/1ce871ee-9b86-46eb-8027-48e56f542c02)


### 🔹 Bronze Layer
- Stores raw data as-is from source systems.
- Ingests data from CSV files into SQL Server.

### 🔸 Silver Layer
- Performs data cleansing, standardization, and normalization.
- Prepares data for analysis.

### 🟡 Gold Layer
- Contains business-ready, analytical data.
- Structured into a **star schema** for reporting and analytics.

---

## 📖 Project Overview

This project involves:

- **Data Architecture**: Building a modern data warehouse using Bronze, Silver, and Gold layers.
- **ETL Pipelines**: Extracting, transforming, and loading data from CSV (ERP & CRM) into SQL Server.
- **Data Modeling**: Developing fact and dimension tables optimized for analytical queries.
- **Analytics & Reporting**: Writing SQL reports and dashboards to derive business insights.

---

## 🎯 Ideal For

This repository is an excellent resource for:

- SQL Developers
- Data Engineers
- ETL Pipeline Developers
- Data Modelers
- Data Analysts
- Students & Job Seekers in Data Roles

---

## 🛠️ Tools & Resources

Everything is free to use! Key tools include:

- **Datasets**: ERP and CRM CSV files
- **SQL Server Express**: Lightweight development server
- **SQL Server Management Studio (SSMS)**: GUI for SQL development
- **Git & GitHub**: Version control and collaboration
- **Draw.io**: Design diagrams and architecture
- **Notion**: Get the full project plan and templates

---

## 🚀 Project Requirements

### 📌 Data Engineering Phase

**Objective:**  
Develop a modern data warehouse to consolidate ERP & CRM data for business reporting.

**Specifications:**
- **Data Sources**: ERP and CRM data (CSV)
- **Data Quality**: Clean and fix quality issues
- **Integration**: Unified, user-friendly data model
- **Scope**: Use latest dataset only (no historization)
- **Documentation**: Clear data model docs for business and analytics teams

---

### 📊 Data Analytics Phase

**Objective:**  
Develop SQL-based insights into:

- Customer Behavior
- Product Performance
- Sales Trends

These help stakeholders make **data-driven decisions**.

More details can be found in `docs/requirements.md`.

---

## 📂 Repository Structure

data-warehouse-project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation and architecture details
│   ├── etl.drawio                      # Draw.io file shows all different techniquies and methods of ETL
│   ├── data_architecture.drawio        # Draw.io file shows the project's architecture
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── data_flow.drawio                # Draw.io file for the data flow diagram
│   ├── data_models.drawio              # Draw.io file for data models (star schema)
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository
├── .gitignore                          # Files and directories to be ignored by Git
└── requirements.txt                    # Dependencies and requirements for the project
