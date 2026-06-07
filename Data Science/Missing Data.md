<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

###  How to deal with missing data?
```
✅ Missing data refers to values that are not available in a dataset.
  ⛔ NULL → No value present 
  ⛔ NaN → Undefined or invalid value
  ⛔ None → Missing value in Python
✅ There is no universal approach that works for every dataset.
✅ Machine learning models usually cannot work properly with missing values.
✅ Appropriate approach depends on the amount of missing data, pattern, data type, and objective of analysis.
```

### 🎯 What Determines the Best Approach?
```
1️⃣ Amount of Missing Data
  Very few missing values: Simple fix
  Many missing values: Advanced techniques

2️⃣ Missing Data Pattern
  Are missing random?
  Are they concentrated in specific column?
  Why data is missing?

3️⃣ Data Type
  Numerical Data: Age, Salary, Height (Mean, Median)
  Categorical Data: Gender, City, Department (Mode, Most frequent)

4️⃣ Analysis Objective
  📊 Statistical Analysis
  🤖 Machine Learning
  📈 Business Reporting
  Different objectives may require different handling strategies.
```

### Terminology
```
Row → Observation | Sample | Record 
Column → Feature | Field | Attribute | Dimension | Variable
```

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

<h3 name="del">🗑️ 1. dropna(): Drop Missing Values</h3>

```
✅ Dropping missing values means removing rows or columns that contain missing data from the dataset.
✅ If the missing values are negligible and won't impact analysis, drop the corresponding rows or columns.
✅ If the percentage of missing values is very small, removing those rows usually won't affect the analysis much.
✅ If a column contains too many missing values, it may not provide enough useful information.
✅ Drop rows if missing values < 5% i.e. (axis = 0) | Drop columns if missing values > 70% i.e. (axis = 1)
✅ Deleting irrelevant rows or columns can improve data quality and model performance.
✅ Generally it's better to impute data, deleting data can lead to loss of valuable information.
```
  
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

<h3 name="impute">➕ 2. fillna(): Fill / Impute Missing Values</h3>

Estimating and filling missing values using the available data (non-missing rows or columns)

### 1️⃣ SimpleImputer():
```
✅ SimpleImputer fills missing values using simple statistical measures (mean, median, most_frequent)
🔢 Numerical Data: Fill missing values with the sample mean or median (strategy = 'mean' or 'median') 
📝 Categorical Data: Fill missing values with the most frequent value (strategy = 'most_frequent')
✅ Pros: Fast, easy to implement, works well on small dataset.
❌ Cons: Ignores relationships between features, can distort variance and correlation.
```

### 2️⃣ Forward Fill / Backward Fill:
```
📌 Use the previous or next value to fill the missing value.
🎯 Best use case: Time Series Data (Stock prices, Weather data, Sensor readings)
```
  
### 3️⃣ KNNImputer: 
```
📌 Fills missing values using K Nearest Neighbours (similarity).
✅ Pros: Preserve feature relationships, handles correlated features.
❌ Cons: Computationally expensive, slow on large datasets, requires feature scailing.
```

### 📊 SimpleImputer vs KNNImputer

Feature |	SimpleImputer |	KNNImputer
:--- | :--- | :---
Speed | ⚡ Fast |	🐢 Slow
Dataset Size | Small datasets | Large datasets
Feature Relationships |	❌ Ignores |	✅ Preserves
Variance & Correlation | Can distort | Better preserves
Scaling Required |	❌ No |	✅ Yes

### ⚠️ Important things to consider:
```
1️⃣ fit() → Learns the values needed for imputation.

Example:
  Mean = 30
  Median = 28
  Mode = Bengaluru

👉🏻 Only learns, does not fill.

2️⃣ transform() → Uses the learned values to fill missing data.

👉🏻 Applies the imputation.

3️⃣ fit_transform() → Performs both steps together in one operation.

✅ Learn
✅ Fill

🚨 Never apply on test set to avoid data leakage.
```
- **fit_transform():** Learn and apply the values in one step (Apply only on the training set)
- Never apply **fit_transform()** on test set to avoid data leakage.

```python
# DataFrame.fillna()
df.fillna('🌞')

# DataFrame.Series.fillna()
df['Sales'].fillna(0)
```

### 🚨 Data Leakage 
```
✅ Data Leakage happens when a model gets access to information it should not have during training.
✅ Model make unrealistically good predictions, but it won't be available in the real world.
```

🎓 Simple Example
```
Imagine a student taking an exam 📚.

Normal Situation → Student studies before the exam. Takes the exam honestly.

Data Leakage Situation → Student secretly sees the answer sheet before the exam.

😄 Of course, the score will be very high! But that doesn't reflect the student's actual knowledge.
```

