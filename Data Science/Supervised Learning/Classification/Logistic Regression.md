<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Logistic Regression**
- A model used for classification tasks like classifying flower species or image classification.
- The logistic regression predicts the probability distribution of a binary outcome.
- Transforms any real number to a value between 0 (low) and 1 (high) using the Sigmoid/Logit function.  
- Probability of occurrence of the target label is predicted based on threshold (0.5) 
- The scale affects Logistic regression, so always standardize the features before applying logistic regression. 

### **Logistic | Logit | Sigmoid Function (S-Shaped Curve)**
- Accepts any real value and maps it into a value between 0 and 1.
- The probability prediction is transformed to binary | dichotomous (0 and 1)
- **Threshold:** 0.5 (Probability < 0.5 is considered as 0 else 1)

### **When to use Logistic Regression?**
- When the target variable has binary class labels, it performs well with a small number of observations.
- Data with very low outliers or missing data points in the data set. No tuning is usually required.

### How to find the relationship between the independent variable and target labels?
- Unlike regression, we can't use correlation to access the relationship.
- Data Visualization: Bar Charts, Histogram.
- **Statistical Test:** Chi-Square Test (Significant association between independent variable and dependent variables)
- Information Gain (High), Gini Index (Low) and Entropy (Low) in Decision Trees and Random Forests.
- **L1 Regularization:** Shrinks the coefficient of less important features towards zero.
- Features with large coefficients are considered more important.

### **Remove Correlated Independent Feature**
- The model can overfit if you have multiple highly correlated independent features.
- Calculate the pairwise correlations between all independent features and remove highly correlated independent features.

### **Example**
- Linear regression helps us to predict the student's test score on a scale of 0 - 100 | Continuous
- Logistic regression helps us to classify whether the student has passed (PASS) or failed (FAIL) | Discrete

### **Types of Logistic Regression**
- Binary (Pass(1) | Fail(0)  
- Multiclass (Cats | Dogs | Sheep)

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
X_train, X_test, y_train, y_test = train_test_split(df["independent variable"], df["target variable"], random_state = 0)

# Standardize the data ( Mean = 0 and Std = 1 )
scaler = StandardScaler()

# Fit the training data : 
scaler.fit(X_train)

# Apply transform on train set and test set :
X_train = scaler.transform(X_train)
X_test = scaler.transform(X_test)

# Logistic regression ( Create model object )
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

### **How to handle Multiclass classification problems?**
- Split the task into multiple binary classification datasets.
- Fit the binary classification model on each dataset. Set parameter **multi_class='ovr'**
- The model that predicts the highest class probability is the predicted class.

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, classification_report

# Load the Iris dataset:
df = pd.read_csv("iris.csv")

# Split data into features (X) and target variable (y):
X = df.drop("species", axis=1)
y = df["species"]

# Split data into training and testing sets:
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create a logistic regression model:
model = LogisticRegression(multi_class='ovr')  # One-vs-rest

# Train the model:
model.fit(X_train, y_train)

# Make predictions on the testing set:
y_pred = model.predict(X_test)

# Evaluate the model:
accuracy = accuracy_score(y_test, y_pred)
report = classification_report(y_test, y_pred)

print("Accuracy:", accuracy)
print("Classification Report:\n", report)
```

### OvR (One vs Rest) | OvA (One vs All)
Extends binary class classification to multiclass classification.
- digit 0 vs. digits 1, 2 and 3
- digit 1 vs. digits 0, 2 and 3
- digit 2 vs. digits 0, 1 and 3
- digit 3 vs. digits 0, 1 and 2

[Implementation](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/05.Logistic%20Regression%20for%20Multiclass%20Classification.ipynb)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
