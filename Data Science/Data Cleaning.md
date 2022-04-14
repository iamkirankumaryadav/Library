# `Data Cleaning`

`Data Cleaning` is very important to prevent from encountering `Errors`

### Types of `Errors`

1. **Missing Values** : NaT, NaN, NA, None ( Data type of NaN is `float` )
2. **Bad Values** : Outlier, Value generated due to error, spelling mistakes, case mistakes ( cpu and CPU )
```python
# How to find bad data : Look after distribution and outliers
df.groupby('column').describe()

# Check the count of labels (Categorical) or distribution of data labels :
df['column'].value_counts()

# Data visualization is the best way to check the distribution (Numerical) and frequency or count (Categorical) of data
pd.pivot(df, index='time', columns='name').plot(subplots=True)

# Remove the outliers by setting a lower and upper bounds :
df.query('type'='cpu' & (value > 0 | value < 20 )

# Find Outliers by using Mean and Standard Deviation (Z Score):
```

3. **Duplicates** : Same data 

```python
# How to look for duplicates :
df.duplicated()

# Duplicates only in particular columns.
df.duplicated(['column1', 'column3']) 
```
