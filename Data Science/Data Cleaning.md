# Data Cleaning

1. [Handling missing values](https://github.com/iamkirankumaryadav/Library/blob/d023ba0dac66a55007b1c518e1fc1039b4a4e9c1/Data%20Science/Missing%20Data.md)
2. [Outlier detection and treatment](https://github.com/iamkirankumaryadav/Library/blob/d023ba0dac66a55007b1c518e1fc1039b4a4e9c1/Data%20Science/Outliers.md)
3. [Encoding categorical variable](https://github.com/iamkirankumaryadav/Library/blob/d023ba0dac66a55007b1c518e1fc1039b4a4e9c1/Data%20Science/Categorical.md)
4. [Feature scaling](https://github.com/iamkirankumaryadav/Library/blob/d023ba0dac66a55007b1c518e1fc1039b4a4e9c1/Data%20Science/Normalization%20vs%20Standardization.md)

### Types of Errors

1. **Missing Values**: NaT, NaN, NA, None (Data type of NaN is float)

2. **Bad Values**: Outlier, value generated due to error, spelling mistakes, case mistakes (cpu and CPU)
```python
# How to find bad data: Look after distribution and outliers
df.groupby('column').describe()

# Check the count of labels (Categorical) or distribution of data labels :
df['column'].value_counts()

# Data visualization is the best way to check the distribution (Numerical) and frequency or count (Categorical) of data
pd.pivot(df, index='time', columns='name').plot(subplots=True)

# Remove the outliers by setting lower and upper bounds: 
df.query("type='cpu' & (value > 0 | value < 20)")
df.query("type='cpu' and (value > 0 or value < 20)")

# Find outliers by using Mean and Standard Deviation (Z Score):
zscore = x - mean() / std()
# Data / Values / Points outside 3 std is considered as outliers.
```

3. Duplicates: Same data 

```python
# How to look for duplicates :
df.duplicated()

# Duplicates only in particular columns.
df.duplicated(['column1', 'column3']) 
```

### Causes of Errors
1. **Human Error:** Entering wrong data (Uppercase/Lowercase, No proper validation, 'O' instead of **0**, Typo, Spelling, Copy/Paste)
2. **Machine Error:** Faulty sensor, measuring devices, dirt on camera, time inaccuracy, network error. 
3. **Design Error:** System and UI for collecting data (Input forms, payment forms without proper input and data validations)

### Detecting Errors
1. **Schema and Validation:** Data type, relationship, format, constraint, accuracy, consistency, etc.
2. **Missing:** Filling missing values or dropping rows/columns with missing values (NULL, NaN, Empty)
3. **Domain Knowledge:** Help to understand the valid value and range of the data (-90 <= Latitude <=90 and -180 <= Longitude <= 180)
4. **Visualization:** Histograms, boxplots and bar charts help visualise data distribution, frequency, and outliers.

### Cleaning Empty Cells
- Fixing bad data (Empty cells, data in wrong format, wrong data, and duplicates)
```python
# Remove rows that contain empty cells/ NULL values:
import pandas as pd
df = pd.read_csv('data.csv')
df.dropna(inplace=True)

# Replace/Fill empty cells with a new values:
df.fillna(999)

# Replace/Fill only for specified Columns:
df['MRP'].fillna(450.50)

# Replace/Fill using mean, median, or mode:
df['MRP'].fillna(df['MRP'].mean(), inplace=True)
```

### Cleaning data of wrong format
```python
df['Sale_Date'] = pd.to_datetime(df['Sale_Date'])
```

<p align='right'><a align="right" href="https://github.com/iamkirankumaryadav/Library/blob/main/Interview.md">Back to Questions</a></p>
