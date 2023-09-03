<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# `Dimensionality Reduction`

- Dimensionality reduction is reducing the number of features in a dataset while preserving as much information as possible.
- Helps in improving the accuracy of models, simplifying data visualization, and making data easier to interpret.
- The number of **features** ( `columns` ) should be low compared to the number of **observations** ( `rows` ) in the dataset. 
- Certain algorithms struggle to **train** effective models ( Especially algorithms that consist of `distance` calculations )
- Algorithms that consist of distance calculations: `Regressions`, `KNN`, `K Mean` and `SVM`

### Feature `Selection`
- `Select` only features that make an impact on the target variable, `filter` irrelevant or redundant features from your dataset.
- `Feature Selection` keeps a subset of the `original` features. 

### Feature `Extraction`
- Creates a new dataset with only `relevant` features that capture most of the **information** and **insights**. 

### Variance `Thresholds`
- Variance represents how `spread out` the data points are with respect to each other in the dataset.
- `Variance` is dependent on `scale`, always `normalize` or `standardize` your features first.
- Remove features whose values don't change much from observation to observation. 
- e.g. If a health dataset contains 96% observations for `35 years` men, then age and gender features can be eliminated.

### Correlation `Threshold`
- Remove highly correlated features ( Multicollinearity ), and remove `redundant` information.

### Dimensionality reduction advantage
- Reduce `dimensions` ( # features ), explain `variance` and minimize `correlation` ( redundancy )

### Principle Component Analysis `PCA`: Unsupervised | Numerical
- `Transforms` large data sets into small ones without `loss` of any information in the dataset.
- Reduce the number of data, especially `numerical` data.

### Linear Discriminant Analysis `LDA`: Supervised | Categorical
- Separate `classes` or `labels`, works better with the large data set, especially `categorical` data.
 
### Auto Encoder | Unsupervised | `ANN`
- Learn and discover the `structure` of the dataset, ignoring noise in data. 

### Applications of Auto Encoders include:

1. Anomaly detection ( Unusual or unexpected behaviour )
2. Removing noise from data ( Images, audio and video )
3. Image inpainting | Conservation | Restoration ( `Reconstructing` missing part of an image )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
