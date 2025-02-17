<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# **Dimensionality Reduction**

- A fundamental technique in the field of Data Science and ML that refers to reducing the # input variables in a dataset.
- A technique to simplify complex datasets by reducing the # features (variables) while preserving the significant information.
- Datasets with many features can be complicated to analyze, visualize, and process. Not all features are equally important.
- Irrelevant or redundant features can confuse ML models, leading to poor accuracy and undesirable errors.
- Transforming the data into a lower-dimensional space while retaining as much original information as possible.
- The number of features (variables) should be low compared to the dataset's observations (rows).
- Dimensionality reduction is more helpful for the algorithms that consist of distance calculations: Regressions, KNN, K Mean, and SVM.  
- Dimensionality reduction helps identify and focus on the features that capture the most significant information.

**When to use Dimensionality Reduction?**
- When facing high computational costs due to a large number of features.
- When a model suffers from overfitting due to many features.
- When you need to visualize high-dimensional data in 2D or 3D.

### Benefits:
- **Simplified Analysis:** Analyzing data with fewer, relevant features is easier and faster.
- **Improved Accuracy:** Simplifies the model, which improves accuracy, consistency and efficiency.
- **Faster Training:** Less data means faster computation, faster training, and faster prediction/classification.
- **Improved Visualization:** Lower-dimensional data can be visualized more effectively using charts and plots.
- **Enhanced ML:** Reduced computational cost, faster model training and better accuracy + model performance.

**Feature Selection** | **Feature Extraction**
:--- | :---
Selecting a subset of the existing features in your data | Creating entirely new features from existing ones
Keeping the original dataset, but selecting the subset of important features | Transforming the original dataset and creating something entirely new.
Selects the most relevant features that best represent the data | Transforms the raw data into a new set of features that are more suitable for ML algorithms.
Improves model performance by eliminating irrelevant or redundant features | Simplifies data processing by creating more meaningful features
Reduces training time by using a smaller set of features | Improves model performance by capturing underlying patterns

### **Feature Selection**
- Feature selection selects the most relevant features and creates a new subset of data for building a better model with better accuracy.
- Features are selected by calculating the correlation (regression) or information gain (classification)
- Wrapper methods use algorithms to search for the most predictive subset of features (Random Forest)
- Embedded methods perform feature selection as a part of the model training process.
- Regularization (LASSO and Ridge) also helps in finding the relevant features for the model training.

### **Feature Extraction**
- Feature extraction identifies the most relevant features and transforms the original dataset into a new dataset. 
- Models with only the relevant features (variables) require less training data, training time, and computational resources.
- Examples: PCA (Unsupervised Numerical), LDA (Supervised Categorical Classification), and t-SNE (Non-linear)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
