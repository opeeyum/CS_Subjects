## Relational model

### Cardinalty of a Relation
- In the context of Relational Database Management Systems (RDBMS), the cardinality of a table refers to the number of rows (also known as records or tuples) in that table. In other words, it is a measure of the table's size and represents the number of distinct entities or instances that the table represents.

- For example, if we have a table called "Customers" that stores information about all the customers of a business, the cardinality of this table would be the total number of customers in the database, which would be equal to the number of rows in the "Customers" table.

- The cardinality of a table is an important factor in database design and optimization, as it affects the performance of queries and operations on the table. Tables with a large cardinality may require more resources to query and update, and may benefit from indexing or partitioning to improve performance.

### Degree of a Relation
- In the context of Relational Database Management Systems (RDBMS), the degree of a table refers to the number of columns (also known as attributes or fields) in that table. In other words, it is a measure of the table's width and represents the number of distinct properties or characteristics that the table represents for each row.

- For example, if we have a table called "Customers" that stores information about all the customers of a business, the degree of this table would be the total number of columns in the table, such as "CustomerID", "Name", "Address", "Phone", and so on.

- The degree of a table is also an important factor in database design and optimization, as it affects the storage requirements and performance of queries and operations on the table. Tables with a large degree may require more storage space and processing power to handle queries and updates, and may benefit from normalization or denormalization to optimize for specific use cases.

### Constraint in RDBMS
- Constraints in Relational Database Management Systems (RDBMS) are used to enforce rules and restrictions on the data that can be stored in tables. These constraints ensure that the data is accurate, consistent, and follows certain rules or business logic. Here are some common types of constraints in RDBMS:

  1. **Primary Key Constraint**: A primary key constraint ensures that each row in a table is uniquely identifiable by a specific column or set of columns. This constraint is used to enforce data integrity and to prevent duplicates.

  2. **Foreign Key Constraint**: A foreign key constraint establishes a relationship between two tables by linking a column in one table to the primary key of another table. This constraint ensures referential integrity between the tables and can be used to enforce business rules, such as ensuring that a customer cannot be assigned to a non-existent sales region.

  3. **Unique Constraint**: A unique constraint ensures that each value in a column or set of columns is unique across all rows in the table. This constraint is similar to a primary key, but it does not require the column(s) to be the table's primary key.

  4. **Check Constraint**: A check constraint specifies a condition that must be true for each row in a table. This constraint can be used to enforce business rules or data validation, such as ensuring that a birthdate column contains a valid date value.

  5. **Not Null Constraint**: A not null constraint ensures that a column cannot contain null values. This constraint is used to enforce data integrity and to ensure that required data is always present in the table.

  6. **Default Constraint**: A default constraint specifies a default value for a column that is used when a row is inserted and the column is not specified. This constraint is used to simplify data entry and to ensure that a default value is always present when no other value is specified.

### What is key, super key, primary key, candidate key and alternate key in rdbms?
- In Relational Database Management Systems (RDBMS), a key is a set of one or more columns that uniquely identify each row in a table. There are several types of keys in RDBMS, including super keys, candidate keys, primary keys, and alternate keys:

  1. **Super Key**: A super key is any combination of one or more columns that uniquely identifies each row in a table. A super key can have more columns than necessary to uniquely identify each row, and it can include non-key columns as well.

  2.  **Candidate Key**: A candidate key is a minimal super key, which means that it is a set of columns that can uniquely identify each row in a table, and no subset of these columns can also uniquely identify each row. In other words, a candidate key is a key that cannot be further reduced without losing the ability to uniquely identify each row.

  3. **Primary Key**: A primary key is a specific candidate key that is chosen as the main key for a table. It is the key that is used to establish relationships with other tables, and it is used to enforce data integrity and prevent duplicate rows. A primary key must be unique, non-null, and immutable.

  4. **Alternate Key**: An alternate key is a candidate key that is not chosen as the primary key for a table. It can be used as a unique identifier for a table, and it can be used to establish relationships with other tables.

  - **Can we say that candidate key is set of minimal super keys?**
    - Yes, we can say that a candidate key is a set of minimal super keys that can uniquely identify each row in a table.

## Normalization
- Normalization is the process of organizing the data in a relational database management system (RDBMS) in a way that reduces redundancy and ensures data integrity. It involves dividing a large table into smaller tables and defining relationships between them.

- Normalization is important in RDBMS because it helps to minimize data duplication, which can lead to inconsistencies and inaccuracies. By dividing data into smaller tables and linking them with foreign keys, we can eliminate redundant data and ensure that each piece of information is stored in only one place.

- Normalization is typically divided into several normal forms, each of which represents a higher level of normalization than the previous one. The most commonly used normal forms are:

  1. First Normal Form (1NF): This involves ensuring that each table has a primary key and that each column contains atomic values.

  2. Second Normal Form (2NF): This involves ensuring that each non-key column in a table is functionally dependent on the entire primary key.

  3. Third Normal Form (3NF): This involves ensuring that each non-key column in a table is functionally dependent only on the primary key and not on any other non-key columns.

  - There are additional normal forms beyond 3NF, such as Boyce-Codd Normal Form (BCNF) and Fourth Normal Form (4NF), but they are less commonly used in practice.

- In summary, normalization is the process of organizing data in a way that reduces redundancy and ensures data integrity. It involves dividing large tables into smaller ones and defining relationships between them, according to specific normal forms.

## What is functional dependency?
- Functional dependency is a relationship between two attributes (columns) in a relational database, where the value of one attribute determines the value of another attribute. In other words, if we know the value of one attribute, we can determine the value of the other attribute.

- For example, consider a table of customer information with two attributes: "Customer ID" and "Customer Name." If we know the value of the "Customer ID" attribute, we can determine the value of the "Customer Name" attribute. In this case, we say that "Customer Name" is functionally dependent on "Customer ID."

- Functional dependencies are important in relational database design because they help to ensure data integrity and reduce redundancy. By identifying functional dependencies between attributes, we can eliminate redundant data and ensure that each piece of information is stored in only one place.

- Functional dependencies are typically represented using arrows, where the arrow points from the determining attribute to the dependent attribute. For example, we would represent the functional dependency between "Customer ID" and "Customer Name" as follows: Customer ID → Customer Name.

- Functional dependencies are also used in the process of normalization, which involves dividing large tables into smaller ones and ensuring that each table meets a specific normal form. For example, the process of Third Normal Form (3NF) requires that each non-key attribute in a table is functionally dependent only on the primary key, and not on any other non-key attributes.








