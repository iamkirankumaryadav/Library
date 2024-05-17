<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Normalization | Standardization | Rescaling

- Dataset contains independent features with different ranges/scales of values. 
- We normalize/standardize data to bring it down to the same range/scale.
- Important for the models that depend on distance calculations like Linear Regression, KNN, K Mean, and SVM.
- Decision Trees and Ensemble Learnings do not require data normalization.

Data Normalization | Data Standardization ( Z Score Normalization )
:--- | :---
**x(normal) =  x - min(x) / max(x) - min(x)** | **z = x - mean(x) / std(x)**
Rescale feature value between the range 0 and 1 | Rescale features to have the **mean = 0** and **standard deviation = 1**
**sklearn.preprocessing.MinMaxScaler()** | **sklearn.preprocessing.StandardScaler()**

### **Scaling:**
- Convert numeric feature values from their natural range into a standard range.
- A dataset with only one feature doesn't need scaling, it's beneficial only with multiple features of different ranges.

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
- **x(new) = x - min(x) / max(x) - min(x)**

<table>
  <tr><th colspan=2>Before Normalization</th><th colspan=2>After Normalization</th></tr>
  <tr><td>Age</td><td>Salary</td><td>Age</td><td>Salary</td></tr>
  <tr><td>20</td><td>45000</td><td>0</td><td>0</td></tr>
  <tr><td>30</td><td>250000</td><td>0.33</td><td>0.45</td></tr>
  <tr><td>40</td><td>150000</td><td>0.66</td><td>0.23</td></tr>
  <tr><td>50</td><td>500000</td><td>1</td><td>1</td></tr>
</table>

```python
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()

wine[wine.columns] = scaler.fit_transform(wine[wine.columns])
```

### Data Standardization (Z-Score Normalization) | Standard Score
- **z = x - mean / std** (z: specific data point)
- How many standard deviations a specific data point is away from the mean of a dataset?
- How far a particular value is away from the average value.
- A Z-score of 0 means that the data point is exactly at the mean.
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
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

wine[wine.columns] = scaler.fit_transform(wine[wine.columns])
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

### Benefits 
1. Helps the gradient descent to converge (Achieve global minima) more quickly.
2. Helps the model to learn appropriate weights for each independent feature.
3. The model pays more attention to features with a high range even if the feature is irrelevant.
4. A feature with a low **range** is ignored even if it is a better feature for model training.
5. Large-scale features play a dominating role in the model. Scaling discourages domination.
6. Reduces the effect of outliers. Improves the model's accuracy and performance.

### **Transformation:**
- Split the data set into a train set and a test set.
- Apply the same transformation on the train set and the test set (Consistency)
- No need to scale dependent variable | target vector.
- **fit():** Learn parameters and scales of data which will be needed to transform the data | Apply only on a train set.
- **transform():** Transforms data based on what it learns from **fit()** | Apply on the train and test set.
- **fit_transform():** First learn and then apply in place | Apply only on the train set.
- Prevents **data leakage**: **Sharing information** of **train set** with **test set**.

```python
# Create instance:
scaler = StandardScaler()

# Fit on train set:
scaler.fit(X_train)

# Transform on train and test set:
X_train = scaler.transform(X_train)
X_test = scaler.transform(X_test)
```

### **How to Prevent Data Leakage?**
- Never apply **fit_transform()** on the test set.
- Remove duplicate data using **drop_duplicates()**.
- **Time series data:** The train set should contain the past data and the test set should contain the new data, sorted by date.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
