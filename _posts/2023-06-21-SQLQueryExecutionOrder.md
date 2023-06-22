---
layout: single
title: "SQL query execution order"
categories: Database
tag: [Database, SQL]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Definition

SQL query execution order refers to the sequence in which operations in a SQL query are performed by the database management system. Despite the order in which the clauses appear in the written SQL statement, the actual execution order is determined by the database system's query optimizer to ensure efficient data retrieval.

## SQL query execution order

1. `FROM` : Choose the table that the query will work with.
2. `JOIN` : This performs join operations between the tables specified in the `FROM` clause.
3. `WHERE` : This filters rows from the result of `FROM` and `JOIN` that match certain conditions.
4. `GROUP BY` : This groups rows that have passed through the `WHERE` clause based on specified columns.
5. `HAVING` : This filters groups created through `GROUP BY` that match certain conditions.
6. `SELECT` : This selects the desired columns from the final result passed through filtering and grouping
7. `DISTINCT` : This eliminates duplicates rows in the `SELECT` clause.
8. `ORDER BY` : This sorts the result of the `SELECT` clause based on specified columns.
9. `LIMIT` : This selects only a certain number of rows from the result sorted by `ORDER BY`.

