<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **How to deal with outliers?**

<h3><a href="#zscore">Z Score</a> ( Extreme Value Analysis ) | <a href="#dbscan">DBSCAN</a> | <a href="#summary">5 Number Summary</a> | <a href="#algo">Algorithm</a></h3>

### **What are outliers?**
- Data points that differ significantly from other observations (data points) in the dataset are outliers.
- Outlier affects the distribution of data by introducing skewness in the data and also affects the correlation among features.
- Positive Skew / Right Skew (Mean is on the right side | Mode < Median < Mean)
- Negative Skew / Left Skew (Mean is on the left side | Mode > Median > Mean) 
- Outliers have a significant impact on the performance and lead to inaccurate predictions of new unseen data.
- **Distant metric:** Algorithms that use the **Euclidean distance metric** are more sensitive to outliers as compared to the **Manhatten distance metric**.

### **How to detect outliers?**

<h5><b>1. Visualization</b></h5>

- Visualization helps to understand the distribution of data and helps to identify outliers in data.
- Boxplot, scatter plot and histogram are better plotting to identify outliers in the dataset.

<h5 name="zscore">2. Z Score or Extreme Value Analysis</h5>

![Standard Deviation](Image/Std.png)

- How many standard deviations a data point is away from its **sample's mean**.
- **z = (x - mean(x)) / std(x) (Z score normalization)**
- Data points after 3 standard deviations (mean +- 3 * std) are considered as outliers.

**Solution:** Apply transformation of data : [Scaling](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Normalization%20vs%20Standardization.md) (Bring scales at the same level)

<h5 name="dbscan">3. DBSCAN | Density-based spatial clustering of applications with noise</h5>

- Clustering methods help us to visualize the distribution of data and outliers.
- Relationships between **features** can be represented via clustering.
- It focus on finding **neighbors** by **density**.
- Outlier lies in no cluster region, it is separate from every other data point cluster region.

<h5 name="summary">4. Five Number Summary</h5>

Divide the Data into 4 Equal Quarters **(Quartiles)** 
1. Minimum: **Lowest** data point value in a dataset.
2. 1<sup>st</sup> **Quartile** (**Q1**) | 25<sup>th</sup> **Percentile**: 25% of data values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** (**Q2**) | 50<sup>th</sup> **Percentile**: Median | 50% of data values are smaller and 50% are larger than the median.
4. 3<sup>rd</sup> **Quartile** (**Q3**) | 75<sup>th</sup> **Percentile**: 75% of data values are smaller and 25% are larger.
5. Maximum: **Highest** data point value in a dataset.

Five Number Summary can be visually represented using **boxplot**.
- Horizontal lines on both ends of boxplots are whiskers.
- Box is called **Interquartile Range** (IQR)
- IQR = Q3 - Q1
- Data value **<** Q1 - 1.5 * IQR
- Data value **>** Q3 + 1.5 * IQR
- Outlier is represented by a dot o in **boxplot**  

<h5 name="algo">5. Algorithms</h5>

<table>
  <tr>
    <th colspan="2">Machine Learning Algorithms</th>
  </tr>
  <tr>
    <th>Sensitive to Outliers (Distance-based)</th>
    <th>Not Sensitive to Outliers</th>
  </tr>
   <tr>
    <td>
      <ol type="1">
        <li>Linear Regression</li>
        <li>K Nearest Neighbours (KNN)</li>
        <li>K Means Clustering</li>
        <li>Support Vector Machine</li>
      </ol>
    </td>
    <td>
      <ol type="1">
        <li>Naive Bayes</li>
        <li>Decision Tree</li>
        <li>Random Forest</li>        
        <li>Boosting Algorithms</li>        
      </ol>
    </td>
  </tr>
</table>

### **How the models are affected by outliers?**
1. **Linear Regression:** Outliers can affect the relationship, and correlation, leading to inaccurate predictions.
2. **K Mean Clustering:** Outliers can pull the centroid towards them, leading to misclassification and distorted clusters.
3. **SVM:** Outliers can move the hyperplanes to less optimal positions, reducing classification accuracy.

### **How to handle outliers?**
1. Set up a filter and trim extremely low and high data points in the dataset.
2. Remove the outlier if it is very small, change the value of the outlier or replace it with something meaningful.
3. Inter Quartile Range (IQR) and Extreme value analysis (Z Score)
5. Rescale | Standardize | Normalize (Bring to the same scale) prevents outliers from dominating.
6. Apply [ensemble learning techniques](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md) ( `Bagging` and `Boosting` )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
