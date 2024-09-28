<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to deal with outliers?

<h3><a href="#zscore">Z Score</a> (Extreme Value Analysis) | <a href="#dbscan">DBSCAN</a> | <a href="#summary">5 Number Summary</a> | <a href="#algo">Algorithm</a></h3>

### What are outliers?
- Outliers are the data points that differ significantly from other data points in the dataset.
- Outliers affect the distribution of the dataset by introducing skewness and also affect the correlation among features.
- Outliers affect the overall central tendency (mean, median, mode) and measure of dispersion/deviation (variance, std)
- **Positive Skew/Right Skew:** Mean is on the right side | Mean > Median > Mode
- **Negative Skew/Left Skew:** Mean is on the left side | Mode > Median > Mean
- Outliers create a significant impact on the performance and lead to inaccurate predictions of new unseen data.
- Algorithms that are based on distance calculations are more sensitive towards the outliers.

### How to detect outliers?

<h3><b>1. Visualization</b></h3>

- Visualization helps us to understand the distribution of data and to identify the outliers in data.
- Boxplot, scatter plot and histogram help us to identify outliers in the dataset.

<h3 name="zscore">2. Z Score or Extreme Value Analysis</h3>

![Standard Deviation](Image/Std.png)

- How many standard deviations a data point is away from its **sample's mean**.
- **z = (x - mean(x)) / std(x) (Z score normalization)**
- Data points after 3 standard deviations (mean +- 3 * std) are considered as outliers.

**Solution:** Apply transformation of data : [Scaling](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Normalization%20vs%20Standardization.md) (Bring scales at the same level)

<h3 name="dbscan">3. DBSCAN | Density-based spatial clustering of applications with noise</h3>

- Clustering methods help us to visualize the distribution of data and outliers.
- Relationships between **features** can be represented via clustering.
- It focus on finding **neighbors** by **density**.
- Outlier lies in no cluster region, it's separate from every other data point cluster region.

<h3 name="summary">4. Five Number Summary</h3>

Divide the data into 4 equal quarters **(Quartiles)** 
1. Minimum: **Lowest** data point value in a dataset.
2. 1<sup>st</sup> **Quartile** (**Q1**) | 25<sup>th</sup> **Percentile**: 25% of data values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** (**Q2**) | 50<sup>th</sup> **Percentile**: Median | 50% of data values are smaller and 50% are larger than the median.
4. 3<sup>rd</sup> **Quartile** (**Q3**) | 75<sup>th</sup> **Percentile**: 75% of data values are smaller and 25% are larger.
5. Maximum: **Highest** data point value in a dataset.

**Five Number Summary** can be visually represented using **boxplot**.
- Horizontal lines on both ends of boxplots are whiskers.
- Box is called **Interquartile Range** (IQR)
- IQR = Q3 - Q1 (Interquartile range can define thresholds for outliers based on deviation from median)
- Data value **<** Q1 - 1.5 * IQR
- Data value **>** Q3 + 1.5 * IQR
- Outlier is represented by a dot o in **boxplot**  

<h3 name="algo">5. Algorithms</h3>

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

1. Remove the outliers if they are truly errors or irrelevant to your analysis.
2. Cap outliers by setting up a filter | Trim extremely low (min) and high (max) to bound the outliers.
3. Impute/Replace the outlier value with something meaningful (mean, median, most_frequent)
4. Rescale | Standardize | Normalize (Bring to the same scale) prevents outliers from dominating.
5. Apply algorithms that work perfectly or are less sensitive towards outliers i.e. [ensemble learning techniques](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md) (Bagging and Boosting)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
