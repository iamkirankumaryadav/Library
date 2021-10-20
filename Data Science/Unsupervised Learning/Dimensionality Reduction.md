<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Dimensionality Reduction

- `Unsupervised` Machine Learning. 
- Number of **features** ( `columns` ) should be low as compared to the number of **observations** ( `rows` ) in your dataset. 
- Certain algorithms struggles to **train** effective models ( Especially algorithms which consist `distance` calculations )

### Feature Selection

- `Select` only **relevant** features that make impact on target variable.
- `Filter` irrelevant or redundant features from your dataset.

### Feature Extraction
- Create a new dataset with relevant features that captures most of the **information** and **insights**. 

### Key difference between Feature Selection and Feature Extraction
- Feature **selection** keeps a subset of the `original` features. 
- Feature **extraction** creates a `new` subset.

### Variance Thresholds
- `Variance` is dependent on scale, always **normalize** your **features** first.
- Remove features whose values don't change much from observation to observation. 
e.g ( If a public health dataset contains 96% of observations for `35 years old men`, then age and gender features can be eliminated )

### Correlation Threshold
- Remove highly correlated features ( Multicollinearity )
- **Highly correlated** data provides **redundant** information.

### Principle Component Analysis ( PCA ) : Unsupervised | Numerical
- Dimensionality reduction method ( Reduce `dimensions`, explains `variance` and minimize `correlation` )
- **Transforming** large set of variables into small without **loss** of any information in large dataset.
- Reducing the number of **variables** of a dataset.
- `PCA` is used for `Numerical` Data only.

### Linear Discriminant Analysis ( LDA ) : Supervised | Categorical
- `LDA` is used especially for `categorical` data.
- Seperate `classes` or `labels`.
- Works better with large data set.

### Auto Encoder
- `Unsupervised` learning method, type of Artificial Neural Network.
- Learn and discover the **representation** and **structure** of dataset.
- Ignore noise in data. 

### Applications of Auto Encoders include:

1. Anomaly detection.
2. Removing noise from data ( Images, Audio )
3. Image inpainting | Conservation | Restoration ( **Reconstructing** missing part of an image )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
