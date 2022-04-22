# Common SQL Questions :

### 1. When and how might you use an **alias** ?
```sql
SELECT S.Last_Name, 
COUNT(S.Last_Name) 
AS TotalStudents
FROM Students S
```

### 2. **Relationship** types in SQL ?
```sql
1. One to One   : One person can choose one stream. 
2. One to Many  : One teacher can teach many subjects.
3. Many to Many : Many students can learn many subjects.
```

### 3. Difference between **UNION** and **UNION ALL**
- The **Number** of the columns, **Data type** and **Order** of the columns should be same, the only difference is **UNION** keeps only **DISTINCT** where as **UNION ALL** preserves duplicates.

### 4. **Main Clauses** in **SQL Query**.
```sql
SELECT S.First_Name, S.Last_Name, S.Department, Count(S.Class)
FROM Staff S
WHERE S.Last_Name LIKE '%ol%'
ORDER BY S.Last_Name
HAVING Count(S.Class) > 5
GROUP BY S.Department DESC
```
```
1. SELECT   : Select the columns.
2. FROM     : Where the data is coming from ? (Which Table)
3. WHERE    : Filter out the data.
4. ORDER BY : Column which we will be using to sort the data. 
5. HAVING   : What characteristics ? (Usually used in Aggregate Function)
6. GROUP BY : Always follows the HAVING Clause.
```
