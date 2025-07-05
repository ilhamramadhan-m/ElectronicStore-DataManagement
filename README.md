# 🛍️ Smart Inventory & Transaction Management for Wisantoko Electronic Store

## 📌 Background

In today’s fast-paced retail environment, efficient information management is key to operational success. **Wisantoko Electronic Store**, like many small-to-medium businesses, faced challenges in handling product inventory and transaction data. Customers often encountered delays due to disorganized stock information and limited access to real-time product details.

To address these issues, this project implements a structured **relational database system using MySQL**, aiming to optimize store operations, enhance the customer experience, and streamline internal processes like stock management and invoicing.

## 🛠 Methodology

The project development includes the following stages:

1. **Needs Analysis**: Identify bottlenecks in current operations such as stock lookup delays and transaction inefficiencies.
2. **Database Design & Normalization**:

   * Design entities based on store operations: Customers, Products, Membership, Shipping, Payments, etc.
   * Apply **1NF, 2NF, and 3NF** normalization to reduce redundancy and ensure data integrity.
3. **ERD & Relational Schema Construction**:

   * Model complex **Many-to-Many** relationships using junction tables like `DetailTransaksi`.
   * Implement **One-to-Many** relationships among key entities (e.g., Membership → Customer).
4. **Trigger Implementation**:

   * Auto-update stock on purchase or restock.
   * Maintain inventory consistency (e.g., trigger auto-replenish if stock < 20).
5. **Stored Procedures**:

   * `generate_invoice` & `generate_invoice_pertransaction`: Generate complete transactional receipts.
   * `calculate_subtotal`: Compute total price including discount, shipping, and membership benefits.
6. **Advanced SQL Queries**:

   * Identify **most and least sold products**, and track **monthly sales trends**.
   * Filter product sales by specific month on request.

## 📊 Key Features & Results

* **Real-Time Inventory Update**: Stock is auto-reduced on purchase and replenished if understocked.
* **Comprehensive Invoicing System**: Aggregated invoices including fees, discounts, and shipping.
* **Sales Insights**:

  * Most sold product: *Samsung Upright Vacuum Cleaner – Orange Sunset*.
  * Least sold category: *Refrigerators*.
  * Detailed monthly sales per product and per transaction.
* **Data Normalization Benefits**: Avoid redundancy and allow scalable data management.
* **Custom Procedures & Triggers**: Reduce manual input, automate routine calculations, and prevent inconsistencies.

## 📦 Technologies Used

* **Database**: MySQL
* **Data Design**: Entity-Relationship Diagram (ERD), Normal Forms
* **SQL Features**: Views, Stored Procedures, Triggers, Joins, Grouping, Conditional Queries

## 🔍 Example Use Cases

* A cashier enters a new transaction — the system:

  * Deducts stock,
  * Calculates subtotal including discounts,
  * Adds shipping cost & payment interest based on membership,
  * Generates an invoice for the customer in a single row.
* Management views a report of all products sold this month, identifies low-performing products, and triggers a stock restock operation.

## 📎 Data Access

🔗 [Raw Dataset & SQL Scripts (ITS Cloud)](https://github.com/ilhamramadhan-m/ElectronicStore-DataManagement/blob/main/Electronic%20Store's%20Selling%20RDBMS.xlsx)
