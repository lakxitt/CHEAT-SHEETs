# 🗄️ SQL Cheat Sheet

> A comprehensive SQL Cheat Sheet covering syntax, database operations, queries, joins, functions, constraints, indexes, transactions, views, and best practices.

![SQL](https://img.shields.io/badge/Database-SQL-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Made With](https://img.shields.io/badge/Made%20With-Markdown-orange)

---

# 📖 Table of Contents

- SQL Basics
- Database Commands
- Table Commands
- Data Types
- CRUD Operations
- Filtering Data
- Sorting
- Limiting Results
- Aggregate Functions
- GROUP BY
- HAVING
- Joins
- Set Operators
- Constraints
- Keys
- Views
- Indexes
- Transactions
- Stored Procedures
- Triggers
- Common Functions
- CASE Statements
- Date Functions
- String Functions
- Math Functions
- Window Functions
- Subqueries
- CTE (WITH)
- Best Practices

---

# What is SQL?

**SQL (Structured Query Language)** is the standard language used to communicate with relational databases.

Popular databases include:

- MySQL
- PostgreSQL
- SQLite
- Microsoft SQL Server
- Oracle Database
- MariaDB

---

# SQL Syntax

```sql
SELECT column_name
FROM table_name
WHERE condition;
```

---

# Comments

```sql
-- Single line comment

/*
Multi-line
comment
*/
```

---

# Database Commands

## Create Database

```sql
CREATE DATABASE company;
```

## Delete Database

```sql
DROP DATABASE company;
```

## Use Database

```sql
USE company;
```

---

# Table Commands

## Create Table

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    salary DECIMAL(10,2)
);
```

---

## Show Tables

```sql
SHOW TABLES;
```

---

## Describe Table

```sql
DESCRIBE employees;
```

---

## Rename Table

```sql
ALTER TABLE employees
RENAME TO staff;
```

---

## Delete Table

```sql
DROP TABLE employees;
```

---

## Empty Table

```sql
TRUNCATE TABLE employees;
```

---

# Data Types

## Numeric

```
INT
BIGINT
SMALLINT
FLOAT
DOUBLE
DECIMAL
```

## Character

```
CHAR
VARCHAR
TEXT
```

## Date

```
DATE
TIME
DATETIME
TIMESTAMP
YEAR
```

## Boolean

```
BOOLEAN
```

---

# CRUD Operations

## INSERT

```sql
INSERT INTO employees
(name, age, salary)
VALUES
('John',25,50000);
```

---

## SELECT

```sql
SELECT *
FROM employees;
```

Specific columns

```sql
SELECT name,salary
FROM employees;
```

---

## UPDATE

```sql
UPDATE employees
SET salary=60000
WHERE id=1;
```

---

## DELETE

```sql
DELETE FROM employees
WHERE id=5;
```

---

# WHERE Clause

```sql
SELECT *
FROM employees
WHERE age > 25;
```

Operators

```
=
!=
<>
>
<
>=
<=
```

Logical Operators

```
AND
OR
NOT
```

---

# LIKE Operator

```sql
WHERE name LIKE 'A%'
```

Patterns

```
A%
%A
%A%
_
```

Examples

```sql
'A%'
```

Starts with A

```sql
'%A'
```

Ends with A

```sql
'%abc%'
```

Contains abc

```sql
'_A%'
```

Second letter is A

---

# IN Operator

```sql
SELECT *
FROM employees
WHERE department IN
('HR','IT');
```

---

# BETWEEN

```sql
WHERE salary
BETWEEN 30000 AND 70000;
```

---

# IS NULL

```sql
WHERE salary IS NULL;
```

---

# ORDER BY

Ascending

```sql
ORDER BY salary ASC;
```

Descending

```sql
ORDER BY salary DESC;
```

---

# LIMIT

```sql
SELECT *
FROM employees
LIMIT 10;
```

---

# DISTINCT

```sql
SELECT DISTINCT department
FROM employees;
```

---

# Aggregate Functions

Count

```sql
SELECT COUNT(*)
FROM employees;
```

Average

```sql
SELECT AVG(salary)
FROM employees;
```

Sum

```sql
SELECT SUM(salary)
FROM employees;
```

Minimum

```sql
SELECT MIN(age)
FROM employees;
```

Maximum

```sql
SELECT MAX(age)
FROM employees;
```

---

# GROUP BY

```sql
SELECT department,
COUNT(*)
FROM employees
GROUP BY department;
```

---

# HAVING

```sql
SELECT department,
AVG(salary)
FROM employees
GROUP BY department
HAVING AVG(salary)>50000;
```

---

# Joins

## INNER JOIN

```sql
SELECT *
FROM orders
INNER JOIN customers
ON orders.customer_id=customers.id;
```

---

## LEFT JOIN

```sql
SELECT *
FROM customers
LEFT JOIN orders
ON customers.id=orders.customer_id;
```

---

## RIGHT JOIN

```sql
SELECT *
FROM customers
RIGHT JOIN orders
ON customers.id=orders.customer_id;
```

---

## FULL OUTER JOIN

```sql
SELECT *
FROM customers
FULL OUTER JOIN orders
ON customers.id=orders.customer_id;
```

---

## CROSS JOIN

```sql
SELECT *
FROM table1
CROSS JOIN table2;
```

---

# UNION

```sql
SELECT city FROM customers

