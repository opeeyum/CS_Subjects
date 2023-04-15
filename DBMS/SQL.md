## What are different types of SQL statements?
- SQL (Structured Query Language) is a programming language used to manage and manipulate relational databases. There are several types of SQL statements, including:

  1. **Data Definition Language (DDL)**: These statements are used to create, modify, and delete database objects such as tables, indexes, and views. Some common DDL statements include CREATE, ALTER, and DROP.

  2. **Data Manipulation Language (DML)**: These statements are used to insert, update, and delete data in a database. Some common DML statements include SELECT, INSERT, UPDATE, and DELETE.

  3. **Data Control Language (DCL)**: These statements are used to control access to the database and its objects. Some common DCL statements include GRANT and REVOKE.

  4. **Transaction Control Language (TCL)**: These statements are used to control transactions in a database. Some common TCL statements include COMMIT, ROLLBACK, and SAVEPOINT.

  5. **Data Query Language (DQL)**: This is a subset of DML that is used specifically for retrieving data from a database. The most common DQL statement is SELECT, which is used to query a database and retrieve data from one or more tables.

- Each type of SQL statement serves a specific purpose and is used in different scenarios depending on the requirements of the application or database. By using these statements in combination, developers can build powerful applications and manage large amounts of data efficiently.

## What is the priority of sql clause while execution?
- The priority of SQL clauses during execution is determined by the logical query processing order. SQL is processed in a specific order, which defines how the various clauses in a query are executed. Here's the logical query processing order:

  1. **FROM** clause: specifies the tables or views to be queried.
  2. **JOIN** clause: used to join tables together.
  3. **WHERE** clause: specifies the conditions that must be met for a row to be returned.
  4. **GROUP BY** clause: groups the result set by one or more columns.
  5. **HAVING** clause: specifies the conditions that must be met for a group of rows to be returned.
  6. **SELECT** clause: specifies the columns to be returned.
  7. **DISTINCT** clause: removes duplicates from the result set.
  8. **ORDER BY** clause: sorts the result set based on one or more columns.
- It's important to note that not all clauses are required in a query, and some clauses may be optional or interchangeable depending on the query. The logical query processing order is simply a guideline for understanding how SQL processes a query.

- Also, it's worth noting that some database management systems may optimize query execution by reordering the clauses based on the available indexes, statistics, and other factors. However, the logical query processing order still provides a useful framework for understanding the order in which SQL processes a query.

## What will be priority of sub query in the main query?
- In SQL, a subquery is a query that is nested inside another query. The priority of a subquery in the main query depends on where the subquery is located in the main query.

- If a subquery is used in the **SELECT**, ***WHERE**, or **HAVING** clause of the main query, it will be executed before the main query. The result of the subquery will then be used as input for the main query.

- For example, consider the following query that uses a subquery in the WHERE clause:

  ```sql
  Copy code
  SELECT *
  FROM orders
  WHERE customer_id IN (
      SELECT customer_id
      FROM customers
      WHERE country = 'USA'
  );
  ```
- In this query, the subquery **`SELECT customer_id FROM customers WHERE country = 'USA'`** is executed first, and returns a list of customer IDs who are located in the USA. This list is then used as input for the main query, which selects all orders from those customers.

- If a subquery is used in the FROM clause of the main query, it will be executed first and the result will be treated as a temporary table. The main query will then be executed against this temporary table.

- For example, consider the following query that uses a subquery in the FROM clause:

  ```sql
  Copy code
  SELECT *
  FROM (
      SELECT customer_id, COUNT(*) as num_orders
      FROM orders
      GROUP BY customer_id
  ) AS order_counts
  WHERE num_orders > 10;
  ```
- In this query, the subquery **`SELECT customer_id, COUNT(*) as num_orders FROM orders GROUP BY customer_id`** is executed first, and returns a temporary table **`order_counts`** that shows the number of orders for each customer. The main query then selects all rows from order_counts where the number of orders is greater than 10.

- So the priority of a subquery in the main query depends on where it is used. If it is used in the SELECT, WHERE, or HAVING clause, it will be executed before the main query. If it is used in the FROM clause, it will be executed first and the result will be treated as a temporary table.

## What is the difference between executing before main query and executing first?
- When a subquery is executed before the main query, it means that the subquery is executed first and its result is then used as input for the main query. The subquery is executed once for each row in the main query, and the result of the subquery is used to filter, join or aggregate the data in the main query.

- When a subquery is executed first, it means that the subquery is used to create a temporary table, and the main query is then executed against this temporary table. The subquery is executed only once, and its result is stored in a temporary table that is used by the main query.

- The main difference between these two approaches is how the subquery results are used in the main query. When a subquery is executed before the main query, the subquery is used to filter, join or aggregate the data in the main query. This approach is useful when you want to select data from multiple tables, or when you want to perform complex filtering or aggregation.

- On the other hand, when a subquery is executed first, the main query is executed against a temporary table that contains the results of the subquery. This approach is useful when you want to simplify a complex query, or when you want to reuse the results of a subquery in multiple queries.

- In general, the approach you choose depends on the complexity of your query and the performance requirements of your application. In some cases, executing the subquery before the main query may be more efficient, while in other cases, executing the subquery first may be more efficient.

### Consider following query, there dependency in sub query with main, 
  ```sql
  SELECT *
  FROM customers
  WHERE EXISTS (SELECT * FROM orders WHERE orders.customer_id = customers.customer_id);
  ```
  What will be the execution order?
- In this query, the subquery is dependent on the main query, since it uses a column from the main query in its **`WHERE`** clause. Therefore, the execution order will be as follows:

  1. The main query will be executed first, selecting all rows from the "customers" table.

  2. For each row in the "customers" table, the subquery will be executed to check if there are any orders associated with that customer. If the subquery returns at least one row, the row from the "customers" table will be included in the result set.

  3. Once all rows from the "customers" table have been processed, the result set will be returned to the user.

> **Note**: That the subquery will be executed once for each row in the "customers" table, so if there are a large number of customers, the query may take a significant amount of time to execute. It is generally a good practice to optimize queries with subqueries to avoid this type of performance issue.
