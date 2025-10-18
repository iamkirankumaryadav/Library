<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to deal with outliers?

<h3><a href="#zscore">Z Score</a> (Extreme Value Analysis) | <a href="#dbscan">DBSCAN</a> | <a href="#summary">5 Number Summary</a> | <a href="#algo">Algorithm</a></h3>

### What are outliers?
- Outliers are data points that are far from the rest of the dataset.
- They skew distribution, affecting overall correlations and summary statistics:
- Central tendency (mean, median, and mode) and Dispersion (range, variance and standard deviation).
- They can pull the regression line and distort the correlation coefficients.
- Outliers can reduce the predictive power of ML models and lead to inaccurate predictions.
- Distance-based models (Regression, KNN, K Mean, SVM, etc.) are highly sensitive to outliers.

### Skewness and Outliers:
- **Positive/Right Skew:** Mean > Median > Mode (Mean on the right side)
- **Negative/Left Skew:** Mode > Median > Mean (Mean on the left side)

### How to detect outliers?

<h3><b>1. Data Visualization</b></h3>

- Visualization helps us understand data distribution and spot outliers.
- Boxplots, scatter plots, and histograms are useful for identifying outliers in the data.

<h3 name="zscore">2. Z Score or Extreme Value Analysis</h3>

![Standard Deviation](Image/Std.png)

- The Z-score measures how far a data point is from the mean in terms of standard deviations.
- Formula: z = (x - mean) / std (Z-score normalization).
- Data points more than 3 standard deviations away from the mean (mean ± 3 * std) are considered outliers.

**Solution:** Apply transformation of data: [Scaling](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Normalization%20vs%20Standardization.md) (Bring scales at the same level)

<h3 name="dbscan">3. DBSCAN | Density-based spatial clustering of applications with noise</h3>

- Clustering helps visualize data distribution and spot outliers.
- It shows relationships between features by grouping similar data points.
- Clustering focuses on finding neighbors based on density.
- Outliers are not part of any cluster, they lie outside the cluster of data points.

<h3 name="summary">4. Five Number Summary</h3>

Divide the data into 4 equal quarters **(Quartiles)** 
1. Minimum: The lowest value in the dataset.
2. 1<sup>st</sup> **Quartile** (**Q1**) | 25<sup>th</sup> **Percentile**: 25% of values are smaller, 75% are larger.
3. 2<sup>nd</sup> **Quartile** (**Q2**) | 50<sup>th</sup> **Percentile**: Median | 50% are smaller, 50% are larger.
4. 3<sup>rd</sup> **Quartile** (**Q3**) | 75<sup>th</sup> **Percentile**: 75% of smaller, 25% are larger.
5. Maximum: The highest value in the dataset.

**Five Number Summary** can be visually represented using **boxplot**.
- The whiskers are the horizontal lines at both ends of a boxplot.
- The box represents the Interquartile Range (IQR).
- **IQR = Q3 - Q1** (It defines a range for outliers based on how far values are from the median.)
- Data points **<** Q1 - 1.5 * IQR or **>** Q3 + 1.5 * IQR are considered outliers.
- Outliers are shown as dots (o) on the boxplot.

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
1. **Linear Regression:** Outliers can affect the relationship, and correlation, causing inaccurate predictions.
2. **K Mean Clustering:** Outliers can pull/shift the centroid, leading to misclassification and inaccurate clusters.
3. **SVM:** Outliers can move the hyperplanes to less optimal positions, reducing classification accuracy.

### **How to handle outliers?**
1. Remove outliers if they are errors, irrelevant, or affecting analysis.
2. Cap outliers by setting filters to limit extremely low (min) and high (max) values.
3. Impute/Replace outliers with meaningful values (mean, median, or most frequent).
4. Rescale/Standardize/Normalize the data to prevent outliers from dominating.
5. Apply algorithms that are less sensitive to outliers, like [ensemble learning techniques](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md) (Bagging and Boosting)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
