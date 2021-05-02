<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

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
SELECT * 
FROM Students 
WHERE Age BETWEEN 8 AND 16;
```

### Select Like ( Pattern )  

```SQL
SELECT * 
FROM Employee 
WHERE Name LIKE 'K%';
```

1. 'K%'    : Starts with K
2. '%K'    : Ends with K
3. '%K%'   : K at any Position
4. '_K%'   : K at Second Position
5. 'A___%' : Four Letter Words Starting with A
6. 'K%V'   : Starting with K and Ending with V
7. '[ABC]%': Starting with A, B and C
8. '[!AB]%': Not Starting with A and B

### Select In 

```SQL
SELECT * 
FROM Sales 
WHERE State IN ('Maharashtra', 'Banglore');
```

### Select Null 

```SQL
SELECT * 
FROM Shop 
WHERE Sale IS NULL
```

### Select Not Null 

```SQL
SELECT * 
FROM Shop 
WHERE Sale IS NOT NULL
```

### Select And 

```SQL
SELECT * 
FROM Sales 
WHERE State = "Maharashtra" AND City = "Mumbai";
```

### Select Or 

```SQL
SELECT * 
FROM Sales 
WHERE State = "Maharashtra" OR City = "Mumbai";
```

### Select And + Or 

```SQL
SELECT * 
FROM Sales
WHERE State = "Maharashtra" AND ( City = "Mumbai" OR City = "Pune" );
```

### Select Not  

```SQL
SELECT * 
FROM Sales 
WHERE NOT City = "Mumbai";
```

### Select Not And 

```SQL
SELECT * 
FROM Sales 
WHERE NOT City = "Mumbai" AND NOT City = "Pune";
```

### Select Order By  

```SQL
SELECT State, City
FROM Sales 
ORDER BY State DESC, City ASC;
```

### Insert 

```SQL
INSERT INTO Table(Column1, Column2, Column3) 
VALUES(Value1, Value2, Value3); 
```

### Update 

```SQL
UPDATE Table 
SET Column1 = Value1, Column2 = Value2 
WHERE Condition;
```

### Delete 

```SQL
DELETE FROM Table 
WHERE Column = Value;
```

### Select Top 

```SQL
SELECT TOP 10 * 
FROM Table; 
```

```SQL
SELECT * 
FROM Table 
LIMIT = 10;
```

### Select Aggregate 

1. COUNT()
2. AVG()
3. SUM()
4. MIN()
5. MAX() 

```SQL
SELECT SUM(Column) AS SumColumn 
FROM Table WHERE Column = A;
```

# Joins

1. Inner Join
2. Left Join
3. Right Join
4. Full Join | Full Outer Join

### Inner Join  

```SQL
SELECT Table1.Column1, Table1.Column2, Table1.Column3 
FROM Table1 INNER JOIN Table2 ON Table1.ID = Table2.ID
```

### Join 3 Tables : 

```SQL
SELECT Table1.Column1, Table2.Column2, Table3.Column3 
FROM ((Table2 INNER JOIN Table1 ON Table1.ID = Table2.ID ) Table3 INNER JOIN Table1 ON Table1.ID = Table3.ID)
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

### Union + Condition 

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
SELECT Country, COUNT(Customer) 
FROM Sales 
GROUP BY Country;
```

```SQL
SELECT Country, COUNT(Customer) 
FROM Sales 
GROUP BY Country 
ORDER BY Count(Customer) DESC;
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
END 
AS QuantityMessage
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

### Sub Queries | Inner Query | Nested Query

```SQL
SELECT * 
FROM Employees
WHERE ID IN (SELECT ID FROM Employees WHERE Salary > 50000);
```

### Extract String

```SQL
SELECT LEFT("Kirankumar Yadav", 10);
------------------------------------
Output : Kirankumar

SELECT RIGHT('Kirankumar Yadav', 5);
------------------------------------
Output : Yadav

SELECT MID("Aspiring Data Scientist", 10, 4)
--------------------------------------------
Output : Data

SELECT CONCAT("Data ", "Science ", "and ", "Artificial ", "Intelligence")
-------------------------------------------------------------------------
Output : Data Science and Artificial Intelligence
```   

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
