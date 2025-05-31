# 📘 Gold Layer – Data Catalog

The **Gold Layer** is the business-level data model designed for analytics and reporting. It consists of cleanly structured **dimension** and **fact** views that provide a denormalized and enriched representation of your data.

---

## 📁 gold.dim_customers

**Purpose:** Stores customer details enriched with demographic and geographic data.

| Column Name       | Data Type      | Description                                                                 |
|-------------------|----------------|-----------------------------------------------------------------------------|
| `customer_key`    | `INT`          | Surrogate key uniquely identifying each customer record.                    |
| `customer_id`     | `INT`          | Unique numerical identifier assigned to each customer.                      |
| `customer_number` | `NVARCHAR(50)` | Alphanumeric identifier used to track the customer.                         |
| `first_name`      | `NVARCHAR(50)` | First name of the customer.                                                 |
| `last_name`       | `NVARCHAR(50)` | Last name (surname) of the customer.                                        |
| `country`         | `NVARCHAR(50)` | Country of residence (e.g., 'Germany').                                     |
| `marital_status`  | `NVARCHAR(50)` | Marital status (e.g., 'Married', 'Single').                                 |
| `gender`          | `NVARCHAR(50)` | Gender of the customer (e.g., 'Male', 'Female', 'n/a').                     |
| `birthdate`       | `DATE`         | Date of birth (e.g., `1971-10-06`).                                         |
| `create_date`     | `DATE`         | Timestamp when the customer was created in the system.                      |

---

## 📁 gold.dim_products

**Purpose:** Provides product master data including classification and cost information.

| Column Name            | Data Type      | Description                                                                 |
|------------------------|----------------|-----------------------------------------------------------------------------|
| `product_key`          | `INT`          | Surrogate key uniquely identifying each product.                            |
| `product_id`           | `INT`          | Unique identifier for the product.                                          |
| `product_number`       | `NVARCHAR(50)` | Alphanumeric code used to track the product.                                |
| `product_name`         | `NVARCHAR(50)` | Full name of the product.                                                   |
| `category_id`          | `NVARCHAR(50)` | Identifier linking to product's category.                                   |
| `category`             | `NVARCHAR(50)` | Broad classification (e.g., 'Bikes').                                       |
| `subcategory`          | `NVARCHAR(50)` | Sub-category of the product (e.g., 'Mountain Bikes').                       |
| `maintenance_required` | `NVARCHAR(50)` | Indicates if maintenance is required (e.g., 'Yes', 'No').                   |
| `cost`                 | `INT`          | Base cost of the product.                                                   |
| `product_line`         | `NVARCHAR(50)` | Series or line to which the product belongs (e.g., 'Road').                 |
| `start_date`           | `DATE`         | Date when the product became available.                                     |

---

## 📁 gold.fact_sales

**Purpose:** Stores transactional sales data used for analysis and KPI tracking.

| Column Name     | Data Type      | Description                                                                 |
|------------------|----------------|-----------------------------------------------------------------------------|
| `order_number`   | `NVARCHAR(50)` | Unique alphanumeric sales order ID (e.g., `SO54496`).                       |
| `product_key`    | `INT`          | Foreign key to `dim_products`.                                              |
| `customer_key`   | `INT`          | Foreign key to `dim_customers`.                                             |
| `order_date`     | `DATE`         | Date when the order was placed.                                             |
| `shipping_date`  | `DATE`         | Date when the order was shipped.                                            |
| `due_date`       | `DATE`         | Payment due date.                                                           |
| `sales_amount`   | `INT`          | Total value of the sale.                                                    |
| `quantity`       | `INT`          | Quantity of products sold.                                                  |
| `price`          | `INT`          | Price per unit of the product.                                              |