UNION

SELECT city FROM suppliers;
```

---

# UNION ALL

```sql
SELECT city FROM customers

UNION ALL

SELECT city FROM suppliers;
```

---

# Constraints

```
PRIMARY KEY
FOREIGN KEY
NOT NULL
UNIQUE
DEFAULT
CHECK
AUTO_INCREMENT
```

---

# Keys

Primary Key

```sql
PRIMARY KEY(id)
```

Foreign Key

```sql
FOREIGN KEY(department_id)
REFERENCES department(id)
```

---

# ALTER TABLE

Add Column

```sql
ALTER TABLE employees
ADD phone VARCHAR(15);
```

Drop Column

```sql
ALTER TABLE employees
DROP COLUMN phone;
```

Modify Column

```sql
ALTER TABLE employees
MODIFY salary DECIMAL(12,2);
```

---

# Indexes

Create

```sql
CREATE INDEX idx_name
ON employees(name);
```

Delete

```sql
DROP INDEX idx_name
ON employees;
```

---

# Views

Create

```sql
CREATE VIEW employee_view AS

SELECT
name,
salary
FROM employees;
```

Delete

```sql
DROP VIEW employee_view;
```

---

# Transactions

```sql
START TRANSACTION;

UPDATE accounts
SET balance=balance-100
WHERE id=1;

UPDATE accounts
SET balance=balance+100
WHERE id=2;

COMMIT;
```

Rollback

```sql
ROLLBACK;
```

---

# CASE Statement

```sql
SELECT

name,

CASE

WHEN salary>100000
THEN 'High'

WHEN salary>50000
THEN 'Medium'

ELSE 'Low'

END

FROM employees;
```

---

# String Functions

```sql
UPPER()

LOWER()

CONCAT()

LENGTH()

SUBSTRING()

TRIM()

REPLACE()
```

Example

```sql
SELECT UPPER(name)
FROM employees;
```

---

# Numeric Functions

```sql
ROUND()

ABS()

CEIL()

FLOOR()

MOD()
```

---

# Date Functions

```sql
NOW()

CURDATE()

CURTIME()

YEAR()

MONTH()

DAY()

DATEDIFF()
```

---

# Window Functions

```sql
ROW_NUMBER()

RANK()

DENSE_RANK()

LAG()

LEAD()
```

Example

```sql
SELECT

name,

salary,

RANK()
OVER(ORDER BY salary DESC)

FROM employees;
```

---

# Subquery

```sql
SELECT *

FROM employees

WHERE salary>

(
SELECT AVG(salary)

FROM employees
);
```

---

# EXISTS

```sql
SELECT *

FROM customers c

WHERE EXISTS

(
SELECT *

FROM orders o

WHERE o.customer_id=c.id
);
```

---

# Common Operators

```
=
!=
<>
>
<
>=
<=

LIKE

IN

BETWEEN

IS NULL

EXISTS

ANY

ALL
```

---

# SQL Execution Order

```
FROM

WHERE

GROUP BY

HAVING

SELECT

ORDER BY

LIMIT
```

---

# Best Practices

✅ Use meaningful table names

✅ Always use WHERE with UPDATE

✅ Always use WHERE with DELETE

✅ Normalize your database

✅ Use indexes wisely

✅ Avoid SELECT *

✅ Backup databases regularly

✅ Use transactions

✅ Use parameterized queries

✅ Prevent SQL Injection

---

# SQL Injection Prevention

Use Prepared Statements

❌

```sql
SELECT *
FROM users
WHERE username='admin'
AND password='123';
```

✅

```sql
SELECT *
FROM users
WHERE username=?
AND password=?;
```

---

# Quick Reference

| Command | Description |
|----------|-------------|
| SELECT | Read Data |
| INSERT | Insert Data |
| UPDATE | Modify Data |
| DELETE | Delete Data |
| CREATE | Create Objects |
| DROP | Delete Objects |
| ALTER | Modify Objects |
| TRUNCATE | Remove All Rows |
| JOIN | Combine Tables |
| GROUP BY | Group Records |
| ORDER BY | Sort Records |
| LIMIT | Limit Rows |
| HAVING | Filter Groups |
| DISTINCT | Remove Duplicates |

---

# Resources

- MySQL Documentation
- PostgreSQL Documentation
- SQLite Documentation
- SQL Server Documentation

---

⭐ If you found this repository helpful, don't forget to **Star** it!
