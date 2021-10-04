<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Transform | Normalize | Standardize | Rescale | Scaling

**Data Set** contains **Features** with different range of values, so we **Normalize** or **Standardize** data to bring down to same **Range** | **Scale**.

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
1. Helps **Gradient Descent** to `Converge` ( Achieve Global Minima ) more quickly.
2. Helps the model to learn appropriate `Weights` for each **Feature** ( Model pay more attention to the features having `High` **Range** )
3. Otherwise, Feature with `High` **Range** is given more **Importance** as compared to feature with `Low` **Range** even if it is better Feature.
4. `Reduce` the effect of the features with **Larger Scale** which plays a **Dominating Role** in the model and the effect of **Outlier**.

### Transformation

- **Split** the data set into `Train` set and `Test` set.
- Application of the same **Calculation** to each and every data point in `Train` set and `Test` set ( No need to scale **Dependent Variable** )
- `fit()` : **Learn Parameters** and **Scales** of data which will be needed to **Transform** the data | Applied on `Train` set.
- `transform()` : **Transforms** data on the basis of what it **Learns** from **fit( )** | Applied on `Test` set.
- `fit_transform()` : First Learn ( **Fit** ) and then apply in place ( **Transform** )
- Applies same **Transformation** to both sets of data ( `Train` Set and `Test` Set ) keeps **Consistency** and prevents **Data Leakage**.
- **Data Leakage** :  **Sharing information** of **Test Set** with **Train Set**.

### How to Prevent Data Leakage 
- Never Apply `fit_transform()` on Test Set.
- Remove `Duplicate` Data ( `drop_duplicates()` )
- Time Series Data : Train set should contain past data and Test set should contain new data based on date ( `Sort` Dataset by Date ) 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
