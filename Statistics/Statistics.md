<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Statistics

### Descriptive Statistics:

- A branch of `statistics` that helps us **summarize** and **describe** a set of data.
- It provides us techniques to understand the main **features** and **characteristics** of the data.
- Provides a quip overview for a data. Measures `central tendency`, `variability`, and `distribution`

<h3><a href='#center'>Measure of Center</a>&nbsp;|&nbsp;<a href='#spread'>Measure of Spread</a></h3>

When we start anything we start from beginning but with a dataset we start from `centre`

`Sample` is **representative** of `Population`

Larger Sample = Greater Accuracy = More Confidence

<h3 name='center'>Measures of Centre | Central Tendency</h3>

1. `Mean` : `Average` of data points 
2. `Median` : **Middle** data point value of an **ordered** dataset | Large data set : **Median** position : `( n + 1 ) / 2`
3. `Mode` : Most frequent | Most common | Most occuring data point value.

`Outlier` :  The data point value which are different or far away from all the other data point values.

- `Mean` calculates `average`, therefore it is affected by an `outlier`
- `Median` concentrates only on `middle` value, therefore there is a very `low` to `no` effect by an `outlier`
- `Mode` concentrates only on the `most frequent` values, there is `no` effect by an `outlier`

### `Central Limit Theorem`
- As the `sample size` increases, the `distribution` approaches towards `Normal Distribution`

<h3 name='spread'>Measures of Spread | Variability</h3>
  
- Relationship of individual data point with it's Mean 

How the `observations` are `spreadout` or `scattered` on each side of the `centre` ( Mean | Median | Mode )

### 1. `Range`

