# sql-basics

We will be using AdventureWorks database in SQL Server for this exercise.

```
USE AdventureWorks2019;
```

## CRUD

#### Create a Sample Table

```
CREATE TABLE SAMPLE_TABLE (
ID INT NOT NULL,
NAME VARCHAR(50) NOT NULL,
AGE INT,
PRIMARY KEY (ID)
);
```

#### Insert record in this table

```
INSERT INTO DBO.SAMPLE_TABLE 
(ID, NAME, AGE) 
VALUES 
(101, 'John Smith', 30);
```

#### Retrieve/Select records from table

All records

```
SELECT * FROM SAMPLE_TABLE;
```

Based on condition

```
SELECT * FROM SAMPLE_TABLE WHERE ID=101;
```

Only specific columns

```
SELECT NAME FROM SAMPLE_TABLE WHERE ID=101;
```
