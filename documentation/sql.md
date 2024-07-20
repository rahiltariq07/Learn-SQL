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

| ID | Name | Age | City |
|----|------|-----|------|
| 1 | Rahil | 22  | Srinagar |
| 2 | Sahil | 27  | Pulwama  |
| 3 | Aamir | 30  | Budgam   |

- table2 - City

| ID | City |
|----|------|
| 1 | Srinagar |
| 2 | Pulwama  |
| 3 | Budgam   |
