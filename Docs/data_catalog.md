📊 Data Catalog – Gold Layer
The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of dimension tables and fact tables that provide high-quality, curated information optimized for decision-making and BI tools.

1. gold.dim_customers
Purpose: Stores customer details enriched with demographic and geographic data.

Column Name	Data Type	Description
customer_key	INT	Surrogate key uniquely identifying each customer record.
customer_id	INT	Unique numerical identifier assigned to each customer.
customer_number	NVARCHAR(50)	Alphanumeric identifier used for customer tracking.
first_name	NVARCHAR(50)	Customer's first name.
last_name	NVARCHAR(50)	Customer's last/family name.
country	NVARCHAR(50)	Country of residence (e.g., 'Germany', 'United States').
marital_status	NVARCHAR(50)	Customer's marital status (e.g., 'Married', 'Single').
gender	NVARCHAR(50)	Gender of the customer (e.g., 'Male', 'Female', 'n/a').
birthdate	DATE	Customer's date of birth (e.g., 1971-10-06).
create_date	DATE	Timestamp of when the customer was created in the system.

2. gold.dim_products
Purpose: Provides enriched product details and classification data.

Column Name	Data Type	Description
product_key	INT	Surrogate key uniquely identifying each product.
product_id	INT	Unique identifier for internal product tracking.
product_number	NVARCHAR(50)	Alphanumeric code representing the product.
product_name	NVARCHAR(50)	Descriptive name of the product.
category_id	NVARCHAR(50)	Identifier for product's top-level category.
category	NVARCHAR(50)	Broad product category (e.g., 'Bikes').
subcategory	NVARCHAR(50)	Sub-category of the product (e.g., 'Road Bikes').
maintenance_required	NVARCHAR(50)	Indicates if maintenance is required (e.g., 'Yes', 'No').
cost	INT	Base cost of the product in monetary units.
product_line	NVARCHAR(50)	Product series or line (e.g., 'Mountain', 'Urban').
start_date	DATE	Product availability start date.

3. gold.fact_sales
Purpose: Stores transactional sales data used for metrics, reporting, and analysis.

Column Name	Data Type	Description
order_number	NVARCHAR(50)	Unique alphanumeric identifier for the sales order (e.g., SO54496).
product_key	INT	Surrogate key referencing dim_products.
customer_key	INT	Surrogate key referencing dim_customers.
order_date	DATE	Date the order was placed.
shipping_date	DATE	Date the order was shipped.
due_date	DATE	Payment due date for the order.
sales_amount	INT	Total monetary value of the sale.
quantity	INT	Number of units sold.
price	INT	Price per unit of product.
