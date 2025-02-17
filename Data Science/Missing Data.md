<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to deal with missing data?
- There is no particular approach for dealing with missing data (NULL, NaN, None)
- **NULL:** Represents a missing or undefined value in a database. NULL is a marker to denote missing data.
- **NaN:** Represents a value that is not a valid number. Typically a floating-point value.
- **None:** Represents the absence of a value or a null value. It is an object of its own data type (NoneType)
- The appropriate approach depends on your dataset (missing quantity), data type and the analysis goal.
- Row | Observation | Tuple | Sample | Record (All are same)           
- Column | Feature | Field | Attribute | Dimension (All are same)

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

- If the missing data is negligible and doesn't affect the overall analysis, drop the corresponding rows or columns.
- Drop rows if missing values < 5% i.e. (axis = 0) | Drop columns if missing values > 70% i.e. (axis = 1)
- Deleting irrelevant rows or columns helps to get a robust model.
- But it's better to keep data rather than dropping, removing data may lead to loss of information.

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

- Imputation involves estimating missing values with the help of other available (non missing) rows or columns.
- Impute the numerical missing data with the sample mean or median (SimpleImputer: strategy = 'mean' or 'median') 
- Impute the categorical missing data with the sample most frequent values (SimpleImputer: strategy = 'most_frequent') 
- SimpleImputer() is used to fill in the missing values (Univariate imputation) 
- **fit():** Learn the values (Mean, Median, Mode) to be imputed and **transform():** Fill in the missing values.
- **KNNImputer():** Fill missing data with the help of the **K Nearest Neighbours**.
- **fit_transform():** Learn and impute the values in place. Only apply on the train set.
- Never apply **fit_transform()** on the test set, it will cause data leakage.

```python
# DataFrame.fillna()
df.fillna('🌞')

# DataFrame.Series.fillna()
df['Sales'].fillna(0)
```

### Data Leakage 
- Data was accidentally shared from the train set to the test set.

### Disadvantage
- Imputation changes the distribution and the statistical properties of the dataset.
- Statistical Properties: Mean, median, mode, variance, standard deviation of the sample.
- Imputation might bring skewness and new outliers in the dataset.
- Imputation changes the correlation among features and the impact of independent variables on the target variable.

<h3 name="assign">3. Assign a Unique Category (Categorical Data) | Flag (Numeric Value)</h3>

- Assign a **unique** category for data with **missing values** or assign with a "Missing" flag or some binary flag.
- **Flag** the **numeric** missing data with -1 or 0.
- Create a difference between missing data and remaining non-missing data.

<h3 name="predict">4. Predict Missing Value</h3>

- Fill missing data with the help of other **features** by **predicting** them (**Multivariate** imputation) 
- Use the non-missing data (rows) as the **train** set and missing data (rows) as the **test** set.
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

# X: Independent Variables, y: Dependent Variable
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=1)
```

<h3 name="algo"> 5. Use algorithms that work fine with missing values</h3>

- **KNN:** KNN fills the missing values by taking most of the K nearest values (Focus on nearest neighbours)
- **Random forest:** Weak learners are trained by non-missing data and missing values can be used for testing.
- **SVM:** SVM focuses on the support vectors (data points) nearest to the hyperplane.
- Experiment with different algorithms and compare their performance on specific datasets.

### Domain Knowledge
- It will help us understand why the data is missing, whether the absence is random or due to an error.
- Understanding the cause can help us decide how to handle the missing data better.
<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
