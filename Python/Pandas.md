<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Pandas 🐼

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
pd.Series([1, 2, 3, 4])
```

### `DataFrame`: 2 Dimensional Array

- Data is aligned in tabular form with `rows` and `columns`

```python
# Empty DataFrame:
pd.DataFrame()
```

### Important features of Pandas library:
- Row column selection, indexing and slicing
- Filter data 
- Data alignment 
- Merge, join and concat
- Group by and aggregate
- Reshaping and sorting
- Time series analysis

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