### 🚩 Common Causes of Data Leakage
```
1️⃣ Using Future Information → Using data that won't be available at prediction time.

2️⃣ Fitting Preprocessing on the Entire Dataset

Examples:
  Scaling
  Encoding
  Imputation

Before train-test split. Which is ❌ Wrong.

3️⃣ Duplicate Records → The same records appear in both training and test sets.

4️⃣ Target Leakage → Using a feature that directly reveals the target variable.

Example: Predicting loan default while using a feature like: "Loan Default Status"

😄 The answer is already present!
```

### ❌ Incorrect Approach
```
❌ Imputation on testing set using fit_transform(X_test): Learns (mean, median, mode) from test dataset instead of predicting.
✅ Always apply only transform(X_test) on test dataset.
❌ Feature Engineering using target variable: Creating a feature that uses the target data.
✅ Always apply Feature Engineering on training dataset and preprocess after splitting data.
```

### 🛟 Preventive Measures
```
✅ Split data into train and test sets first
✅ Fit preprocessing only on training data
✅ Use proper cross-validation
✅ Avoid any target reference into feature engineering or preprocessing
✅ For time series data always order data according to timestamp chronology.
```

### ⚠️ Disadvantages of Imputation
```
Although imputation helps keep data, it is still an estimate, not the actual value.
Because of this, imputation can change the original characteristics of the dataset.

1️⃣ Changes Statistical Properties:
  Mean
  Median
  Mode
  Variance
  Standard Deviation
When we replace missing values with estimated values, these statistics can change.

2️⃣ Can Distort the Data Distribution:
  Imputation may make the data look different from reality.

3️⃣ Can Introduce Skewness or Outliers:
  Sometimes imputation creates unnatural patterns.

4️⃣ Changes Feature Relationships:
  Changes correlation betwwen the features, impacting model accuracy
```

<h3 name="assign">🏷️ 3. Assign a Unique Category (Categorical Data) | Flag (Numeric Value)</h3>

```
✅ Instead of deleting or estimating missing values, we explicitly mark them as missing.
✅ Assign a unique category for missing data or use a "Missing" flag (binary flag)
✅ Allows the model to know that the value was missing rather than guessing a replacement value.

1️⃣ For Categorical Data: Assign a Unique Category
2️⃣ For Numerical Data: Use a Missing Flag
🚨 Important Note: Only use -1 or 0 if they are not valid values in the dataset.

🎯 Better Approach: Missing Indicator Flag
Instead of replacing with special values only, create an additional flag column.

✅ Advantages
  ✔️ Keeps all records
  ✔️ Simple and fast
  ✔️ No need to estimate values
  ✔️ Preserves original data distribution
  ✔️ Missingness itself can become a useful feature

❌ Disadvantages
  ❌ Special values may be confused with real values
  ❌ Doesn't recover the actual missing information
  ❌ May not work well if many values are missing
```

<h3 name="predict">🤖 4. Predict Missing Value</h3>

```
✅ Instead of filling missing values with: Mean, Median, or Mode
✅ We use other features in the dataset to predict the missing values.
✅ Use the information we already have to estimate the missing value more intelligently.

✅ Advantages
  ✔️ Preserves relationships between features
  ✔️ More accurate than mean/median imputation
  ✔️ Better maintains correlations
  ✔️ Often improves model performance

❌ Disadvantages
  ❌ More complex
  ❌ Computationally expensive
  ❌ Prediction errors can introduce bias
  ❌ Requires enough non-missing data to train a model
```

### 🔄 How It Works
```
1️⃣ Separate rows into:
  Non-Missing Rows → These rows become the training set.
  Missing Rows → These rows become the prediction set (test set).

2️⃣ Train a model using non-missing rows.

3️⃣ Use the trained model to predict the missing values.

4️⃣ Fill the dataset with the predicted values.
```

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
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42, stratify=y)

# Parameters: stratify=y (Maintain class distribution, important for classification)
```

### ⏳ Interpolation (Special Case for Time Series)
```
Interpolation estimates missing values based on nearby values over time.

It is commonly used in:
  📈 Stock prices
  🌦️ Weather data
  📡 Sensor readings
  💰 Sales forecasting

🎯 When to Use Interpolation?
  ✅ Time-series data
  ✅ Sequential data
  ✅ Data with trends over time
```

<h3 name="algo">🤖 5. Use algorithms that handles missing values</h3>

```
1️⃣ KNN (K-Nearest Neighbors)
KNN looks for the most similar data points (nearest neighbors) and uses them to estimate missing values or make predictions.

✅ Pros
  ✔️ Preserves relationships between features
  ✔️ Works well when similar records exist

❌ Cons
❌ Slow on large datasets
❌ Requires feature scaling
```

- **KNN:** Fills missing values by looking at the K nearest values (Focus on nearby data points)
- **Random Forest:** Trains weak models using non-missing data and uses missing values for testing.
- **SVM:** Focuses on support vectors (data points close to the decision boundary/hyperplane)
- Experiment with different algorithms and compare their performance on specific datasets.

### Domain Knowledge
- It helps us understand the missing patterns, whether it’s random or due to an error.
- Knowing the cause can guide us in deciding the best way to handle the missing data.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
