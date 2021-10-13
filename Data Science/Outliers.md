<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to Deal with Outliers ?

<h3><a href="#zscore">Z Score</a> ( Extreme Value Analysis ) | <a href="#dbscan">DBSCAN</a> | <a href="#summary">5 Number Summary</a> | <a href="#algo">Algorithm</a></h3>

### Outliers
- **Data point** that differs significantly from other **observations** in the dataset.
- `Outlier` affects the distribution of data. 
- `Outliers` brings `skewness` in the data and lead to false decision making.

### Cause of Outliers 

- Human Error ( Data Entry ) 
- Measurement ( Instrumental ) 
- Experimental ( Data Extraction ) 
- Natural ( Special unique case )

How many **features** to take into account to **Detect Outliers** ?

- **Univariate** ( Only one feature ) | **Multivariate** ( More than one feature )
- **Data visualization** helps to visualize the distribution of data and also the presence of `outlier` in data.
- **Boxplot**, **scatter plot** and **histograms** are better plots to find **outliers** in the data set.

### Methods for Outlier Detection

<h3 name="zscore"> Z Score or Extreme Value Analysis</h3>

![Standard Deviation](Image/Std.png)

- How many `standard deviations` a data point is away from it's **sample's mean**.
- **z** = ( x - **mean** ) / **standard deviation** ( Z score normalization )
- Data points after **3 standard deviations** ( `mean` +- `3` * `std` ) are considered as `outliers`

`Solution` : Apply transformation of data : Scaling ( Bring scales at same level )

<h3 name="dbscan"> ( DBSCAN ) | Density based spatial clustering of applications with noise</h3>

- `Clustering` methods are useful tools that helps us to `visualize` distribution of data and `outliers`
- Relationships between **features** can be represented via `clustering`
- It focus on finding **neighbors** by **density**.
- `Outlier` lies in no cluster region, it is seperate from every other data point cluster regions.

### How to deal with outliers ?

1. Setup a `filter` and `trim` extreme low or extreme high data data points in the dataset.
2. Remove the `outlier` if it is very small, change the value of `outlier` or replace it with something meaningful.
3. **Inter Quartile** Range ( `IQR` ) and Extreme value analysis ( `Z Score` )
5. `Rescale` | `Standardize` | `Normalize` ( Bring to same scale )
6. Apply `ensemble` learning techniques ( `Bagging` and `Boosting` )

<h3 name="summary"> Five Number Summary</h3>

Divide the Data into `4` Equal Quarters ( `Quartiles` ) 

1. Minimum : **Lowest** daat point value in a dataset.
2. 1<sup>st</sup> **Quartile** ( **Q1** ) | 25<sup>th</sup> **Percentile** : `25%` of data values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** ( **Q2** ) | 50<sup>th</sup> **Percentile** : **Median** | `50%` of data values are smaller and 50% are larger the median.
4. 3<sup>rd</sup> **Quartile** ( **Q3** ) | 75<sup>th</sup> **Percentile** : `75%` of data values are smaller and 25% are larger.
5. Maximum : **Highest** data point value in a dataset.

`Five Number Summary` can be visually represented using **boxplot**.
- Horizontal lines on both ends of boxplots are `whiskers`.
- `Box` is called **Interquartile Range** ( `IQR` )
- `IQR` = `Q3` - `Q1`
- Data value **<** `Q1` - `1.5` * `IQR`
- Data value **>** `Q3` + `1.5` * `IQR`
- `Outlier` is represented by dot `o` in **boxplot**  

<table>
  <tr>
    <th colspan="2">Machine Learning Algorithms</th>
  </tr>
  <tr>
    <th>Sensitive to Outliers</th>
    <th>Not Sensitive to Outliers</th>
  </tr>
   <tr>
    <td>
      <ol type="1">
        <li>Linear Regression</li>
        <li>Logistic Regression</li>
        <li>K Nearest Neighbours ( KNN )</li>
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

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
