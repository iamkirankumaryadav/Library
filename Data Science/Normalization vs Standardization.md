# Normalize | Standardize | Rescale | Scaling

### Normalization
- **Rescale** Feature values range between 0 and 1.
- Data Set may contain two **Features** with Different Range of Values.
- So we **Normalize** Data to bring in Same **Range**.
- - x(**Normal**) =  x - **min**(x) / **max**(x) - **min**(x)

### Scaling :
- Converting **Floating Point** Feature values from their Natural Range (e.g. 100 to 900) into a Standard Range (e.g. 0 to 1 or -1 to 1)
- A Feature Set consisting only Single Feature, Scaling provides little to no practical benefit.
- Scaling is Beneficial if the Feature Set consists of **Multiple Features**.

### Benefits :
1. Helps **Gradient Descent** Converge more Quickly.
2. Helps the Model Learn Appropriate Weights for Each Feature. ( Model Pay more Attention to the Features having Wider Range )

### Min Max Scaling
- x(**Rescaled**) =  x - **min**(x) / **max**(x) - **min**(x)

### Standardization (Z Score Normalization)
- z = x - **mean**(x) / **std**(x)
- **Mean** = 0 and **Standard Deviation** = 1
- Standardizing **Features** around center | Equalize the Range or Data **Variability**
- Important when we **Compare** Measurements that have Different **Units**

### Transformation
- Application of the Same Calculation to Every Point of the Data separately.
