# Tira E-Commerce Order Management System

## Project Overview

The **Tira E-Commerce Order Management System** is a progressive database design project developed for an e-commerce platform for beauty and personal care products.

The project is developed incrementally through four tasks. Each task builds upon the database structure created in the previous task.

The system is designed to manage customers, products, categories, suppliers, inventory, customer orders, and order details.

---

## Project Objectives

* Analyze the requirements of an e-commerce order management system.
* Design a structured relational database.
* Identify entities, attributes, primary keys, and foreign keys.
* Establish relationships between entities.
* Manage products and categories.
* Manage suppliers and product inventory.
* Manage customer orders and order details.
* Generate useful reports using SQL queries.
* Demonstrate progressive database development.

---

## Technology Used

* **Database:** MySQL
* **Database Design:** ER Diagram
* **ERD Tool:** StarUML
* **Query Language:** SQL
* **Version Control:** Git & GitHub

---

# Task I – Requirement Analysis and Customer Database Module

## Objective

The first task focuses on analyzing the requirements of the Tira E-Commerce Order Management System and designing the Customer module.

## Deliverables

* Software Requirements Specification (SRS)
* Customer Entity
* Customer Attributes
* Customer ER Diagram
* Customer Relational Schema

## Customer Entity

Main attributes include:

* Customer_ID – Primary Key
* Full_Name
* Email
* Mobile_Number
* Password
* Date_Of_Birth
* Gender
* Profile_Image
* Registration_Date
* Account_Status

The SRS defines the functional and non-functional requirements of the complete e-commerce system.

---

# Task II – Product and Category Management System

## Objective

The second task focuses on designing the Product and Category modules.

## Category

Main attributes:

* Category_ID – Primary Key
* Category_Name
* Description

## Product

Main attributes:

* Product_ID – Primary Key
* Product_Name
* Brand
* Category_ID – Foreign Key
* Description
* Ingredients
* Price
* Stock_Quantity
* Skin_Type
* Hair_Type
* Average_Rating
* Product_Image
* Offer_ID – Foreign Key

## Relationship

```text
CATEGORY 1 ───────── M PRODUCT
```

One category can contain many products.

## Operations

* Insert Product
* Update Product
* Delete Product
* Category-wise Product Report

---

# Task III – Supplier and Inventory Management System

## Objective

The third task introduces supplier management and inventory management.

## Supplier

Main attributes:

* Supplier_ID – Primary Key
* Supplier_Name
* Contact_Information

## Product and Supplier Relationship

```text
SUPPLIER 1 ───────── M PRODUCT
```

One supplier can provide many products.

## Inventory Management

Product inventory is managed using:

```text
Stock_Quantity
```

### Inventory Status

**Available**

```text
Stock_Quantity > 0
```

**Unavailable**

```text
Stock_Quantity = 0
```

## Reports

* Available Products
* Out-of-Stock Products
* Supplier Product List

---

# Task IV – Order Management System

## Objective

The fourth task focuses on managing customer orders and order details.

## Orders Table

| Attribute    | Data Type     | Key |
| ------------ | ------------- | --- |
| Order_ID     | INT           | PK  |
| Customer_ID  | INT           | FK  |
| Order_Date   | DATE          |     |
| Total_Amount | DECIMAL(10,2) |     |
| Order_Status | VARCHAR(20)   |     |

## Order_Details Table

| Attribute       | Data Type     | Key |
| --------------- | ------------- | --- |
| Order_Detail_ID | INT           | PK  |
| Order_ID        | INT           | FK  |
| Product_ID      | INT           | FK  |
| Quantity        | INT           |     |
| Unit_Price      | DECIMAL(10,2) |     |

## Relationships

```text
CUSTOMER 1 ───────── M ORDERS

ORDERS 1 ───────── M ORDER_DETAILS

PRODUCT 1 ───────── M ORDER_DETAILS
```

## Operations

* Insert Orders
* Modify Orders
* Generate Customer Order History
* Generate Order Details Report

---

# Complete Database Progression

The project progressively develops the database as follows:

```text
TASK I
Customer
   │
   ▼
TASK II
Customer
Category
Product
   │
   ▼
TASK III
Customer
Category
Product
Supplier
   │
   ▼
TASK IV
Customer
Category
Product
Supplier
Orders
Order_Details
```

---

# Final Core Tables

After Task IV, the core database contains:

```text
CUSTOMER
CATEGORY
SUPPLIER
PRODUCT
ORDERS
ORDER_DETAILS
```

The system can be extended in future tasks with:

```text
PAYMENT
DELIVERY
REVIEW
WISHLIST
SHOPPING_CART
CART_ITEM
OFFER
ADMIN
```

---

# Project Structure

```text
Tira-ECommerce-Order-Management-System/

├── Task-I-Requirement-Analysis/
│   ├── SRS.md
│   ├── Customer-ERD.mdj
│   └── Customer-Relational-Schema.md
│
├── Task-II-Product-Category/
│   ├── Product-Category-ERD.mdj
│   ├── Relational-Schema.md
│   └── task-II.sql
│
├── Task-III-Supplier-Inventory/
│   ├── Supplier-Inventory-ERD.mdj
│   ├── Inventory-Report.md
│   └── task-III.sql
│
├── Task-IV-Order-Management/
│   ├── Order-Management-ERD.mdj
│   ├── Order-Report.md
│   └── task-IV.sql
│
└── README.md
```

---

# Conclusion

The **Tira E-Commerce Order Management System** demonstrates the progressive development of a relational database from requirement analysis and customer management to product, category, supplier, inventory, and order management.

Each task builds upon the previous task, resulting in an integrated database structure suitable for an e-commerce application.

---

## Author

**Priyasree**

**Project:** Tira E-Commerce Order Management System
