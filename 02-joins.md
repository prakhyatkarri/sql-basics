# Joins

#### Inner Join
Inner Join joins two tables on select column(s) and display only matched records. Inner join is the default join unless mentioned otherwise.

Let's observe these two tables

SalesOrderDetail
![image](./diagrams/sales-orders-product-id.png)

Product
![image](./diagrams/product-product-id.png)


We can see `productID` is a column that exists in both tables and these tables can be joined on this column.

```
SELECT 
	P.ProductID, P.Name, P.ProductNumber,
	S.ProductID, S.SalesOrderDetailID, S.SalesOrderID, S.OrderQty, S.LineTotal
FROM 
	Production.Product P, Sales.SalesOrderDetail S
WHERE
	P.ProductID = S.ProductID;
```
![image](./diagrams/sales-product-product-id-inner-join.png)

Above query can also be written as below

```
SELECT 
	P.ProductID, P.Name, P.ProductNumber,
	S.ProductID, S.SalesOrderDetailID, S.SalesOrderID, S.OrderQty, S.LineTotal
FROM 
	Production.Product P
JOIN
	Sales.SalesOrderDetail S
ON
	P.ProductID = S.ProductID
;
```
```
SELECT 
	P.ProductID, P.Name, P.ProductNumber,
	S.ProductID, S.SalesOrderDetailID, S.SalesOrderID, S.OrderQty, S.LineTotal
FROM 
	Production.Product P
INNER JOIN
	Sales.SalesOrderDetail S
ON
	P.ProductID = S.ProductID
;
```

#### Left Join
Left join joins two tables on selected colun(s) and displays matched records along with all records from left mentioned table. For the records that doesn't have a match, records from right mentioned table will be shown as NULL.

```
SELECT 
	P.ProductID, P.Name, P.ProductNumber,
	S.ProductID, S.SalesOrderDetailID, S.SalesOrderID, S.OrderQty, S.LineTotal
FROM 
	Production.Product P
LEFT JOIN
	Sales.SalesOrderDetail S
ON
	P.ProductID = S.ProductID
ORDER BY P.ProductID
;
```
![image](./diagrams/sales-product-product-id-left-join.png)

#### Right Join
RIght join joins two tables on selected column(s) and displays all records from right table and only matched records from left table. If there is no match in left table, 0 records will be displayed.

```
SELECT 
	P.ProductID, P.Name, P.ProductNumber,
	S.ProductID, S.SalesOrderDetailID, S.SalesOrderID, S.OrderQty, S.LineTotal
FROM 
	Production.Product P
RIGHT JOIN
	Sales.SalesOrderDetail S
ON
	P.ProductID = S.ProductID
ORDER BY 
	P.ProductID
;
```
![image](./diagrams/sales-product-product-id-right-join.png)

#### Full/Outer Join
Full/Outer join joins two tables on selected column(s) and displays all records from both tables. If there is no match, records from unmatched table will be shows as NULL.

```
SELECT 
	P.ProductID, P.Name, P.ProductNumber,
	S.ProductID, S.SalesOrderDetailID, S.SalesOrderID, S.OrderQty, S.LineTotal
FROM 
	Production.Product P
FULL JOIN
	Sales.SalesOrderDetail S
ON
	P.ProductID = S.ProductID
ORDER BY 
	P.ProductID
;

```
```
SELECT 
	P.ProductID, P.Name, P.ProductNumber,
	S.ProductID, S.SalesOrderDetailID, S.SalesOrderID, S.OrderQty, S.LineTotal
FROM 
	Production.Product P
FULL OUTER JOIN
	Sales.SalesOrderDetail S
ON
	P.ProductID = S.ProductID
ORDER BY 
	P.ProductID
;

```
![image](./diagrams/sales-product-product-id-full-outer-join.png)

  