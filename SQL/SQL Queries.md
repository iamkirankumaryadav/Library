# SQL

### Select All 

```SQL
SELECT * FROM Table;
```

### Select Columns 

```SQL
SELECT Column1, Column2, Column3 
FROM Table;
```	

### Select Distint 

```SQL
SELECT DISTINCT Column 
FROM Table;
```

### Select Count 

```SQL
SELECT COUNT(DISTINCT Column) 
FROM Table;
```

### Select Condition  

```SQL
SELECT * FROM Table 
WHERE Column = Value;
```

### Select Between  

```SQL
Select * From Table Where Column Between A And B;
```

Select Like ( Pattern ) :  Select * From Table Where Column Like 'S%' ( Start with S );

'K%'    : Starts with K
'%K'    : Ends with K
'%K%'   : K at any Position
'_K%'   : K at Second Position
'A___%' : Four Letter Words Starting with A
'K%V'   : Starting with K and Ending with V
'[ABC]%': Starting with A, B and C
'[!AB]%': Not Starting with A and B
--------------------------------------------------------------------------------------

Select In : Select * From Table Where Column in ('A', 'B');

Select Null : Select * From Table Where Column Is Null

Select Not Null : Select * From Table Where Column Is Not Null

Select And : Select * From Table Where Column1 = A And Column2 = B;

Select Or : Select * From Table Where Column1 = A Or Column2 = B;

Select And + Or : Select And : Select * From Table Where Column1 = A And ( Column2 = B or Column3 = C );

Select Not : Select * From Table Where Not Column = A;

Select Not And : Select * From Table Where Not Column1 = A And Not Column2 = B;

Select Order By : Select Column1, Column2 From Table Order By Column1 DESC, Column2 ASC;

Insert : Insert Into Table(Column1, Column2, Column3) Values(Value1, Value2, Value3); 

Update : Update Table Set Column1 = Value1, Column2 = Value2 Where Condition;

Delete : Delete From Table Where Column = Value;

Select Top : Select Top 10 * From Table; | Select * From Table Limit = 10;

Select Aggregate ( COUNT(), AVG(), SUM(), MIN(), MAX() )  

```SQL
SELECT SUM(Column) AS SumColumn 
FROM Table Where Column = A;
```

# Joins

1. Inner Join
2. Left Join
3. Right Join
4. Full Join | Full Outer Join

### Join 3 Tables : 

```SQL
SELECT Table1.Column1, Table2.Column2, Table3.Column3 
FROM ((Table2 INNER JOIN Table1 ON Table1.ID = Table2.ID ) Table3 INNER JOIN Table1 ON Table1.ID = Table3.ID)
```

### Inner Join  

```SQL
SELECT Table1.Column1, Table1.Column2, Table1.Column3 
FROM Table1 INNER JOIN Table2 ON Table1.ID = Table2.ID
```

# Union

### Distinct Union 

```SQL
SELECT Column1, Column2, Column3 
FROM Table1 
UNION 
SELECT Column1, Column2, Column3 
FROM Table2
```

### Condition 

```SQL
SELECT Column1, Column2, Column3 
FROM Table1 
WHERE Column1 = A 
UNION 
SELECT Column1, Column2, Column3 
FROM Table2 
WHERE Column1 = B 
ORDER BY Column1
```

### Union All  

```SQL
SELECT Column1, Column2, Column3 
FROM Table1 
UNION ALL 
SELECT Column1, Column2, Column3 
FROM Table2
```

### Group By 

```SQL
SELECT COUNT(ID), Column1 
FROM Table 
GROUP BY Column1;
```

```SQL
SELECT COUNT(ID), Column1 
FROM Table 
GROUP BY Column1 
ORDER BY Count(ID) DESC;
```

### Join + Group By 

```SQL
SELECT Table1.Column1, Count(Table1.ID) 
FROM Table1 LEFT JOIN Table2 ON Table1.ID = Table2.ID 
GROUP BY Column1
```

### Join + Group By + Having 

```SQL
SELECT Table1.Column1, Count(Table1.ID) 
FROM Table1 INNER JOIN Table2 ON Table1.ID = Table2.ID
WHERE Column1 = 'A' And Column2 = B
GROUP BY Column1
HAVING Count(Table1.Column1) > 20
ORDER BY Count(ID) DESC;
```
                            
### Where Exists   

```SQL
SELECT Column1 
FROM Table1 
WHERE EXISTS(SELECT Column2 FROM Table2 WHERE Table2.ID = Table1.ID)
```

### Select Any 

```SQL
SELECT Column1 
FROM Table1 
WHERE Column1ID = ANY(SELECT Column FROM Table2 WHERE Column = 'Value')
```

### Select All 

```SQL
SELECT Column1 
FROM Table1 
WHERE Column1ID = ALL(SELECT Column FROM Table2 WHERE Column > 10)
```

### Select Into 

```SQL
SELECT * INTO New Table 
FROM Old Table 
WHERE Column = B;
```

```SQL
SELECT * INTO IndianCustomer 
FROM Customers 
WHERE Country = 'India';
```

### Insert Into : 

```SQL
INSERT Into Table2(Colum1, Column2, Column3) 
SELECT Column1, Column2, Column3 
FROM Table1
WHERE Column1 = Value;
```	

### SQL Case   

```SQL
SELECT OrderID, Quantity,
CASE
    WHEN Quantity = 30 THEN 'Quantity is Matching'
    WHEN Quantity < 30 THEN 'Quantity is Less than 30'
    ELSE 'Quantity is More than 30'
END AS QuantityMessage
FROM OrderDetails;
```

### Select Null : 

`IFNULL`(Column, Value) : If Value is NULL Replace it by 0 

```SQL
SELECT Product, IFNULL(Price, 0) 
FROM Products.
```

### Sql Constraints

1. NOT NULL
2. AUTO_INCREMENT
3. PRIMARY KEY
4. FOREIGN KEY
5. CHECK
6. DEFAULT

```SQL
CREATE TABLE Employee
(
      ID     INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
      Name   VARCHAR(255),
      Age    INT CHECK(Age > 18),
      DeptID INT NOT NULL FOREIGN KEY REFERENCES Department(DeptID),
      City   VARCHAR(255) DEFAULT 'Banglore'
)
```

### Sql Views

```SQL
CREATE VIEW [Indian Customer] AS
SELECT CustomerName, ContactNumber
FROM Customers
WHERE Country = 'India';
```


```SQL
CREATE VIEW [Over Price] AS 
SELECT ProductName, Price
FROM Product
WHERE Price > (SELECT AVG(Price) FROM Product);
```