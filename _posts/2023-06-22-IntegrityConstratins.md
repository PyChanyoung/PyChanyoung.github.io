---
layout: single
title: "Integrity Constraints"
categories: Database
tag: [Database, SQL]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Definition

Integrity Constraints are rules or restrictions used in a database system to maintain the integrity of the data. These constraints help ensure the accuracy and consistency of the data entered into the database. The following types are commonly included:

1. NOT NULL Constraint: This ensures that a column cannot have a NULL value. When a NOT NULL constraint is applied to a column, you are guaranteed that every row must contain a value for that column.

2. PRIMARY KEY Constraint: The PRIMARY KEY constraint uniquely identifies each record in a database table. Primary keys must contain unique values and cannot be NULL. A table can have only one primary key, which may consist of single or multiple fields.

3. FOREIGN KEY Constraint: A FOREIGN KEY is a field (or collection of fields) in one table that refers to the PRIMARY KEY in another table. The table with the foreign key is called the child table, and the table with the primary key is called the referenced or parent table. This constraint is used to prevent actions that would destroy links between tables.