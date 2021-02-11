# SQL for Data Science

### Table
| ID | FirstName | LastName | Age | Gender | City | BirthDate | 
| --- | --- | --- | ---: | :---: | --- | --- |
| 1 | Kirankumar | Yadav | 25 | M | Thane | 1996-02-07 |
| 2 | Paramveer | Yadav | 26 | M | Kalyan | 1995-01-21 |
| 3 | Gaurav | Sonar | 26 | M | Kalyan | 1995-03-21 |
| 4 | Pranit | Sorte | 28 | M | Ambernath | 1993-06-21 |

### Create Table
``` SQL
CREATE TABLE Employee
(
ID        INT IDENTITY,
FirstName VARCHAR(255) NOT NULL,
LastName  VARCHAR(255),
Age       INT CHECK(Age>=18),
Gender    VARCHAR(1),
City      VARCHAR(255) 
)
```

### INSERT : Insert Row
``` SQL
INSERT INTO Employee VALUES('Kirankumar','Yadav',25,'M','Thane')
```

### ALTER : Add New Column to Table : DATE (yyyy-MM-dd)
``` SQL
ALTER TABLE Employee ADD BirthDate DATE 
```

### UPDATE : Update Table Value
``` SQL
UPDATE Employee SET BirthDate='1996-02-07' WHERE ID=1
```

### SELECT
``` SQL
SELECT * FROM Employee 
```

### INSERT : Insert Multiple Rows
``` SQL
INSERT INTO Employee VALUES('Paramveer','Yadav',26,'M','Kalyan','1995-01-21'),
                           ('Gaurav','Sonar',26,'M','Kalyan','1995-03-21'),
                           ('Pranit','Sorte',28,'M','Ambernath','1993-06-21')
```

``` SQL
INSERT INTO Employee VALUES('Nimesh','Verma',27,'M','Badlapur','1994-09-21')
```

### DELETE
``` SQL
DELETE FROM Employee WHERE ID=5
```
                      
### DISTINCT() : Uniques Values in a Column
``` SQL
SELECT DISTINCT(Age) FROM Employee
```

# Aggregations 

### COUNT() : Number of Rows | Items
``` SQL
SELECT COUNT(ID) FROM Employee
```

### SUM() : Sum of Numerical Values
``` SQL
SELECT SUM(Age) FROM Employee
```

### AVG() : Average of Numerical Values
``` SQL
SELECT AVG(Age) FROM Employee
```

### MAX() : Maximum Numeric Value
``` SQL
SELECT MAX(Age) FROM Employee
```

### MIN() : Minimum Numeric Value
``` SQL
SELECT MIN(Age) FROM Employee
```
### Slicing Data 
``` SQL
SELECT * FROM Employee WHERE City='Kalyan'
```

### Sorting Data 
``` SQL
SELECT * FROM Employee ORDER BY Age DESC

SELECT * FROM Employee ORDER BY FirstName -- Alphabetical Order
```
### Filtering Patterns
``` SQL
SELECT * FROM Employee WHERE FirstName LIKE 'K%' -- Starting with K
SELECT * FROM Employee WHERE FirstName LIKE '%R' -- Ending with r
SELECT * FROM Employee WHERE FirstName LIKE '%an%' -- Contains an
```

### GROUP BY with Aggregation
``` SQL
SELECT SUM(Age) AS Age, City 
FROM Employee 
GROUP BY City

SELECT SUM(Age) AS Age, LastName 
FROM Employee 
GROUP BY LastName
```

### GROUP BY + HAVING
``` SQL
SELECT SUM(Age) AS Age, City 
FROM Employee 
GROUP BY City 
HAVING SUM(Age) > 30
```

### OFFSET
``` SQL
SELECT FirstName, LastName
FROM Employee
ORDER BY City
OFFSET 2 ROWS
```

### TOP 
``` SQL
SELECT TOP 2 * FROM Employee
```

### BETWEEN
``` SQL
SELECT * FROM Employee WHERE Age BETWEEN 26 AND 28
```

### IN
``` SQL
SELECT * FROM Employee WHERE Age IN (26,28)
```

### IS NOT NULL
``` SQL
SELECT * FROM Employee WHERE Age IS NOT NULL
```

### DROP Table
```SQL
DROP TABLE Employee
```
