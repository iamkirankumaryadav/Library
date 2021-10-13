<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Transform | Normalize | Standardize | Rescale | Scaling

**Data set** contains **features** with different range of values, so we **Normalize** or **Standardize** data to bring down to same **Range** | **Scale**.

Data Normalization | Data Standardization ( Z Score Normalization )
:--- | :---
`x` ( **Normal** \| **Rescaled** ) =  x - **min** ( x ) / **max** ( x ) - **min** ( x ) | `z` = x - **mean** ( x ) / **std** ( x )
**Rescale** Feature Value between **Range** `0` and `1` | **Mean** = `0` and **Standard Deviation** = `1`
sklearn.preprocessing.`MinMaxScaler()` | sklearn.preprocessing.`StandardScaler()`
Use for **Neural Networks** ( ANN, CNN, RNN ) | Algorithms that rely on **Gradient Descent**, **Distance** and **Dimensions**

### Scaling 
- Convert **Numeric** Feature values from their `Natural` **range** ( e.g. 100 to 900 ) into a `Standard` or `Normal` **range**.
- A feature set with only one feature do not need Scaling.
- Scaling is beneficial only if the feature set consists of **Multiple** features with different range.

### Data Standardization ( Z Score Normalization )
- Standardize features around center ( `Mean` ) | Equalize the range or data **Variability**.
- Important when we **compare** measurements that have different **Units**.

Where to **Use** ? | Where **not** to **Use** ?
:--- | :---
Algorithms that rely on **Gradient Descent** ( **Regressions** ) | **Probability** based Algorithms : **Naive Bayes**
**Distance** based Algorithms ( **KNN**, **K Mean**, **Clusterings** and **SVM** ) | **Tree** based Algorithms : CART, Decision Trees.  
**Dimensionality Reduction** Transformers ( **PCA**, **LDA** and **t-SNE** ) | **Ensemble Learning Techniques** : Bagged Trees and Boosted Trees

### Benefits 
1. Helps **gradient descent** to `converge` ( Achieve global minima ) more quickly.
2. Helps the model to learn appropriate `weights` for each **feature**.
3. Model pay more attention to the features having `high` **range** even if the feature is irrelevant.
4. Feature with `low` **range** are ignored even if it is better feature for model training.
5. **Larger scale** features plays a **dominating role** in the model. 
6. Reduces the **effect** of `outlier`

### Transformation

- **Split** the data set into `Train` set and `Test` set.
- Apply same **calculation** to each and every data point in `train` set and `test` set.  
- No need to scale **dependent variable** 
- `fit()` : Learn **parameters** and **scales** of data which will be needed to **transform** the data | Applied on `train` set.
- `transform()` : **Transforms** data on the basis of what it **learns** from **fit( )** | Applied on `test` set.
- `fit_transform()` : First learn ( **Fit** ) and then apply in place ( **Transform** ) | Applied only on `train` set
- Applies same **transformation** to both sets of data ( `Train` set and `test` set ) keeps **Consistency**
- Prevents **Data Leakage** : **Sharing information** of **train set** with **test set**.

### How to Prevent Data Leakage 
- Never apply `fit_transform()` on test set.
- Remove `duplicate` data ( `drop_duplicates()` )
- Time series data : Train set should contain past data and test set should contain new data based on date ( `Sort` dataset by date ) 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
