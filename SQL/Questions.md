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

