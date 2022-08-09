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
df.query("type='cpu' & (value > 0 | value < 20)") or df.query("type='cpu' and (value > 0 or value < 20)")

# Find outliers by using Mean and Standard Deviation (Z Score):
zscore = x - x.mean() / x.std()
# Data / Values / Points outside 3 std is considered as outliers.
```

3. **Duplicates** : Same data 

```python
# How to look for duplicates :
df.duplicated()

# Duplicates only in particular columns.
df.duplicated(['column1', 'column3']) 
```

### Causes of `Errors`

1. **Human** Error : Entering wrong data ( Uppercase/Lowercase, No proper validation, **'O'** instead of **0**, Typo, Spelling, Copy/Paste )
2. **Machine** Error : Faulty sensor, Measuring devices, Dirt on camera, Time inaccuracy, Network error. 
3. **Design** Error : System and UI for collecting data ( Input forms, Payment forms without proper input and data validations )

### Detecting `Errors`

1. **Schema** and **Validation** : Proper data type and relationship of data, format, Constraints ( Whether NULL is allowed in the column or not )  
2. **Missing** : Filling missing value or Dropping rows with missing values ( NULL, NaN, Empty )
3. **Domain Knowledge** : Help to understand the valid value and range of the data ( -90 <= Latitude <=90 and -180 <= Longitude <= 180 )
4. **Visualization** : Histogram, Boxplot and Bar Charts helps to visualize the distribution or frequency of data and outliers.

### Preventing `Errors`
