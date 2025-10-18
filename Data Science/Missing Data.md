<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to deal with missing data?
- Missing data can appears as NULL, NaN (Undefined / Invalid), or None.
- There is no universal approach for dealing with missing data.
- The appropriate approach depends on the amount of missing data, missing pattern, data type, and the objective of analysis.

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

<h3><a href="#del">Drop</a> | <a href="#impute">Impute</a> | <a href="#assign">Assign</a> | <a href="#predict">Predict</a> | <a href="#algo">Algorithm</a></h3>

<h2 name="del">1. dropna(): Drop Missing Values</h2>

- If the missing data is negligible and won't impact analysis, drop the corresponding rows or columns.
- Drop rows if missing values < 5% i.e. (axis = 0) | Drop columns if missing values > 70% i.e. (axis = 1)
- Deleting irrelevant rows or columns can improve model performance.
- Generally it's better to keep data, deleting data can lead to loss of valuable information.
  
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

<h2 name="impute">2. fillna(): Fill/Impute Missing Values</h2>

Estimating and filling missing values using other available data (non-missing rows or columns)

### SimpleImputer():
- Used for basic imputation strategy (mean, median, most_frequent)
- **Numerical Data:** Fill missing values with the sample mean or median (SimpleImputer: strategy = 'mean' or 'median') 
- **Categorical Data:** Fill missing values with the most frequent value (SimpleImputer: strategy = 'most_frequent')
- Pros: Fast, easy, works well with small dataset
- Cons: Ignores feature relationships, can distort variance and correlation.

### Forward Fill / Backward Fill:
- Use previous or next value (Best for time series)
  
### KNNImputer: 
- Fills missing data using **K Nearest Neighbours** similarity.
- Never apply **fit_transform()** on the test set to avoid data leakage.

Feature | SimpleImputer | KNNImputer
:--- | :--- | :---
Speed | Fast | Slow, depends on k
Dataset Size | Works well for small datasets | Better for large complex datasets
Feature Relationships | Ignores | Preserves
Variance and Correlation | Can distort | Handles correlated features
Scailing | Not required | Required

### Important things to consider:
- **fit():** Learns the imputation values (Mean, Median, Mode)
- **transform():** Applies learned values to fill missing data.
- **fit_transform():** Learn and apply the values in one step (Apply only on the training set)
- Never apply **fit_transform()** on test set (Avoid data leakage)

```python
# DataFrame.fillna()
df.fillna('🌞')

# DataFrame.Series.fillna()
df['Sales'].fillna(0)
```

## Data Leakage 
- Data accidentally used from outside the training dataset (future data) to build the model.
- The model learns pattern it shouldn't have access during prediction.
- Leads to overfitting and inflated accuracy on training / validation datasets.

### Common Causes
- Imputation on testing set using fit_transform(): Learns (mean, median, mode) from test dataset instead of predicting.
- Feature Engineering using target variable: Creating a feature that uses the target data.
- Future Data: Using future data in time series forecasting.
- Cross Validation mistakes: Preprocssing applied before splitting into train / test split.

### Preventive Measures
- Always fit preprocessing steps (Imputation, Scailing, and Encoding) only on training dataset, then transform test dataset.
- Avoid using target reference into feature creation.
- For time series ensure training dataset is ordered according to timestamp chronology.

### Imputation Disadvantage
- Alters the distribution and statistical properties of the dataset.
- **Statistical Properties:** Mean, median, mode, variance, and standard deviation of the sample.
- Imputation might introduce skewness or new outliers in the dataset.
- Imputation changes the correlation between the independent variables and target variable. Impacting model accuracy.

<h2 name="assign">3. Assign a Unique Category (Categorical Data) | Flag (Numeric Value)</h2>

- Assign a unique category for missing data or use a "Missing" flag (binary flag)
- Flag the numeric missing data with -1 or 0 to creates a clear distinction between missing and non-missing data.

<h2 name="predict">4. Predict Missing Value</h2>

- Fill the missing data by predicting from other features.
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

<h2 name="algo"> 5. Use algorithms that work fine with missing values</h2>

- **KNN:** Fills missing values by looking at the K nearest values (Focus on nearby data points)
- **Random Forest:** Trains weak models using non-missing data and uses missing values for testing.
- **SVM:** Focuses on support vectors (data points close to the decision boundary/hyperplane)
- Experiment with different algorithms and compare their performance on specific datasets.

### Domain Knowledge
- It helps us understand the missing patterns, whether it’s random or due to an error.
- Knowing the cause can guide us in deciding the best way to handle the missing data.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
