<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Transform | Normalize | Standardize | Rescale | Scaling

Normalization | Standardization ( Z Score Normalization )
:--- | :---
x ( **Normal** | **Rescaled** ) =  x - **min** ( x ) / **max** ( x ) - **min** ( x ) | z = x - **mean** ( x ) / **std** ( x )
**Range** between `0` and `1` | **Mean** = `0` and **Standard Deviation** = `1`
sklearn.preprocessing.`MinMaxScaler()` | sklearn.preprocessing.`StandardScaler()`
Use for **RNN**, **CNN**, **Images** ( Neural Networks ) | Algorithms that uses **Gradient Descent** and Calculate **Distance** 

### Data Normalization
- **Rescale** Feature values range between 0 and 1
- Data Set may contain two **Features** with Different Range of Values, so we **Normalize** Data to bring down to Same **Range** | **Scale**

Where to **Use** ?
- Normalization works for Deep Learning well ( CNN, RNN ) and even for Images.
- Standard Scaler is Better than Normalization in most cases.

### Min Max Scaling
- x ( **Rescaled** ) =  x - **min** ( x ) / **max** ( x ) - **min** ( x )

### Scaling 
- Converting **Floating Point** Feature values from their Natural Range (e.g. 100 to 900) into a Standard Range ( e.g. 0 to 1 or -1 to 1 )
- A Feature Set consisting only Single Feature, Scaling provides little to no practical benefit.
- Scaling is Beneficial if the Feature Set consists of **Multiple Features**.

### Data Standardization ( Z Score Normalization )
- z = x - **mean** ( x ) / **std** ( x )
- **Mean** = 0 and **Standard Deviation** = 1
- Standardizing **Features** around center | Equalize the Range or Data **Variability**
- Important when we **Compare** Measurements that have Different **Units**

Where to **Use** ?
- Algorithms that rely on Gradient Descent ( **Regression** )
- Algorithms that Calculate Distance ( KNN, K Mean, Clusterings, SVM )
- Dimensionality Reduction Transformer Classes ( PCA, LDA, t-SNE )

Not to **Use** 
- Probability based Algorithms : Naive Bayes
- Trees based Algorithms : CART, Decision Trees and Ensemble Techniques ( Random Forest, Bagged Trees and Boosted Trees ).

### Benefits 
1. Helps **Gradient Descent** Converge more Quickly
2. Helps the Model to Learn Appropriate Weights for Each Feature. ( Model Pay more Attention to the Features having Wider Range )
3. Reduce the Effect of the Features with **Larger Scale** which plays a Dominating Role in the Model and the Effect of **Outlier**

### Transformation
- Application of the Same **Calculation** to Each and Every Data Point.
- **fit( )** : Transformer Learns something about Data ( Mean, Scale and Statistics ) | Applied on Train Set
- **transform( )** : Transforms Data on the basis of what it **Learns** from Data | Applied on Test Set
- **fit_transform( )** : First Learn ( **Fit** ) and then Apply in place ( **Transform** )
- Applies Same **Transformation** to both Sets of Data ( **Train Set** and **Test Set** ) keeps **Consistency** and Prevents **Data Leakage**.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
