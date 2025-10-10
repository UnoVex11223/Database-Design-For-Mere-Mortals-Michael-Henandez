# Relational Database Terminology

Understanding the correct terminology is essential for working with relational databases. This vocabulary is the foundation for expressing ideas, defining design processes, and discussing database concepts professionally.

***

## The Importance of Terminology

A shared vocabulary is crucial because it is used to:
1.  Express and define the special ideas and rules of the relational model.
2.  Communicate and define the steps of the database design process.
3.  Effectively discuss any topic related to a relational database or RDBMS.

## Four Categories of Terminology

The terms used in database design can be grouped into four main categories:

* **Value-Related**: Terms describing the data and values stored.
* **Structure-Related**: Terms describing the objects that hold the data.
* **Relationship-Related**: Terms describing how different structures are linked.
* **Integrity-Related**: Terms describing the rules that maintain data quality.

***

## Value-Related Terms

* **Data**: The raw values stored in the database.
* **Information**: Data that has been processed in a way that makes it meaningful and gives it context.
* **Null**: A condition representing a **missing or unknown value**. It is important to remember that a `NULL` is not the same as zero (`0`) or an empty string. Any mathematical operation involving a `NULL` will always result in `NULL`.

***

## Structure-Related Terms

* **Table**: The primary structure in a database, composed of records (rows) and fields (columns). A well-designed table always represents a **single, specific subject**, which can be an object (like a *Customer*) or an event (like a *Sale*).
    * **Data Table**: A table that stores the primary data used to supply information (e.g., an *Employees* table).
    * **Validation Table (Lookup Table)**: A table that stores a predefined set of values used to enforce data integrity (e.g., a *States* table with a list of all valid state abbreviations).

* **Field (Attribute)**: A characteristic or descriptor of the table's subject. Each field in a table contains a specific piece of data about that subject (e.g., `FirstName`, `HireDate`).
    * **Poor Field Design**:
        * **Multipart Field**: A field that contains two or more distinct items (e.g., storing a full name "John Smith" instead of in `FirstName` and `LastName` fields).
        * **Multivalued Field**: A field that contains multiple instances of the same type of value (e.g., storing multiple phone numbers in a single `PhoneNumber` field).
        * **Calculated Field**: A field that stores a value derived from other fields, which is generally discouraged as it can be calculated on the fly in a query.

* **Record (Tuple)**: A unique instance of the subject of a table, represented as a row.

* **View**: A **virtual table** composed of fields selected from one or more underlying tables (known as **base tables**). Views are important for three reasons:
    1.  They allow you to work with data from multiple tables as if it were a single table.
    2.  They can be used to restrict user access, preventing them from viewing or modifying certain fields.
    3.  They can be used to implement data integrity rules (a validation view).

* **Index**: A special data structure that the RDBMS uses to find records more quickly, improving the performance of data processing operations. 📈

***

## Relationship & Integrity Related Terms

### Keys 
* **Key**: A special field (or combination of fields) that serves a specific role within a table.
* **Primary Key (PK)**: A field whose value **uniquely identifies** every single record in a table. Its value can never be `NULL`.
* **Foreign Key (FK)**: A field in one table that is a primary key in another table. It is used to establish a **relationship** between the two tables.

### Relationships 
* **Relationship**: An association between two tables where records in one table are linked to records in another. This is established using primary and foreign keys.
    * **One-to-One (1:1)**: A single record in one table is related to, at most, one record in the second table.
    * **One-to-Many (1:N)**: A single record in one table can be related to zero, one, or many records in the second table.
    * **Many-to-Many (M:N)**: A record in one table can be related to many records in a second table, and a record in the second table can be related to many in the first. This is implemented using a third, intermediate table called a **linking table** or **associative table**.

* **Relationship Participation**: Defines whether a record must exist in one table before it can exist in another.
    * **Mandatory**: A record must be entered into Table A before you can enter a related record in Table B.
    * **Optional**: You are not required to enter a record in Table A before adding a record in Table B.

* **Orphaned Record**: A record in a child table that does not have a valid, corresponding record in its parent table. This is a state of poor data integrity.

### Data Integrity
* **Data Integrity**: The overall validity, consistency, and accuracy of the data within a database.
* **Field Specification (Domain)**: Defines all the properties of a field.
    * **General Elements**: The most fundamental attributes of the field (e.g., field name).
    * **Physical Elements**: How the field is built and stored by the RDBMS (e.g., data type, length).
    * **Logical Elements**: The rules that describe the values stored in the field (e.g., required value, default value, range of valid entries).
