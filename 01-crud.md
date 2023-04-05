## CRUD (Create/Retrieve/Update/Delete)

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

#### Update records in this table

```
UPDATE DBO.SAMPLE_TABLE
SET NAME = 'Jane Smith'
WHERE ID = 101;
```

#### Delete records from table

```
DELETE FROM DBO.SAMPLE_TABLE
WHERE ID = 101;
```




