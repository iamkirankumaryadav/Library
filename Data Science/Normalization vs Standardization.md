<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Transform | Normalize | Standardize | Rescale | Scaling

**Data Set** contains **Features** with Different Range of Values, so we **Normalize** or **Standardize** Data to bring down to Same **Range** | **Scale**

Data Normalization | Data Standardization ( Z Score Normalization )
:--- | :---
x ( **Normal** \| **Rescaled** ) =  x - **min** ( x ) / **max** ( x ) - **min** ( x ) | z = x - **mean** ( x ) / **std** ( x )
**Rescale** Feature Value between **Range** `0` and `1` | **Mean** = `0` and **Standard Deviation** = `1`
sklearn.preprocessing.`MinMaxScaler()` | sklearn.preprocessing.`StandardScaler()`
Use for **Neural Networks** ( ANN, CNN, RNN ) | Algorithms that rely on **Gradient Descent**, **Distance** and **Dimensions**

### Scaling 
- Convert **Numeric** Feature values from their `Natural` **Range** ( e.g. 100 to 900 ) into a `Standard` or `Normal` **Range**.
- A Feature Set with only One Feature do not need Scaling, Beneficial only if the Feature Set consists of **Multiple Features**.

### Data Standardization ( Z Score Normalization )
- Standardize **Features** around center ( `Mean` ) | Equalize the Range or Data **Variability**.
- Important when we **Compare** Measurements that have Different **Units**.

Where to **Use** ? | Where **not** to **Use** ?
:--- | :---
Algorithms that rely on **Gradient Descent** ( **Regressions** ) | **Probability** based Algorithms : **Naive Bayes**
**Distance** based Algorithms ( **KNN**, **K Mean**, **Clusterings** and **SVM** ) | **Tree** based Algorithms : CART, Decision Trees.  
**Dimensionality Reduction** Transformers ( **PCA**, **LDA** and **t-SNE** ) | **Ensemble Learning Techniques** : Bagged Trees and Boosted Trees

### Benefits 
1. Helps **Gradient Descent** Converge ( Achieve Global Minima ) more Quickly.
2. Helps the Model to Learn Appropriate **Weights** for Each **Feature** ( Model Pay more Attention to the Features having `High` **Range** )
3. Otherwise, Feature with `High` **Range** is given more **Importance** as compared to Feature with `Low` **Range** even if it is Better Feature.
4. Reduce the Effect of the Features with **Larger Scale** which plays a **Dominating Role** in the Model and the Effect of **Outlier**.

### Transformation

- **Split** the Data Set into `Train` Set and `Test` Set.
- Application of the Same **Calculation** to Each and Every Data Point in `Train` Set and `Test` Set ( No need to Scale **Dependent Variable** )
- `fit( )` : **Learn Parameters** and **Scales** of Data which will be needed to **Transform** the Data | Applied on `Train` Set.
- `transform( )` : **Transforms** Data on the basis of what it **Learns** from **fit( )** | Applied on `Test` Set.
- `fit_transform( )` : First Learn ( **Fit** ) and then Apply in place ( **Transform** )
- Applies Same **Transformation** to both Sets of Data ( `Train` Set and `Test` Set ) keeps **Consistency** and Prevents **Data Leakage**.
- **Data Leakage** :  **Sharing Information** of **Test Set** with **Train Set**.

### How to Prevent Data Leakage 
- Never Apply `fit_transform()` on Test Set.
- Remove `Duplicate` Data ( `drop_duplicates( )` )
- Time Series Data : Train Set should contain Past Data and Test Set should contain New Data based on Date ( `Sort` Dataset by Date ) 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