- `Range` : `Max` - `Min`, difference between the lowest and highest data point values in the data set.
- `Very high` data point value can mislead the `Range` ( e.g. {8, 11, 5, 9, 7, 6, 3616 ) `Outlier`
- Here the lowest data point value is `5` and the highest data point value is `3616`

### 2. Variance ( s <sup>2</sup> )

- Sum of square of distance from its `mean`  
- `Variability` of the data point values from its mean.

### 3. Standard Deviation ( s : Square Root of Variance )
- Distance of the **data points** from its **mean** in the **data set**.
- **Small** std means `low` **variability** | Most of the **data points** are `close` to **mean** | `Narrow` distribution
- **Large** std means `high` **variability** | Most of the **data points** are `far away` from the **mean** | `Wider` distribution
- Standard deviation calculates `mean`, so it is affected by an `outlier`

### Coefficient of variation

- Measures `standard deviation` relative to the mean.
- Used to compare the standard deviation of variables with significantly different means.

![Sample vs Population](Image/Sample.jpg)

### Z Score
- `z` = ((`x` - `mean`) / `std`)
- `x` : Data Points.

### Confidence
- While **Sampling**, different `Samples` can be **randomly** selected from the same **population**.
- Each **sample** can often produce a different **Confidence Interval**. 
- Some **Confidence Intervals** include the true **Population Parameter** ( `Centre` and `Spread` ) and others do not.

### Confidence Level
- `Percentage` of all possible samples that can be expected to be present in the true population parameter. 
- `95%` **confidence level** implies that `95%` of the confidence intervals would include the true **population parameter**.

### Confidence Intervals
- A `range` of values we are sure that our population `values` will lie within that range.
- If the `sample` doesn't fit a distribution, use the `central limit theorem` to make estimates about `population` parameters.

### The **Effect** of **Transforming** Data on **Spread** and **Centre**

- Measures of `centre` are affected by every **mathematical operations** ( `+` `-` `*` `/` )
- Measures of `spread` are affected only by **multiplication & divison** ( `*` and `/` )

<h3 name='spread'>Measures of Distribution</h3>

- Describe how the data is spread out or distributed across different values.
- `Histograms` and `Frequency distributions` are graphical representations that help us visualize the distribution of data.

### `Empirical Rule`
- `68 %` of the data points in a given **normally distributed data set** fall within `1` **standard deviations**.
- `95 %` of the data points in a given **normally distributed data set** fall within `2` **standard deviations**.
- `99.7 %` of the data points in a given **normally distributed data set** fall within `3` **standard deviations**.

### Five Number Summary

> Divide the Data into 4 Equal `Quarters`

1. `Min` : **lowest** data point value in a dataset.
2. 1<sup>st</sup> **Quartile** ( `Q1` ) | 25<sup>th</sup> **Percentile** : 25% of data point values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** ( `Q2` ) | 50<sup>th</sup> **Percentile** : **Median** | 50% of data point values are smaller and 50% are larger.
4. 3<sup>rd</sup> **Quartile** ( `Q3` ) | 75<sup>th</sup> **Percentile** : 75% of data point values are smaller and 25% are larger.
5. `Max` : **Highest** data point value in a dataset.

> **Five Number Summary** can be visually represented using **Boxplot**.
- Horizontal lines on both the ends of boxplot are **Whiskers**.
- Box is called **Interquartile Range** ( `IQR` )
- `IQR` = `Q3` - `Q1`

> Data point value is considered as **Outlier** if : 
- Data point value **<** `Q1` - `1.5` * `IQR`
- Data point value **>** `Q3` + `1.5` * `IQR`

> **Outlier** is represented by dot ( **.** ) in **Boxplot** 

### Percentile 

Describe Percentage `%` of data point value that falls `At` or `Below` another data point value. 

1. 25<sup>th</sup> **Percentile** | 1<sup>st</sup> **Quartile** 
- 25% of data point values are **as small** or smaller.
- 75% of data point values are **as large** or larger.

2. 50<sup>th</sup> **Percentile** | 2<sup>nd</sup> **Quartile** | Median
- 50% of data point values are **as small** or smaller.
- 50% of data point values are **as large** or larger.

3. 75<sup>th</sup> **Percentile** | 3<sup>rd</sup> **Quartile**
- 75% of data point values are **as small** or smaller.
- 25% of data point values are **as large** or larger.

`Percentage` and `Percentile` are **different**.

### `Correlation`

- Measures the `direction` ( Positive or Negative ) and `strength` ( `-1` to `1` ) of **relationship** between two **quantitative** variables.
- One variable can `predict` the other variable.
- Varies between `-1` ( Perfect `Negative` Correlation ) to `1` ( Perfect `Positive` Correlation )

Amount of `R` | Strength of `Correlation`
:--- | :---
0.0  | No Correlation
0.1 - 0.3 | Little Correlation
0.3 - 0.5 | Medium Correlation
0.5 - 0.7 | High Correlation
0.7 - 1.0 | Very High Correlation

![Perfect Linear Correlation](Image/Perfect.png)

![Direction of Slope](Image/Direction.png)

![Strength of Slope](Image/Strength.png)

### Test Correlation Coefficient for Significance ( T Test ) 
- **Null** Hypothesis ( `H0` ) : There is **No Linear Relationship**
- **Alternate** Hypothesis ( `H1` ) : There is a **Linear Relationship**
- P Value is Calculated ( if P Value > `0.05` : Then Accept Null Hypothesis else Reject Null Hypothesis )

### Multicollinearity
- Two or more independent features **correlate** strongly with each other.
- Regression equation becomes **unstable** and create **confusion**.
- **Remove** one feature to prevent from **multicollinearity** and make regression **stable**.

### Causality
- Relationship between the **cause** and its **effect**.
- One variable affects other variable ( Temperature affect icecream sale | Sale of icecream is more in summer )

### R Squared | R<sup>2</sup>

- How close each data point **fits** to **regression line**. 
- How well the **Regression line** predicts almost **actual value**.
- Value of R<sup>2</sup> lies between `0` and `1`.
- Closer to `1` : Better the data points fit the **Regression line**.

![R is Low](Image/R007.png)

![R is Low](Image/R090.png)

![R is Low](Image/R1.png)

Correlation `R` and Coefficient of Determination `R` <sup>2</sup> are `Different`.

![Difference](Image/RRS.png)

### Covariance  
- Measures how much two variables vary with each other.

### Sampling Fact 
- A `sample` is never a **perfect representation** of the `population`.
- `Different` **samples** of `same` **population** will give **different** `mean` ( Sampling **Error** | **Variation** due to sampling )

### Confidence Interval ( alpha )
- Express a `range` of values within which we are sure that **population parameters** lies ( `Prediction` will be true )
- Population `parameters` : `mean`, `median`, **difference** between `means`, `range`, `variance` and `standard deviation`. 
- `Mean` of population lies between this interval `range` ( **Confidence Interval** )
- `Base` **estimate** is the **sample** `mean` ( Variation and sample size affects the width of **confidence interval** )
- If **prediction** falls within the `range` of **confidence interval** then it is `true` and represents the **population**.
- `Confidence Interval`: `95%` : You are **confident** that `95` out of `100` times the estimation will falls within **confidence interval** range.
