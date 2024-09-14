<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Normalization | Standardization | Rescaling**

- A technique used in ML to rescale numerical features from their natural range to a standard range, typically between 0 to 1 or -1 to 1.
- Dataset contains independent features with different ranges/scales of values. Depending on their units of measurement.
- Data is normalized/standardized/rescaled to bring it down from their natural range/scale to a standard/normal range.
- This process is essential for ensuring that the features are trained equally and contribute equally to the model's predictions.
- It also prevents the model from being biased towards features with a larger magnitude/scale/range.
- Important for the models that depend on distance calculations like Linear Regression, KNN, K Mean, and SVM.
- Decision Trees and Ensemble Learnings do not require data normalization.

**Data Normalization** | **Data Standardization (Z Score Normalization)**
:--- | :---
**x(normal) =  x - min(x) / max(x) - min(x)** | **z = x - mean(x) / std(x)**
Rescale feature value between the range 0 and 1 | Standardize features to have a **mean of 0** and a **standard deviation of 1**
**sklearn.preprocessing.MinMaxScaler()** | **sklearn.preprocessing.StandardScaler()**

### **Simple Feature Scaling:**
- **x(new) = x / max(x)**
<p>
<table>
  <tr><th colspan=2>Before Normalization</th><th colspan=2>After Normalization</th></tr>
  <tr><td>Age</td><td>Salary</td><td>Age</td><td>Salary</td></tr>
  <tr><td>20</td><td>45000</td><td>0.4</td><td>0.09</td></tr>
  <tr><td>30</td><td>250000</td><td>0.6</td><td>0.5</td></tr>
  <tr><td>40</td><td>150000</td><td>0.8</td><td>0.3</td></tr>
  <tr><td>50</td><td>500000</td><td>1</td><td>1</td></tr>
</table>

### **Min-Max Scaling:**
- **x(normal) = x - min(x) / max(x) - min(x)**

<table>
  <tr><th colspan=2>Before Normalization</th><th colspan=2>After Normalization</th></tr>
  <tr><td>Age</td><td>Salary</td><td>Age</td><td>Salary</td></tr>
  <tr><td>20</td><td>45000</td><td>0</td><td>0</td></tr>
  <tr><td>30</td><td>250000</td><td>0.33</td><td>0.45</td></tr>
  <tr><td>40</td><td>150000</td><td>0.66</td><td>0.23</td></tr>
  <tr><td>50</td><td>500000</td><td>1</td><td>1</td></tr>
</table>

```python
# Import the libraries:
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import MinMaxScaler

# Split the data:
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create a scaler:
scaler = MinMaxScaler()

# Fit the scaler on the training data:
scaler.fit(X_train)

# Transform both training and test data:
X_train_scaled = scaler.transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

### **Data Standardization (Z-Score Normalization) | Standard Score**
- **z = x - mean / std** (z: specific data point)
- How many standard deviations is a specific data point away from the mean of a dataset?
- How far a particular value is away from the average value of a dataset.
- A **Z-score** of 0 means the data point is exactly at the mean.
- Standardize features around the centre (Mean). Ranges from +3 (Above the mean) to -3 (Below the mean).

<table>
  <tr><th colspan=2>Before Normalization</th><th colspan=2>After Normalization</th></tr>
  <tr><td>Age</td><td>Salary</td><td>Age</td><td>Salary</td></tr>
  <tr><td>20</td><td>45000</td><td>-1.34</td><td>-1.13</td></tr>
  <tr><td>30</td><td>250000</td><td>-0.44</td><td>0.08</td></tr>
  <tr><td>40</td><td>150000</td><td>0.44</td><td>-0.51</td></tr>
  <tr><td>50</td><td>500000</td><td>1.34</td><td>1.56</td></tr>
</table>

```python
# Import the libraries:
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler

# Split the data:
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create a scaler:
scaler = StandardScaler()

# Fit the scaler on the training data:
scaler.fit(X_train)

# Transform both training and test data:
X_train_scaled = scaler.transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

Where to **use**? | Where **not** to **use** ?
:--- | :---
Gradient Descent based algorithms: Regressions | Probability-based algorithms: Naive Bayes
Distance-based algorithms: KNN, K Mean, and SVM | Tree-based algorithms: CART, and Decision Trees.  
Dimensionality reduction transformers: PCA, LDA and t-SNE | Ensemble learning techniques: Bagged and Boosted trees

Feature |	Euclidean Distance | Manhattan Distance
:--- | :--- | :---
Interpretation | Shortest straight line |	Total distance on a grid
Formula |	√((x1 - x2)² + (y1 - y2)²) |	abs(x1 - x2) + abs(y1 - y2)
Formula Description | The square root of the sum of squared differences between corresponding coordinates (x, y) of the two points | The sum of absolute differences between corresponding coordinates (x, y) of the two points
Visualization | Straight line	| Right-angle movements (Horizontal + Vertical)

### **Benefits** 
1. Helps the **gradient descent** to converge (reach the local minimum point) more quickly when features are normalized.
2. Helps the model to learn appropriate weights for each independent feature during training.
3. The model prioritizes the features with a high range even if the feature is irrelevant.
4. A feature with a low **range** is ignored even if it is a better feature for model training.
5. Large-scale features play a dominating role in the model. Scaling discourages domination.
6. Help the model generalize better on unseen data by reducing the impact of outliers, improving the model's accuracy and performance.

### **Transformation:**
- Split the data set into a **train set** and a **test set**.
- Apply the same transformation on the **train set** and the **test set** (Consistency)
- No need to scale the dependent variable | target vector and categorical features (But needs encoding)
- **fit():** Learn parameters and scales of data that will be needed to transform the data. | Apply only on a train set.
- **transform():** Transforms data based on what it learns during **fit()** | Apply on the train and test set.
- **fit_transform():** First learn and then apply in place | Apply only on the train set.
- Prevents **data leakage**: **Sharing information** of **train set** with **test set**.
- Data Leakage happens when the scaling parameters calculated from the entire dataset are applied to the training and test sets. 

### **How to Prevent Data Leakage?**
- Split the dataset properly into training, validation and testing sets (No overlapping or replacement)
- Calculate the scaling parameters (mean, median, standard deviation, min, max, etc) exclusively on the training set.
- Use the scaling parameters obtained from the training set to transform both the training set and test sets.
- Never apply **fit_transform()** directly on the test set. Also, remove duplicate data using **drop_duplicates()**.
- **Time series data:** The train set should contain the past data and the test set should contain the new data, sorted by date.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
