<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Logistic Regression

- `Model` used for `classification`, tasks like classifying flower species or image recognition.
- Especially `binary` classification | Assign observations to a `discrete` set of classes.
- Predict the `probability distribution` of class which lies within Range `0` and `1`.
- Transforms output using `Sigmoid` function to return a `probability distribution` value ( Mapped to 2 `discrete` classes )
- Explain relationship between one dependent **binary** variable and one or more **nominal** or **ordinal** independent variable.
- Logistic regression is affected by the scale, so always `standardize` the features before applying logistic regression. 

### Logistic Function  | Sigmoid ( S Shaped Curve ) Function
- Accepts any `real` value and map it into a value between `0` and `1`
- The probability prediction must be transformed to `binary` | dichotomous ( `0` and `1` )
- Threshold | Decision boundary : 0.5 ( `Probability` < `0.5` is considered as `0` else `1` )

### When to Use Logistic Regression
- **Binary** target variable | Performs will with a small number of observations.
- **Fair** data ( Not to many `outliers` or `missing` data in the data set ) 
- Logistic regression is good for **fast training** ( It is not the best performing model )
- No tuning is usually required.

### Remove Correlated Independent Feature
- The model can `overfit` if you have multiple highly correlated independent features.
- Calculate the pairwise correlations between all independent features and removing highly correlated independent feature.

### Example
- **Linear regression** helps us to predict the student's test score on a scale of 0 - 100 | `Continuous`
- **Logistic regression** helps us to classify whether the student is passed or failed | `Discrete`

### Types of Logistic Regression
1. Binary (Pass(1) | Fail(0))
2. Multiclass or Multinomial (Cats | Dogs | Sheep)
3. Ordinal (Low | Medium | High)

```python
# Binary Classification

import seaborn as sns
import pandas as pd

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression

from sklearn import metrics

# Import the dataset :
df = pd.read_csv("Data.csv")

# Split the data set :
X_train, X_test, y_train, y_test = train_test_split(df["indepenedent variable"], df["target variable"], random_state = 0]

# Standardize the data ( Mean = 0 and Std = 1 )
scaler = StandardScaler()

# Fit the training data : 
scaler.fit(X_train)

# Apply transform on train set and test set :
X_train = scaler.transform(X_train)
X_test = scaler.transform(X_test)

# logistic Regression ( 1. Import the model )
model = LogisticRegression()

# Model learn from data
model.fit(X_train, y_train)

# Prediction and Prediction Probability
print(f"Prediction : {model.predict(X_test[0].reshape(1,-1))[0]}")
print(f"Probability : {model.predict_proba(X_test[0].reshape(1,-1))}")

# Measuring model performance
score = model.score(X_test, y_test) # Accuracy

# Confusion metrics
cm = metrics.confusion(y_test, model.predict(X_test))

```

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
