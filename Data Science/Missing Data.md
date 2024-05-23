<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **How to deal with missing data?**
- There is no particular approach for dealing with missing data.
- The appropriate technique may vary depending on your dataset, specific context and the desired outcome.
- **Missing data:** NULL | NAN | nan | NaN (Ignored while arithmetic operations)
- Row | Observation | Tuple | Sample | Record
- Column | Feature (Data Science) | Field (Excel) | Attribute | Dimension

### **How to identify missing values?**
Check for None or NaN values:
```python
# Check for None:
missing_values = [x is None for x in data]

# Check for NaN:

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

### **How to handle missing values?**

<h5><a href="#del">Drop</a> | <a href="#impute">Impute</a> | <a href="#assign">Assign</a> | <a href="#predict">Predict</a> | <a href="#algo">Algorithm</a></h5>

<h5 name="del">1. dropna(): Drop Missing Values</h5>

- If the missing data is negligible and doesn't affect the overall analysis, drop the corresponding rows or columns.
- Drop rows if missing values < 5% i.e. (axis = 0)
- Drop columns if missing values > 70% i.e. (axis = 1)
- Deleting irrelevant rows or columns helps to get a robust model.
- But it's better to keep data rather than dropping, removing data may lead to loss of information.
- If one value in observation is missing other values may be important.

```python
# DataFrame.dropna()
df.dropna()

# DataFrame.Series.dropna()
df['Sales'].dropna()

# Drop rows
df.dropna(axis=0)

# Drop if any attribute value is NaN
df.dropna(axis=0, how='any')

# Drop if all the attribute values are NaN
df.dropna(axis=0, how='all')

# Drop columns
df.dropna(axis=1)
```

<h5 name="impute"> 2. fillna(): Fill Missing Values</h5>

- Imputation involves estimating missing values with the help of other available rows or columns.
- Impute the numerical missing data with the sample mean or median (SimpleImputer: strategy = 'mean' or 'median') 
- Impute the categorical missing data with the sample most frequent value (SimpleImputer: strategy = 'most_frequent') 
- SimpleImputer() is used to fill in the missing value (Univariate imputation) 
- **fit():** Learn the values (Mean, Median, Mode) to be imputed and **transform():** Fill in the missing values.
- **KNNImputer():** Fill missing data with the help of **K Nearest Neighbours**.
- **fit_transform():** Learn and impute the values in place. Only apply on the train set.
- Never apply fit_transform() on the test set, it causes data leakage.

```python
# DataFrame.fillna()
df.fillna('🌞')

# DataFrame.Series.fillna()
df['Sales'].fillna(0)
```

### Data Leakage 
- Accidentally sharing data from the train set to the test set.

### Disadvantage
- Changes the distribution of the dataset, which will change the mean, median, variance and standard deviation of the sample.
- Bring new outliers in the dataset.
- Changes the correlation among features and the impact of independent variables on the target variable.

<h5 name="assign"> 3. Assign a Unique Category (Categorical Data) | Flag (Numeric Value)</h5>

- Assign a **unique** category for data with **missing values** or assign with "Missing" flag.
- **Flag** the **numeric** missing data with -1 or 0.
- Create a difference between missing data and remaining non-missing data.

<h5 name="predict"> 4. Predict Missing Value</h5>

- Fill missing data with the help of other **features** by **predicting** (**Multivariate** imputation) 
- Use the non missing data (rows) as **train** set and missing data (rows) as **test** set.
- Interpolation: Predict missing data with the range of date and time (Time series forecasting) 

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

# X: Independent Variables 
# y: Dependent Variable
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=1)
```

<h5 name="algo"> 5. Use algorithms that work fine with missing values</h5>

- **KNN:** KNN fills the missing value by taking most of the K nearest values.
- **Random forest:** Weak learners are trained by non-missing data and missing values can be used for testing.

### **Domain Knowledge**
- It will help us to understand the reason behind the missing data.
- Understanding the cause can help us decide how to handle the missing data.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
