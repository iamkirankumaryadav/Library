<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# `Dimensionality Reduction`

- A technique used to simplify complex datasets by reducing the number of features (variables) while preserving much information.
- Datasets with many features (variables) can be complicated to analyze, visualize, and process. Not all features are equally important.
- Transforming the data into a lower-dimensional space while retaining as much of the original information as possible.
- Helps in improving the accuracy of models, simplifying data visualization, and making data easier to interpret.
- The number of features (variables) should be low compared to the number of observations (rows) in the dataset.
- Algorithms that consist of distance calculations: Regressions, KNN, K Mean, and SVM.  
- Dimensionality reduction helps identify and focus on the features that capture the most significant information.

### **Benefits:**
- **Simplified Analysis:** Analyzing data with fewer features is easier and faster.
- **Improved Visualization:** Lower-dimensional data can be visualized more effectively using techniques like scatter plots.
- **Enhanced Machine Learning:** Reduced dimensionality can lead to better performance in machine learning tasks.

### **Feature Selection**
- Select the most relevant features from the data for building a better model.
- Irrelevant or redundant features can confuse machine learning models, leading to poor accuracy.
- By using a smaller set of relevant features, you can train models faster and potentially reduce computational costs.
- With fewer features, it becomes easier to understand which features are most influential in the model's predictions.
- Features are selected by calculating the correlation (regression) of each feature with the target variable or information gain (classification)
- Feature Selection keeps a subset of the original features. 

### **Feature Extraction**
- Creates a new dataset with only relevant features that capture most of the information and insights.
- Feature extraction helps identify and extract the most relevant features that significantly improve the accuracy and efficiency of ML Models.
- Models with fewer features require less training data and computational resources.
- Feature extraction is a powerful tool that prepares data for machine learning by extracting the most relevant and informative features.
- It simplifies data processing, improves model performance, and helps models focus on the underlying patterns that matter most.

### **Variance Thresholds**
- Variance represents how spread out the data points are for each other in the dataset.
- Variance is dependent on scale, always normalize or standardize your features first.
- Remove features whose values don't change much from observation to observation. 
- e.g. If a health dataset contains 96% observations for 35-year-old men, then age and gender features can be eliminated.

### **Correlation Threshold**
- Remove highly correlated features (Multicollinearity), and remove redundant information.

### Dimensionality reduction advantage
- Reducing dimensions (# features), explaining variance in and minimising correlation (redundancy)

### **Principle Component Analysis (PCA): Unsupervised | Numerical**
- The goal of `PCA` is to reduce the dimensionality of the data while preserving as much of the information as possible.
- `Transforms` large data sets into small ones without `loss` of any information in the dataset.
- `PCA` creates a new set of uncorrelated variables that retain most of the information in the original data.
- Reduce the number of data, especially `numerical` data.

Advantages:
1. Data Visualization: Reduce the dimensions of data to make it easier to visualize.
2. Feature Extraction: Extract the most important features from the dataset.
3. Noise Reduction: Reduce noise in the data.
4. Data Compression: Compress data without losing much information.

### Linear Discriminant Analysis `LDA`: Supervised | Categorical
- Separate classes or labels, works better with a large data set, especially categorical data.
 
### Auto Encoder | Unsupervised | `ANN`
- Learn and discover the structure of the dataset, ignoring noise in data. 

### Applications of Auto Encoders include:

1. Anomaly detection (Unusual or unexpected behaviour)
2. Removing noise from data (Images, audio and video)
3. Image inpainting | Conservation | Restoration (Reconstructing missing part of an image)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
