<table>
  <tr><td><a align="left" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Python/Pandas.md">Back to Pandas</a></td></tr> 
  <tr><td><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></td></tr>
</table>

# `Join`, `Merge` and `Concat`

- For `pandas.DataFrame` both `join` and `merge` operates on columns and rename common columns using parameter `suffix`
- `concat` can operate on columns or rows, depending on parameter `axis` and no renamin is performed.
- `concat` allow defining hierarchy structure by passing in parameters `keys` and `names`

### `DataFrame.join()` : `how = 'left' | 'right' | 'inner' | 'outer'`

- Combine `all` the columns from the two tables.
- Common columns are renamed with the paramaters `lsuffix` and `rsuffix`

![Join](../Python/Image/Join.png)

```python
DataFrame.join(self, 
               other, 
               on=None, 
               how='left', 
               lsuffix='', rsuffix='', 
               sort=False)
```


### `DataFrame.merge()` : `how = 'left' | 'right' | 'inner' | 'outer' | 'cross'`

- `Merge` combines `all` the columns from two tables.
- Common columns can be renamed by parameter `suffixes`

`Merge` provide 3 ways to control alignment 

1. `on = 'ColumnName'` ( Here the given column must be the common column in both tables )
2. `left_on = 'ColumnName'` and `right_on = 'ColumnName'` ( Tables are aligned using different columns )
3. `left_index = True` and `right_index = True` ( Tables are aligned based on their index )

```python

# Starting with DataFrame:
DataFrame.merge(self, 
                right, 
                how='inner', 
                on=None, 
                left_on=None, right_on=None, 
                left_index=False, right_index=False, 
                sort=False, 
                suffixes=('_x', '_y'), 
                copy=True, 
                indicator=False, 
                validate=None)
                
# Starting with Pandas:                
pandas.merge(left, 
             right, 
             how='inner', 
             on=None, 
             left_on=None, right_on=None, 
             left_index=False, right_index=False, 
             sort=False, 
             suffixes=('_x', '_y'), 
             copy=True, 
             indicator=False, 
             validate=None)                
```

### `pandas.concat()` : `join = 'inner' | 'outer'`

### `axis = 0` : `Horizontally` | `Row Wise`
![Join](../Python/Image/ConcatAxis0.png)

### `axis = 1` : `Vertically` | `Column Wise`
![Join](../Python/Image/ConcatAxis1.png)

```python
pandas.concat(objs, 
              axis=0, # 0 for row and 1 for column
              join='outer', join_axes=None, 
              ignore_index=False, 
              keys=None, 
              levels=None, 
              names=None, 
              verify_integrity=False, 
              sort=None, 
              copy=True)
```
