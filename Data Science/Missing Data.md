<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to deal with missing data?
- There is no particular approach for dealing with missing data (NULL, NaN, None) 
- **NULL:** Represents a missing or undefined value/data.
- **NaN:** Represents an invalid or undefined value/data.
- **None:** Represents absence of a value. It is an object of its own data type (NoneType)
- The appropriate approach depends on your dataset (missing quantity), data type and the analysis goal.

### Terminology
- Row = Observation = Sample = Record 
- Column = Feature = Field = Attribute = Dimension 

### How to identify missing values?
```python
# Check for None:
missing_values = [x is None for x in data]

# Using math library: 
import math 
missing_values = [math.isnan(x) for x in data]

# Using Pandas library:
import pandas as pd 
missing_values = df.isnull().any()
missing_counts = df.isnull().sum()

# Using NumPy library:
import numpy as np
missing_values = np.isnan(array)
```

### How to handle missing values?

<h3><a href="#del">Drop</a> | <a href="#impute">Impute</a> | <a href="#assign">Assign</a> | <a href="#predict">Predict</a> | <a href="#algo">Algorithm</a></h3>

<h3 name="del">1. dropna(): Drop Missing Values</h3>

- If the missing data is negligible and won't impact analysis, drop the corresponding rows or columns.
- Drop rows if missing values < 5% i.e. (axis = 0) | Drop columns if missing values > 70% i.e. (axis = 1)
- Deleting irrelevant rows or columns improves model performance.
- It's better to keep data, deleting data could resuly in valuable information loss.
  
```python
# DataFrame.dropna():
df.dropna()

# DataFrame.Series.dropna():
df["Sales"].dropna()

# Drop rows:
df.dropna(axis=0)

# Drop the row if, any attribute value is NaN:
df.dropna(axis=0, how="any")

# Drop the row if, all the attribute values are NaN:
df.dropna(axis=0, how='all')

# Drop columns:
df.dropna(axis=1)
```

<h3 name="impute">2. fillna(): Fill/Impute Missing Values</h3>

- Imputation is estimating and filling missing values using other available data (non-missing rows or columns)
- **SimpleImputer()** is used for basic imputation using simple strategy (mean, median, most_frequent)
- **Numerical Data:** Fill missing values with the sample mean or median (SimpleImputer: strategy = 'mean' or 'median') 
- **Categorical Data:** Fill missing values with the most frequent value (SimpleImputer: strategy = 'most_frequent')
- **Forward / Backward Fill:** Use previous or next value (Useful in the case of time series scenario) 
- **KNNImputer():** Fills missing data using **K Nearest Neighbours** similarity. More accurate
- **fit():** Learns the values (Mean, Median, Mode) to be imputed and **transform():** Fills the missing values.
- **fit_transform():** Learn and impute the values in one step (Apply only on the training set)
- Never apply **fit_transform()** on the test set to avoid data leakage.

SimpleImputer | KNNImputer
:--- | :---
Verfy fast and easy (mean, median, mode) to implement | Speed depends on "k" and computationally expensive for large dataset
Work well with small datasets | More accurate for complex datasets
Ignores relationship between features | Preserve relationshio between features
Can distort variance and correlation | Can handle correlated features
No scailing required | Scailing required

```python
# DataFrame.fillna()
df.fillna('🌞')

# DataFrame.Series.fillna()
df['Sales'].fillna(0)
```

### Data Leakage 
- Data was accidentally shared from the train set to the test set.

### Disadvantage
- Imputation can alter the distribution and statistics of the dataset.
- **Statistical Properties:** Mean, median, mode, variance, and standard deviation of the sample.
- Imputation might introduce skewness or new outliers in the dataset.
- Imputation changes the correlation between features and the impact of independent variables on the target variable.

<h3 name="assign">3. Assign a Unique Category (Categorical Data) | Flag (Numeric Value)</h3>

- Assign a unique category for missing data or use a "Missing" flag (binary flag)
- Flag the numeric missing data with -1 or 0 to creates a clear distinction between missing and non-missing data.

<h3 name="predict">4. Predict Missing Value</h3>

- Multivariate imputation: Fill missing data by predicting from other features.
- Use non-missing rows as the train set and missing rows as the test set.
- Interpolation: Predict missing values based on time or date ranges (used in time series).

```python
from sklearn.linear_model import LinearRegression
import pandas as pd

data = pd.read_csv("train.csv")
data = data[["Survived", "Sex", "Age"]]

test_set = data[data["Age"].isnull()] # Missing data will be test set.

data.dropna(inplace=True) # Remaining data (Non-Null) will be used for training the model.

y_train = data["Age"]
X_train = data.drop("Age", axis=1)
X_test = test_set.drop("Age", axis=1)

model = LinearRegression()
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```

```python
# Create Test Set = 20% of Dataset.
from sklearn.model_selection import train_test_split

# X: Independent Variables, y: Dependent Variable
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=1)
```

<h3 name="algo"> 5. Use algorithms that work fine with missing values</h3>

- **KNN:** Fills missing values by looking at the K nearest values (Focus on nearby data points)
- **Random Forest:** Trains weak models using non-missing data and uses missing values for testing.
- **SVM:** Focuses on support vectors (data points close to the decision boundary/hyperplane)
- Experiment with different algorithms and compare their performance on specific datasets.

### Domain Knowledge
- It helps us understand why data is missing, whether it’s random or due to an error.
- Knowing the cause can guide us in deciding the best way to handle the missing data.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
