# sql-basics

We will be using AdventureWorks database in SQL Server for this exercise.

```
USE AdventureWorks2019;
```

## CRUD

#### Create a Database

```
CREATE TABLE SAMPLE_TABLE (
ID INT NOT NULL,
NAME VARCHAR(50) NOT NULL,
AGE INT,
PRIMARY KEY (ID)
);
```