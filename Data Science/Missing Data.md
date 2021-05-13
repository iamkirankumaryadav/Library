<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to Deal with Missing Data ?

**Missing Data** : `NULL` | `NAN` | `nan` | `NaN` ( Ignored while **Arithmetic Operations** )

Rows : Observations and Column : Feature.

<h3><a href="#del">Drop</a> | <a href="#impute">Impute</a> | <a href="#assign">Assign</a> | <a href="#predict">Predict</a> | <a href="#algo">Algorithm</a></h3>

<h3 name="del"> 1. Drop ( dropna( ) )</h3>

- `Drop` Particular **Observation** if it has a `NULL` value for Particular **Feature**. ( Rows of `Missing` Data < `5%` | `axis = 0` )
- `Drop` Particular **Column** ( **Missing Values** > `70%` | `axis = 1` )
- Deleting an Irrelevant **Rows** or **Columns** helps to get a **Robust Model**.

> But it is **Better** to Keep Data than to **Discard** it, Removing Data may lead to **Loss** of **Important Information**.

<h3 name="impute"> 2. Impute | Fill ( fillna( ) )</h3>

- **Fill** | **Impute** the `Numerical` **Missing Data** with **Mean** or **Median** ( **Univariate** Imputation ) 
- **Fill** | **Impute** the `Categorical` **Missing Data** with **Mode** or **Most Frequent** (  **Univariate** Imputation ) 
- `SimpleImputer()` is used to Fill the Missing Value ( **Univariate Imputation** ) 
- `fit()` : Learn the Value to be Imputed and `transform()` : Fill the Missing Values.
- `KNNImputer()` : **Fill Missing Data** with the Help of **Nearest Neighbors**.
- `IterativeImputer()` : 
- Prevent from Data Loss but can cause **Data Leakage**.

### Disadvantage

- Changes the `Distribution` of Dataset ( `Mean`, `Median`, `Variance` and `Standard Deviation` )
- Bring New `Outliers`.
- Changes the `Correlation` among Data.

<h3 name="assign"> 3. Assign a Unique Category ( Categorical Data ) | Flag ( Numeric Value )</h3>

- Assign a **Unique Category** for Data with **Missing Values** or Assign with `"Missing"`.
- **Flag** the **Numeric Missing Data** with `-1` or `0` ( Create Difference between **Missing Data** and the Remaining Non Missing Data ) 

<h3 name="predict"> 4. Predict Missing Value</h3>

- **Fill Missing Data** with the Help of other **Features** | **Columns** by **Predicting** ( **Multivariate** Imputation ) 
- **Continuous** and **Categorical** Data can be used for **Prediction** and **Classification**.
- **Interpolation** : **Predict Missing Data** with the Range of **Date** and **Time** ( Time Series Data ) 
- This method will bring **Better Accuracy**. 

<h3 name="algo"> 5. Use Algorithm which Supports Missing Values</h3>

- **KNN**, **Naive Bayes** and **Random Forest**.
- **KNN** works on Principle of **Distance Measure**.
- **KNN** fills **Missing Value** by taking the **Majority** of the **K Nearest** Values.
- **Random Forest** works well on **Non Linear** and **Categorical Data**.

> **Domain Knowledge** can also help us to Deal with the **Missing Data**.

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
