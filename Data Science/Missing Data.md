<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to Deal with Missing Data ?

**Missing Data** : `NULL` | `NAN` | `nan` | `NaN` ( Ignored while **Arithmetic Operations** )

#### Row | Observation | Tuple

#### Column | Feature | Field

<h3><a href="#del">Drop</a> | <a href="#impute">Impute</a> | <a href="#assign">Assign</a> | <a href="#predict">Predict</a> | <a href="#algo">Algorithm</a></h3>

<h3 name="del"> 1. Drop ( dropna( ) )</h3>

- `Drop` **Observations** if it has a `NULL` value for particular **Columns** ( Rows of `Missing` Data < `5%` | `axis = 0` )
- `Drop` **Columns** if ( **Missing Values** > `70%` | `axis = 1` )
- Deleting irrelevant **Rows** or **Columns** helps to get a **Robust Model**.

It is **Better** to keep data than to `Drop` it, Removing data may lead to `Loss` of important information.

If one value in observation is `Missing` other values in the observations may be important.

<h3 name="impute"> 2. Impute ( fillna( ) )</h3>

- `Impute` the `Numerical` missing data with `Mean` or `Median` ( **Univariate** Imputation ) 
- `Impute` the `Categorical` missing data with `Mode` or `Most Frequent` (  **Univariate** Imputation ) 
- `SimpleImputer()` is used to `Fill` the missing value ( **Univariate Imputation** ) 
- `fit()` : Learn the values ( `Mean`, `Median`, `Mode` ) to be imputed and `transform()` : `Fill` the missing values.
- `KNNImputer()` : **Fill** missing data with the help of **K Nearest Neighbors**.
- `IterativeImputer()` : 
- Prevent from data loss but can cause **Data Leakage**.

### Data Leakage 
- `Sensitive` information is shared with an `Unauthorized` user.
- Accidently sharing data between the `Train` and `Test` set.

### Disadvantage

- Change the `Distribution` of dataset ( `Mean`, `Median`, `Variance` and `Standard Deviation` )
- Bring new `Outliers`.
- Change the `Correlation` among data ( `Features` ).

<h3 name="assign"> 3. Assign a Unique Category ( Categorical Data ) | Flag ( Numeric Value )</h3>

- Assign a **Unique** category for data with missing values or assign with `"Missing"` flag.
- **Flag** the **Numeric** missing data with `-1` or `0` ( Create difference between missing data and remaining non missing data ) 

<h3 name="predict"> 4. Predict Missing Value</h3>

- `Fill` missing data with the Help of other **Features** by **Predicting** ( **Multivariate** Imputation ) 
- `Continuous` and `Categorical` data can be used for `Prediction` and `Classification`.
- `Interpolation` : `Predict` missing data with the range of `Date` and `Time` ( Time Series `Forecasting` ) 

<h3 name="algo"> 5. Use Algorithms which works fine with missing values</h3>

- **KNN**, **Naive Bayes** and **Random Forest**.
- **KNN** works on principle of **Distance Measure**.
- **KNN** fills missing value by taking the majority of the **K Nearest** values.
- **Random Forest** works well on **Non Linear** and **Categorical Data**.
- Weak learners are trained by non missing data and tested on data with missing values.

### Domain Knowledge can also help us to Deal with the Missing Data.

```python
from sklearn.linear_model import LinearRegression
import pandas as pd

data = pd.read_csv("train.csv")
data = data[["Survived", "Sex", "Age"]]

test_set = data[data["Age"].isnull()] # Missing Data will be Test Set

data.dropna(inplace=True) # Remaining Data ( Non Null ) will be used for Training the Model

y_train = data["Age"]
X_train = data.drop("Age", axis=1)
X_test = test_set.drop("Age", axis=1)

model = LinearRegression()
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
```

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
