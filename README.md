# supply_chain_sql 

## Overview
The Supply Chain Optimization project is designed to manage and analyze various aspects of **supply chain operations**. This project uses a relational database to store and manage data related to suppliers, products, orders, order details, and shipments. The SQL file provided sets up the necessary tables and populates them with sample data.

## Project Structure
The SQL file contains the following main sections:

## Database Creation
Table Creation
Data Insertion
Database Schema
Tables

Suppliers

- *supplier_id* (INT, Primary Key)
- *supplier_name* (VARCHAR)
- *contact_person* (VARCHAR)
- *phone_number* (VARCHAR)
- *email* (VARCHAR)

Products

- *product_id* (INT, Primary Key)
- *product_name* (VARCHAR)
- *description* (TEXT)
- *unit_price* (DECIMAL)
- *supplier_id* (INT, Foreign Key to Suppliers)

Orders

- *order_id* (INT, Primary Key)
- *order_date* (DATE)
- *supplier_id* (INT, Foreign Key to Suppliers)
- *total_amount* (DECIMAL)

OrderDetails

- *order_detail_id* (INT, Primary Key)
- *order_id* (INT, Foreign Key to Orders)
- *product_id* (INT, Foreign Key to Products)
- *quantity* (INT)
- *unit_price* (DECIMAL)
- *total_price* (DECIMAL)

Shipments

- *shipment_id* (INT, Primary Key)
- *order_id* (INT, Foreign Key to Orders)
- *shipment_date* (DATE)
- *delivery_date* (DATE)
- *status* (VARCHAR)
