# Learning SQL

- [Introduction](#introduction)
- [Keys](#keys)

### INTRODUCTION

### 1. What is SQL?

SQL is a programming language used to interact with relational databases.

It is used to perform **CRUD** operations:
- Create
- Read
- Update
- Delete

### 2. Creating our First Database

Our first SQL Query

```SQL

CREATE DATABASE college;

DROP DATABASE college;

```

## 3. Creating our First Table

```SQL

USE college;

CREATE TABLE students(
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT NOT NULL
);

```

## 4. Database related Queries

```SQL

CREATE DATABASE college;

SHOW DATABASES;

SHOW TABLES;

```

## 5. Table related Queries

- Select & View ALL columns

```SQL

SELECT * FROM students;

(* means ALL)

```

- Insert

```SQL

INSERT INTO students values(1,"Rahil Tariq", 22);

```

### KEYS

## 1. Primary Key

It is a column (or set of columns) in a table that uniquely identifies each row. (a unique id).

There is only 1 PK & it should be NOT null.

## 2. Foreign Key

A foreign key is a column (or set of columns) in a table that refers to the primary key in another table.

There can be multiple FK's.

FK's can have duplicate & null values.

- table1 - Student

| ID | Name | Age | City Id |   City    |
|----|------|------|---------|----------|
| 1  | Rahil | 22  |    1    | Srinagar |
| 2  | Sahil | 27  |    2    | Pulwama  |
| 3  | Aamir | 30  |    3    | Budgam   |

- table2 - City

| ID |   City   |
|----|--------- |
| 1  | Srinagar |
| 2  | Pulwama  |
| 3  | Budgam   |

### Clauses

## 1. Where Clause

To define some conditions

```SQL

SELECT * FROM students
WHERE age>21;

```

## 2. Limit Clause

Sets an upper limit on number of rows to be returned

```SQL

SELECT * FROM students LIMIT 3;

```

## 3. Order By Clause

To sort the ascending (ASC) or descending order (DSC)

```SQL

SELECT * FROM students ORDER BY name ASC;

```

### Operators

## 1. AND

To check for both conditions to be true

```SQL

SELECT * FROM students WHERE age > 22 AND city = "Srinagar";

```

## 2. OR

To check for one of the conditions to be true

```SQL

SELECT * FROM students WHERE age > 22 OR city = "Srinagar";

```

## 3. BETWEEN

Selects for a given range

```SQL

SELECT * FROM students WHERE age BETWEEN 20 AND 23;

```

## 4. IN

Matches any values in the list

```SQL

SELECT * FROM students WHERE city IN ("Srinagar", "Pulwama");

```

## 5. NOT

To negate the given condition

```SQL

SELECT * FROM students WHERE city NOT IN ("Srinagar", "Pulwama");

```