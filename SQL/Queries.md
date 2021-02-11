# SQL for Data Science
[1. Counting Rows and Items](#count)

<a href='#agg'>2. Aggregation Functions</a>

<a href='#ext'>3. Extreme Value Identification</a>

<a href='#slice'>4. Slicing Data</a>

<a href='#sort'>5. Sorting Data</a>

<a href='#filter'>6. Filter Patterns</a>

<a href='#group'>7. Group By Filtering</a>

### Table
| ID | First Name | Last Name | Age | Gender | City | Birth Date | 
| --- | --- | --- | ---: | :---: | --- | ---: |
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
                      
### DISTINCT : Uniques Values in a Column
``` SQL
SELECT DISTINCT(Age) FROM Employee
```

#### COUNT : Number of Rows | Items{#count}

``` SQL
SELECT COUNT(ID) FROM Employee
```

<h2 name='agg'> Aggregate Functions </h2>

#### SUM : Sum of Numerical Values
``` SQL
SELECT SUM(Age) FROM Employee
```

#### AVG : Average of Numerical Values
``` SQL
SELECT AVG(Age) FROM Employee
```
<h2 name='ext'> Extreme Value Identification </h2>

#### MAX : Maximum Numeric Value
``` SQL
SELECT MAX(Age) FROM Employee
```

#### MIN : Minimum Numeric Value
``` SQL
SELECT MIN(Age) FROM Employee
```

<h2 name='slice'> Slicing Data </h2>

``` SQL
SELECT * FROM Employee WHERE City='Kalyan'
```

<h2 name='sort'> Sorting Data </h2>

``` SQL
SELECT * FROM Employee ORDER BY Age DESC

SELECT * FROM Employee ORDER BY FirstName -- Alphabetical Order
```

<h2 name='filter'> Filter Patterns </h2>

``` SQL
SELECT * FROM Employee WHERE FirstName LIKE 'K%' -- Starting with K
SELECT * FROM Employee WHERE FirstName LIKE '%R' -- Ending with r
SELECT * FROM Employee WHERE FirstName LIKE '%an%' -- Contains an
```

<h2 name='group'> Group By Filtering (Aggregation + Having) </h2>

``` SQL
SELECT SUM(Age) AS Age, City 
FROM Employee 
GROUP BY City

SELECT SUM(Age) AS Age, LastName 
FROM Employee 
GROUP BY LastName
```

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
