# Chapter Summary: Database Design Methodology

This chapter emphasizes the critical importance of implementing a proper **database design methodology**. A structured approach ensures that the resulting database is efficient, scalable, and accurately models the real-world processes it is intended to support.

***

## Traditional Database Design Phases

The traditional methodology is broken down into three core phases:

### 1. Requirements Analysis
* **Goal**: To understand and document the needs of the end-users.
* **Process**: This phase involves interviewing stakeholders, analyzing existing systems (if any), and defining the specific data that needs to be stored and the operations that will be performed on it. The output is a clear set of requirements that will guide the design.

### 2. Data Modeling
* **Goal**: To create a conceptual representation of the data.
* **Process**: This involves creating an **Entity-Relationship Diagram (ERD)** to visually represent the main entities (e.g., Customers, Products, Orders), their attributes (e.g., Name, Price), and the relationships between them. This model acts as a blueprint for the database.

### 3. Normalization
* **Goal**: To organize the data in the database to reduce redundancy and improve data integrity.
* **Process**: This is a formal process of applying a series of rules (called **normal forms**) to the data model. By eliminating duplicate data, normalization helps prevent data anomalies and ensures that the database is structured efficiently.
