<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# `Dimensionality Reduction`

- A technique used to simplify complex datasets by reducing the number of features (variables) while preserving much information.
- Datasets with many features (variables) can be complicated to analyze, visualize, and process. Not all features are equally important.
- Irrelevant or redundant features can confuse ML models, leading to poor accuracy and undesirable errors.
- Transforming the data into a lower-dimensional space while retaining as much of the original information as possible.
- The number of features (variables) should be low compared to the number of observations (rows) in the dataset.
- Dimensionality reduction is more helpful for the algorithms that consist of distance calculations: Regressions, KNN, K Mean, and SVM.  
- Dimensionality reduction helps identify and focus on the features that capture the most significant information.

### **Benefits:**
- **Simplified Analysis:** Analyzing data with fewer features is easier and faster.
- **Improved Visualization:** Lower-dimensional data can be visualized more effectively using techniques like scatter plots.
- **Enhanced Machine Learning:** Reduced computational cost, faster model training and better accuracy + model performance.

Feature Selection | Feature Extraction
:--- | :---
Selecting a subset of the existing features in your data | Creating entirely new features from existing ones
Keeping the original dataset, but selecting the subset of important features | Transforming the original dataset and creating something entirely new.
Selects the most relevant features that best represent the data | Transforms the raw data into a new set of features that are more suitable for ML algorithms.
Improves model performance by eliminating irrelevant or redundant features | Simplifies data processing by creating more meaningful features
Reduces training time by using a smaller set of features | Improves model performance by capturing underlying patterns

### **Feature Selection**
- Feature selection selects the most relevant features and creates a new subset of data for building a better model with better accuracy.
- Features are selected by calculating the correlation (regression) of each feature with the target variable or information gain (classification)

### **Feature Extraction**
- Feature extraction identifies the most relevant features and transforms the original dataset into a new dataset. 
- Models with only the relevant features (variables) require less training data, training time, and computational resources.

### **Principle Component Analysis (PCA): Unsupervised | Numerical**
- A dataset with many dimensions (features) can be complicated for analysis and visualization. PCA reduces the complexity.
- It compresses/transforms the data into a new set of features, called Principle Components (PCs) that capture the most information from the original features.
- The goal of PCA is to reduce the dimensionality of the data while preserving as much of the information as possible.
- The first principle component (PC1) represents the greatest variance.
- The second principle component (PC2) represents the remaining significant variance perpendicular to PC1.
- Subsequent principle components (PCs) continue explaining the remaining variance (But with decreasing importance)
- By focusing on a smaller set of PCs, PCA simplifies the exploratory data analysis (EDA), data preparation and data visualization.
- Many ML algorithms struggle with high-dimensional data. PCA can reduce the dimensions and potentially improve the model performance.

Advantages:
1. Data Visualization: Reduce the dimensions of data to make it easier to visualize.
2. Feature Extraction: Extract the most important features from the dataset.
3. Data Compression: Compress data without losing much information.

### **Linear Discriminant Analysis (LDA): Supervised | Classification**
- LDA's primary objective is to identify the best way to separate the existing categories in the data.
- LDA finds the best linear separation between categories in your data.
- LDA can reduce the number of features needed for classification.
 
### Auto Encoder | Unsupervised | `ANN`
- Learn and discover the structure of the dataset, ignoring noise in data. 

### Applications of Auto Encoders include:

1. Anomaly detection (Unusual or unexpected behaviour)
2. Removing noise from data (Images, audio and video)
3. Image inpainting | Conservation | Restoration (Reconstructing missing part of an image)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
