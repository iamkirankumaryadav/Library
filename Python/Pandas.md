<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Pandas 🐼 

```python
import pandas as pd
```
Toolkit to `read`, `write`, `analyze`, `filter`, `manipulate`, `aggregate`, `merge`, `pivot` and `clean` the data.

### Excel for Python. 

- `Column` | `Feature` | `Attribute` | `Series` | `Field` | `Dimension`        
- `Row` | `Index` | `Record` | `Tuple` | `Observation` | `Sample`
- Financial term for a tabular data is `Panel`
- Pandas is an exploratory data analysis toolkit.
- Read | `import` and write | `export` data: `.csv`, `.tsv`, `.txt`, `.xls`, `.xlsx`, `.json`, etc.
- Preview data: `head()`, `tail()`, `sort_values()`, `columns`, `dtypes`, `shape`, `describe()`, `value_counts()`, etc.
- Clean data: `dropna()`, `fillna()`, `drop_duplicates()`, `rename()`, `set_index()`, etc. 
- Transform data: `apply()`, `explode()`, etc.
- Aggregate data: `concat()`, `merge()`, `groupby()`, `pivot_table()`, etc.
- Pandas is used in economics, finance, statistics and analytics.
- Data Types: `Series` ( **1** Dimensional ) and `DataFrames` ( **2** Dimensional )
- Panel: **3** Dimensional ( major_axis and minor_axis )
- Read, Write, Transform, Explore, Pivot, Join, Manipulate, Merge, GroupBy, Aggregate, Clean, Stack and Visualize.  

### `Series`: 1 Dimensional Array

- Hold data value of `homogeneous` data type, i.e. All data values are of **same** data type.
- Data axis labels are called as `index`

```python
# Create a series:
pd.Series([1, 2, 3,4])

# Accessing a series:
DataFrame['SeriesName'] or DataFrame["SeriesName"] or DataFrame.SeriesName
```

<img src="../Python/Image/DataFrames.png" alt='DataFrame'>

### `DataFrame`: 2 Dimensional Array

- Data is aligned in tabular form with `rows` and `columns`
- `DataFrame` is a sequence of `Series` that shares the same index.

```python
# Empty DataFrame:
pd.DataFrame()

# Accessing DataFrame:
DataFrame[['SeriesName1', 'SeriesName2', 'SeriesName3']]
```

<img src="../Python/Image/PandasDataTypes.png" alt='DataFrame'>

### Important features of Pandas library:
1. Data reading from various input and writing to various output: `.read_csv()`, `.read_excel()`, `.read_sql_table()`, `.to_csv()`, etc.
2. Data handling and filtering: `.query()`
3. Data indexing and slicing: `.loc[]`, `.iloc`, `.at[]`, `iat[]`       
4. Data cleaning: 
5. Handling missing data:
6. Supports multiple file formats.
7. Merge, concate and join different datasets.
8. Performance optimization
9. Data visualization.
10. Grouping the data as per requirement.
11. Performing different mathematical operations on the available data.
12. Masking out irrelevant data to only use the required data.
13. Taking out unique data from various repetitions in the dataset.
14. Time series analysis.

### Time Period:
- Time Stamp ( Days, Years, Quarter or Month)

### How to Iterate over a Pandas DataFrame?

```python
for i in df.iterrows():
      pass
```

<table align="center">
      <tr>
            <td><img src="Image/PandasMethod.jfif" alt="Pandas Methods">
            </td>
      </tr>
</table>

## DataFrame `Attributes` and `Methods`

`DataFrame.shape`: Dimensions of DataFrame (Number of rows, Number of columns)

```python
# Dimensions of the dataframe:
print(df.shape)

# Extract only the total number of rows in a dataframe:
print(df.shape[0])

# Extract only the total number of columns in a dataframe:
print(df.shape[1])
```            

1. `DataFrame.head(n)`: Return the top n rows from the dataframe
2. `DataFrame.tail(n)`: Return the bottom n rows from the dataframe

```python
# Default value for n is 5
df.head(n=10)

df.tail(n=10)
```                  
