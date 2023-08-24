<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Transform | Normalize | Standardize | Rescale | Scaling

- **Data set** contains **features** with different range of values. 
- We `normalize` or `standardize` data to bring down to the same `range` or `scale`
- It helps in improving the `accuracy` and `performance` of the models.

Data Normalization | Data Standardization ( Z Score Normalization )
:--- | :---
`x` ( **Normal** ) =  x - **min** ( x ) / **max** ( x ) - **min** ( x ) | `z` = x - **mean** ( x ) / **std** ( x )
**Rescale** feature value between **range** `0` to `1` | **Mean** = `0` and **standard deviation** = `1`
sklearn.preprocessing.`MinMaxScaler()` | sklearn.preprocessing.`StandardScaler()`
Use for **neural networks** ( ANN, CNN, RNN ) | Algorithms that rely on **gradient descent**, **distance** and **dimensions**

### Scaling 
- Convert **numeric** feature values from their `natural` **range** into a `standard` or `normal` **range**.
- A dataset with only one feature do not need scaling.
- Scaling is beneficial only if the dataset consists of **multiple** features with different range.

### Data Standardization ( Z Score Normalization )
- Standardize features around center ( `Mean` ) 
- Equalize the range or data **variability**.
- Important when we **compare** measurements that have different **units**.

Where to **Use** ? | Where **not** to **Use** ?
:--- | :---
Algorithms that rely on **gradient descent** ( **Regressions** ) | **Probability** based algorithms : **Naive Bayes**
**Distance** based algorithms ( **KNN**, **K Mean** and **SVM** ) | **Tree** based algorithms : CART, Decision trees.  
**Dimensionality reduction** transformers ( **PCA**, **LDA** and **t-SNE** ) | **Ensemble learning techniques** : Bagged and boosted trees

### Benefits 
1. Helps **gradient descent** to `converge` ( Achieve global minima ) more quickly.
2. Helps the model to learn appropriate `weights` for each **feature**.
3. Model pay more attention to the features having `high` **range** even if the feature is irrelevant.
4. Feature with `low` **range** are ignored even if it is better feature for model training.
5. **Larger scale** features plays a **dominating role** in the model. 
6. Reduces the **effect** of `outlier`

### Transformation

- **Split** the data set into `train` set and `test` set.
- Apply same **transformation** on `train` set and `test` set ( Keep consistency )
- No need to scale **dependent variable** | `Feature vector` 
- `fit()` : Learn **parameters** and **scales** of data which will be needed to **transform** the data | Apply only on `train` set.
- `transform()` : **Transforms** data on the basis of what it **learns** from `fit()` | Apply on `train` and `test` set.
- `fit_transform()` : First learn ( **Fit** ) and then apply in place ( **Transform** ) | Apply only on `train` set.
- Prevents **data leakage** : **Sharing information** of **train set** with **test set**.

```python
# Create instance:
scaler = StandardScaler()

# Fit on train set:
scaler.fit(X_train)

# Transform on train and test set:
X_train = scaler.transform(X_train)
X_test = scaler.transform(X_test)
```

### How to Prevent Data Leakage 
- Never apply `fit_transform()` on test set.
- Remove `duplicate` data ( `drop_duplicates()` )
- Time series data : Train set should contain past data and test set should contain new data based on date, `Sort` by date.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
