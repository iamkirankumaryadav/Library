# Principle Component Analysis | PCA

- **Unsupervised** Machine Learning Algorithm.

- It is **not** any Machine Learning Technique, it just reduces **Dimensions** | **Features** of the Dataset.

- **Dimensionally** Reduction Algorithm.

- Identify **Correlations** and **Patterns** in a **Data Set** so that it can be **Transformed** into a **Low Dimension Data Set**. 

- Dimensions are reduced without any Loss of **Important Information**.

- Remove **Inconsistencies**, **Redundant** and **Highly Correlated** Data.

- **Highly Correlated Features** provides a very **Biased** output. 

- One of the easiest and most intuitive ways to reduce the number of **Dimensions** | **Attributes** | **Features** of a Dataset.

- Reducing Dimension is a part of **Data Preprocessing**.

- Identifying the **Hyperplane** closest to the Dataset

- Main Aim is to reduce **Overfitting**, try to reduce the **Complexity** of the Model.

- The Model gets confused if very large number of **Features** are passed at the Time of **Training**.

- PCA Converts the **Highly Correlated Data** into **Clusters**.

- The Increasing Number of Dimenisons is a **Curse**, it decreases the **Accuracy** of Model.

- Never Select Feature which Creates lot of **Variance**.

- The **Curse of Dimensionality** increases with the Increase in the number of **Dimensions**.

-  It is said that Model is trained well with large the amount of data, but records (Rows) should be more not features.

### Steps of PCA

1. Standardization of the Data (Scaling of data such that all variables and their values lie within similar range)
2. Compute Principal Components (on Scaled Data)
3. Reduce Dimensions 
4. Apply Machine Learning Technique 

### Covariance
- Covariance expresses the **Correlation** between different variables in the Dataset.
- It is essential to identify **Heavily Dependent Variables** because they contain **Biased** and **Redundant** information.
- It reduces the overall **Performance** of the model.
