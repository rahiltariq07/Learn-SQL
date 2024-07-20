# Learning SQL

- [Introduction](#introduction)
- [Keys]()

### Introduction

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

SHOW DATABASE;

SHOW TABLES;

```

## 5. Table related Queries

Select & View ALL columns

```SQL

SELECT * FROM students;

(* means ALL)

```