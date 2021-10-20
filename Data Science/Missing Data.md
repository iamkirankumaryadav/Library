<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to deal with missing data ?

**Missing data** : `NULL` | `NAN` | `nan` | `NaN` ( Ignored while **arithmetic operations** )

`Row` | `Observation` | `Tuple` | `Sample` | `Record`

`Column` | `Feature` ( Data Science ) | `Field` ( Excel ) | Atrribute | Dimension

<h3><a href="#del">Drop</a> | <a href="#impute">Impute</a> | <a href="#assign">Assign</a> | <a href="#predict">Predict</a> | <a href="#algo">Algorithm</a></h3>

<h3 name="del"> 1. Drop ( dropna( ) )</h3>

- `Drop` **observations** if it has a `NULL` value for particular **columns** ( Rows of `missing` data < `5%` | `axis = 0` )
- `Drop` **columns** if **missing values** > `70%` | `axis = 1`
- Deleting irrelevant **rows** or **columns** helps to get a **robust model**.
- But it's **better** to keep data than `dropping`, removing data may lead to `loss` of important information.
- If one value in observation is `missing` other values in the observations may be **important**.

<h3 name="impute"> 2. Impute ( fillna( ) )</h3>

- `Impute` the `numerical` missing data with `mean` or `median` ( SimpleImputer : `strategy` = `'mean'` or `'median'` ) 
- `Impute` the `categorical` missing data with `most frequent` ( SimpleImputer : `strategy` = `'most_frequent'` ) 
- `SimpleImputer()` is used to `fill` the missing value ( **Univariate imputation** ) 
- `fit()` : Learn the values ( `Mean`, `Median`, `Mode` ) to be imputed and `transform()` : `Fill` the missing values.
- `KNNImputer()` : **Fill** missing data with the help of **K Nearest Neighbors**.
- Prevent from data loss but can cause **data leakage**.

### Data Leakage 
- Accidently sharing data between the `train` set and `test` set.

### Disadvantage

- Changes the `distribution` of dataset ( `Mean`, `Median`, `Variance` and `Standard Deviation` )
- Brings new `outliers`.
- Changes the `correlation` among data ( `Features` ).

<h3 name="assign"> 3. Assign a Unique Category ( Categorical Data ) | Flag ( Numeric Value )</h3>

- Assign a **unique** category for data with **missing values** or assign with `"Missing"` flag.
- **Flag** the **numeric** missing data with `-1` or `0` 
- Create difference between missing data and remaining non missing data.

<h3 name="predict"> 4. Predict Missing Value</h3>

- `Fill` missing data with the help of other **features** by **predicting** ( **Multivariate** imputation ) 
- Use the non missing data as **train** set and missing data as **test** set.
- `Continuous` and `Categorical` data can be used for `Prediction` and `Classification`.
- `Interpolation` : `Predict` missing data with the range of `Date` and `Time` ( Time Series `Forecasting` ) 

<h3 name="algo"> 5. Use algorithms which works fine with missing values</h3>

- `KNN` fills missing value by taking the majority of the `K nearest` values.
- `Random forest` works well on **non linear** and **categorical data**.
- Weak learners are trained by **non missing** data and tested on data with **missing** values.

### Domain Knowledge can also help us to deal with the missing data.

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
