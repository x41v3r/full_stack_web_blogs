---
title: mysql
date: 2024-12-23 00:17:38
tags:
---

# 1 Introduction to MySQL

# 2 CRUD (create, read, update, delete)

## 2.1 Querying data

### 2.1.1 SELECT

&emsp;&emsp;The `SELECT` statement is used to *select data from one or more tables*.

To write a `SELECT` statement in MySQL, this is the syntax:

```sql
SELECT select_list
FROM table_name;
```

In this syntax:

* First, specify one or more columns after the `SELECT` keyword (If the `select_list` has multiple columns, each column must be separated by a comma `,`);
* Second, specify the table from which to retrieve data after the `FROM` keyword.

&emsp;&emsp;When executing the `SELECT` statement, MySQL evaluates the `FROM` clause before the `SELECT` clause:

![mysql-select-from](./assets/mysql-select-from.png)

### 2.1.2 ORDER BY

&emsp;&emsp;To sort the rows in the result set, add the `ORDER BY` clause to the `SELECT` statement.

The following illustrates the syntax of the `ORDER BY` clause:

```sql
SELECT 
    select_list
FROM 
    table_name
ORDER BY 
   column1 [ASC|DESC], 
   column2 [ASC|DESC],
   ...;
```

The `ASC` stands for ascending and the `DESC` stands for descending. By default, the `ORDER BY` clause uses `ASC`.

&emsp;&emsp;To sort the result set by multiple columns, specify a comma-separated list of columns in the ORDER BY clause:

```sql
ORDER BY
    column1 ASC,
    column2 DESC;
```

In this case, the `ORDER BY` clause:

1. First, sort the result set by the values in the column1 in ascending order;
2. Then, sort the sorted result set by the values in the column2 in descending order. (Note that *the order of values in the column1 will not change in this step*, only the order of values in the column2 changes.)

When executing the `SELECT` statement with an `ORDER BY` clause, MySQL always evaluates the `ORDER BY` clause after the `FROM` and `SELECT` clauses:

![mysql-select-from-order-by](./assets/mysql-select-from-order-by.png)

### 2.1.3 WHERE

The `WHERE` clause specifies a search condition for the rows returned by a query. The following shows the syntax of the `WHERE` clause:

```sql
SELECT 
    select_list
FROM
    table_name
WHERE
    search_condition;
```

The `search_condition` is a combination of one or more expressions using the logical operator `AND`, `OR` and `NOT`.

The `SELECT` statement will include any row that satisfies the `search_condition` in the result set.

&emsp;&emsp;Besides the `SELECT` statement, we can use the `WHERE` clause in the `UPDATE` or `DELETE` statement to *specify which rows to update or delete*.

&emsp;&emsp;When executing a `SELECT` statement with a `WHERE` clause, MySQL evaluates the `WHERE` clause after the `FROM` clause and before the `SELECT` and `ORDER BY` clauses:

![mysql-select-from-where-order-by]()

### 2.1.4 DISTINCT

&emsp;&emsp;To remove the duplicate rows when querying data, use the `DISTINCT` clause in the `SELECT` statement.

Here’s the syntax of the `DISTINCT` clause:

```sql
SELECT DISTINCT
    select_list
FROM
    table_name
WHERE 
    search_condition
ORDER BY 
    sort_expression;
```

If we specify one column, the `DISTINCT` clause will evaluate the uniqueness of rows based on the values of that column.

However, if we specify two or more columns, the `DISTINCT` clause will use the values of these columns to evaluate the uniqueness of the rows.

&emsp;&emsp;When executing the `SELECT` statement with the `DISTINCT` clause, MySQL evaluates the `DISTINCT` clause after the `FROM`, `WHERE`, and `SELECT` clause and before the `ORDER BY` clause:

![mysql-select-distinct-from-where-order-by]()

# 3 MySQL stored procedures

# 4 MySQL triggers

# 5 MySQL views

# 6 MySQL index

