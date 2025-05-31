# Data Warehouse Naming Conventions and General Principles

## General Principles

- **Naming Style**: Use `snake_case` with lowercase letters and underscores (`_`) to separate words.
- **Language**: Use **English** for all object and column names.
- **Avoid Reserved Words**: Never use SQL reserved keywords (e.g., `select`, `order`, `from`) as object or column names.

---

## Table Naming Conventions

### Bronze Layer

- **Format**: `<source_system>_<entity>`
- **Rules**:
  - Must start with the source system name (e.g., `crm`, `erp`).
  - Table names must match their original source names — no renaming.
- **Example**:
  - `crm_customer_info` → Raw customer data from CRM system.
  - `erp_sales_detail` → Raw sales data from ERP system.

### Silver Layer

- **Format**: `<source_system>_<entity>`
- **Rules**:
  - Also starts with the source system name (e.g., `crm`, `erp`).
  - Table names remain identical to the original source.
  - Used for cleaned and transformed data.
- **Example**:
  - `crm_customer_info` → Cleaned customer information.
  - `erp_product_data` → Cleaned product data from ERP.

### Gold Layer

- **Format**: `<category>_<entity>`
- **Rules**:
  - Table names must be **meaningful** and **business-aligned**.
  - Use standard prefixes to indicate table type:
    - `dim_` for dimension tables
    - `fact_` for fact tables
    - `report_` for reporting tables
- **Examples**:
  - `dim_customers` → Dimension table for customer data.
  - `fact_sales` → Fact table for sales transactions.
  - `report_sales_monthly` → Report table summarizing monthly sales.

---

## Glossary of Category Prefixes

| Prefix     | Meaning            | Example(s)                  |
|------------|--------------------|-----------------------------|
| `dim_`     | Dimension table     | `dim_customer`, `dim_product` |
| `fact_`    | Fact table          | `fact_sales`               |
| `report_`  | Report table        | `report_sales_monthly`     |

---

## Column Naming Conventions

### Surrogate Keys

- **Format**: `<entity>_key`
- **Usage**:
  - Used as primary keys in dimension tables.
- **Example**:
  - `customer_key` → Surrogate key in `dim_customers`.
  - `product_key` → Surrogate key in `dim_products`.

### Technical Columns

- **Format**: `dwh_<column_name>`
- **Usage**:
  - Used for system-generated metadata.
- **Examples**:
  - `dwh_load_date` → Date when the record was loaded into the warehouse.
  - `dwh_update_user` → User/system that updated the record.

---
