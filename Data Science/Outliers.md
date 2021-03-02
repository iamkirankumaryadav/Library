# How to Deal with Outliers ?

### Outliers
- **Data Point** that differs significantly from other **Observations** in the Dataset.

### Cause of Outliers
1. Human Error ( Data Entry )
2. Measurement ( Instrumental )
3. Experimental ( Data Extraction )
4. Natural Case ( Special Unique Case )

In Machine Learning and in any **Quantitative Analysis** the **Quality** of Data is as important as Quality of **Prediction** or **Classification** Model.

How many **Features** to take into account to **Detect Outliers** ?
- **Univariate** | **Multivariate**

### Methods for Outlier Detection

### 1. Z Score or Extreme Value Analysis
- How many **Standard Deviations** a **Data Point** is from the **Sample's Mean**
- **z** = ( x - **mean** ) / **standard deviation**
- Data Points after **3 Standard Deviations** ( mean +- 3 * std ) are considered as **Outliers**.

> **Solution** : Apply Transformation of Data : Scaling

### ( DBSCAN ) | Density Based Spatial Clustering of Applications with Noise
- **Clustering** methods are useful tools that helps us to **Visualize** and **Understand** Data better.
- Relationships between **Features** can be represented via **Clustering**.
- **DBSCAN** is a **Density Based Clustering Algorithm**, it is focused on finding **Neighbors** by **Density**.
- Outlier lies in No Cluster it is Seperate from every other Data point.
