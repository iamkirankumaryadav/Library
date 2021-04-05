<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Normalize | Standardize | Rescale | Scaling

Normalization | Standardization
:--- | :---
x ( **Normal** ) =  x - **min** ( x ) / **max** ( x ) - **min** ( x ) | z = x - **mean** ( x ) / **std** ( x )
**Range** between `0` and `1` | **Mean** = `0` and **Standard Deviation** = `1`
sklearn.preprocessing.`MinMaxScaler()` | sklearn.preprocessing.`StandardScaler()`
Use for **RNN**, **CNN**, **Images** | Algorithms that uses **Gradient Descent** and Calculate **Distance**

### Data Normalization
- **Rescale** Feature values range between 0 and 1
- Data Set may contain two **Features** with Different Range of Values
- So we **Normalize** Data to bring down to Same **Range** | **Scale**
- x ( **Normal** ) =  x - **min** ( x ) / **max** ( x ) - **min** ( x )

**Techniques** : 
- Preprocessing.`MinMaxScaler()`

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
- Algorithms that Calculate Distance ( KNN, K Mean, Clusterings )

Not to **Use** 
- Trees : Decision Trees and Ensemble Techniques.

**Techniques** 
- Preprocessing.`StandardScaler()`

### Benefits 
1. Helps **Gradient Descent** Converge more Quickly
2. Helps the Model Learn Appropriate Weights for Each Feature. ( Model Pay more Attention to the Features having Wider Range )
3. We Reduce the Effect of the Features with **Larger Scale** which plays a Dominating Role in the Model
4. We Reduce the Effect of **Outlier**

### Transformation
- Application of the Same Calculation to Every Point of the Data separately.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
