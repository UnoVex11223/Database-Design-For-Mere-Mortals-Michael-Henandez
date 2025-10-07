## Database Fundamentals

A **database** is an organized collection of data used to model an organization or an organizational process.

***

### Types of Databases

There are two primary types of databases: operational and analytical.

* **Operational Database**
    * Used for **OLTP** (Online Transaction Processing), which involves managing day-to-day transactions.
    * The data is **dynamic** and changes frequently (e.g., a database for an e-commerce store's inventory and sales).

* **Analytical Database**
    * Used for **OLAP** (Online Analytical Processing), which involves analyzing historical data for business intelligence. 
    * The data is **static**, meaning it's a snapshot in time and doesn't change.
    * Often uses data from one or more operational databases as its source.

***

## The Relational Database Model

A **relational database** is a type of database that stores data in relations, which are visually represented as tables with rows and columns.

### Key Advantages

1.  **Built-in Multilevel Integrity**
    * **Entity Integrity**: Ensures every record is unique, identified by a **primary key**.
    * **Referential Integrity**: Maintains consistency between related tables using **foreign keys**.
    * **Domain Integrity**: Enforces correct data types and formats in columns to ensure accuracy.

2.  **Logical and Physical Data Independence**
    * **Logical**: The database schema (its structure) can be changed without affecting the applications that use it.
    * **Physical**: The physical storage location of the data can be changed without affecting the applications.

3.  **Guaranteed Data Consistency and Accuracy**
    * This is ensured by the **ACID** properties (Atomicity, Consistency, Isolation, Durability), which govern how transactions are processed.

4.  **Easy Data Retrieval**
    * Uses **SQL (Structured Query Language)**, a powerful and intuitive language that allows users to easily access and manipulate data. 
