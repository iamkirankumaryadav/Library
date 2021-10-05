<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Statistics
<h3><a href='#center'>Measure of Center</a>&nbsp;|&nbsp;<a href='#spread'>Measure of Spread</a></h3>

When we Start anything we Start from Beginning but with a Data Set we Start from `Centre`.

`Sample` is **Representative** of `Population`.

Larger Sample = Greater Accuracy = More Confidence

> Describing **Distributions** using **Numbers**

<h3 name='center'>Measures of Centre | Central Tendency</h3>

1. `Mean` : `Average` of data points.
2. `Median` : **Middle** data value of an **Ordered** dataset | Large data set : **Median** Position : `( n + 1 ) / 2`
3. `Mode` : Most frequent | Most Common | Most occuring data value | data point.

<h3 name='spread'>Measures of Spread ( Relationship of individual data point with it's Mean )</h3> 

How the **observations** are `spread` out or scattered on each side of the `center` ( Mean | Median | Mode )

### 1. Range 

- `Range` : `Max` - `Min`  
- The difference between the lowest data point value and highest data point value in the data set.
- Very high data point value can mislead the `Range` ( e.g. {8, 11, 5, 9, 7, 6, 3616 )
- Here the lowest data point value is `5` and the highest data point value is `3616`
- Range is affected by the `Outlier`

### 2. Variance ( s <sup>2</sup> )
- `s` <sup>2</sup> : Sum ( x - mean ) <sup>2</sup> / n ( `Population` ) 
- `s` <sup>2</sup> : Sum ( x - mean ) <sup>2</sup> / n - 1 ( `Sample` ) 
- Sum of square of distance from its mean | `Variability` from its mean.

### 3. Standard Deviation ( s : Square Root of Variance )
- `s` : Distance of the **data points** from its `Mean` in the **data set** ( `Sample` )
- `Sigma` is used to denote Standard Deviation ( `Population` )
- **Small** standard deviation means low **Variability** | Most of the **data points** are `close` to **Mean**.
- **Large** standard deviation means high **Variability** | Most of the **data points** are `far` from the **Mean**.

![Sample vs Population](Image/Sample.jpg)

### 4. Z Score
- `z` = ( `x` - `Mean` ) / `Std` )
- `x` : Data Points
- `Std` : Standard Deviation

### Central Limit Theorem
- As the **sample size** increases, the `Distribution` of **sample mean** approaches towards **Normal Distribution**.

### Confidence
- While **Sampling**, different `Samples` can be **randomly** selected from the same **population**.
- Each **sample** can often produce a different **Confidence Interval**. 
- Some **Confidence Intervals** include the true **Population Parameter** ( `Centre` and `Spread` ) and others do not.

### Confidence Level
- The `Percentage` of all Possible Samples that can be Expected to Include the True Population Parameter. 
- `95%` **Confidence Level** implies that `95%` of the Confidence Intervals would Include the True **Population Parameter**.

### Confidence Interval
- A `Range` of Value we are sure that our Population `Value` will lies there.

### The **Effect** of **Transforming** Data on **Spread** and **Centre**

- Measures of **Centre** are Affected by every **Mathematical Operations** (+ - * /)
- Measures of **Spread** are only Affected by **Multiplication & Divison** (* and /)

### The **Effect** of **Outliers** on **Spread** and **Centre**

-  A Data Value that is numerically **Distant** from a Dataset.

1. `Mean` : Heavily affected
2. `Median` : **Low** or **No** affect on the `Median`, Median only cares about **Centre**.
3. `Mode` : **No** affect on the **Mode**, Mode only cares about **Most Frequent** Data Value.
4. `Range` : **Heavily** affects the **Range** ( Outlier can be very High ( **Max** ) or Low ( **Min** ) value )
6. `Standard Deviation` : **Heavily** affected because **Mean** is considered while Calculating **Standard Deviation**.

### Empirical Rule 
- Most of the Data Points in a given **Normally Distributed Data Set** fall within `3` **Standard Deviations** of the `Mean`.

### Outlier 
- A **Data Point** that is an `Abnormal` Distance from the other Values in the Data Set.

### Five Number Summary

> Divide the Data into 4 Equal `Quarters`

1. Minimum : **Smallest** value in a Dataset.
2. 1<sup>st</sup> **Quartile** ( `Q1` ) | 25<sup>th</sup> **Percentile** : 25% of Data Values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** ( `Q2` ) | 50<sup>th</sup> **Percentile** : **Median** | 50% of Data Values are smaller and 50% are larger the Median.
4. 3<sup>rd</sup> **Quartile** ( `Q3` ) | 75<sup>th</sup> **Percentile** : 75% of Data Values are smaller and 25% are larger.
5. Maximum : **Largest** Value in a Dataset.

> **Five Number Summary** can be visually represented using **Boxplot**.
- Horizontal Line on both ends of Boxplots are **Whiskers**.
- Box is called **Interquartile Range** ( `IQR` )
- `IQR` = Q3 - Q1

> Data Value is considered as **Outlier** 
- Data Value **<** Q1 - 1.5 * ( **IQR** ) 
- Data Value **>** Q3 + 1.5 * ( **IQR** ) 

> **Outlier** is represented by dot ( **.** ) in **Boxplot** 

### Percentile : Describe Percentage ( **%** ) of Data Values that Fall **At** or **Below** another **Data Value**. 

1. 25<sup>th</sup> **Percentile** | 1<sup>st</sup> **Quartile** 
- 25% of Data Points are **as small** or smaller.
- 75% of Data Points are **as large** or larger.

2. 50<sup>th</sup> **Percentile** | 2<sup>nd</sup> **Quartile** | Median
- 50% of Data Points are **as small** or smaller.
- 50% of Data Points are **as large** or larger.

3. 75<sup>th</sup> **Percentile** | 3<sup>rd</sup> **Quartile**
- 75% of Data Points are **as small** or smaller.
- 25% of Data Points are **as large** or larger.

> Percentage and Percentile is **Different**

### Correlation

- Measures the `Direction` ( Positive or Negative ) and `Strength` ( `-1` to `1` ) of **Relationship** between two **Quantitative** Variable.
- One Variable can Predict the other Variable.
- Varies between `-1` ( Perfect `Negative` Correlation ) to `1` ( Perfect `Positive` Correlation )

Amount of `R` | Strength of Correlation
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
- Two or More Independent Features **Correlate** Strongly with each other.
- Regression Equation becomes **Unstable** and Create **Confusio** 
- **Remove** One Feature to Prevent from Multicollinearity and make Regression **Stable**.

### Causality
- Relationship between **Cause** and its **Effect**
- One Variable affects other Variable ( Temperature affect Icecream Sale | Sale of Icecream is more in Summer )

### R Squared | R<sup>2</sup>

- How close each Data point **Fits** to **Regression Line** | **Regression Line** Predicts **Actual Value**.
- Value of R<sup>2</sup> lies between `0` and `1`.
- Closer to 1 : Better the Data Points Fit the **Regression Line**.

![R is Low](Image/R007.png)

![R is Low](Image/R090.png)

![R is Low](Image/R1.png)

> Correlation ( `R` ) and ( R<sup>2</sup> ) are `Different`.

![Difference](Image/RRS.png)

### Covariance  
- Measures how much two variables vary with each other.

### Sampling Fact 
- A `Sample` is never a **Perfect Representation** of the `Population`.
- `Different` **Samples** of `Same` **Population** will give **Different** `Mean` ( Sampling **Error** | **Variation** due to Sampling )

### Confidence Interval ( alpha )
- Express a `Range` of Values within which we are Sure that **Population Parameters** lies ( `Prediction` will be True )
- Population `Parameters` : `Mean`, `Median`, **Difference** between `Means`, `Range`, `Variance` and `Standard Deviation`. 
- `Mean` of Population lies between this Interval `Range` ( **Confidence Interval** )
- `Base` **Estimate** is the **Sample** `Mean` ( Variation and Sample Size affects the Width of **Confidence Interval** )
- If **Prediction** Falls within the `Range` of **Confidence Interval** then it is `True` and Represents the **Population**.
- `Confidence Interval` : `95%` : You are **Confident** that `95` out of `100` Times the Estimation will Falls within **Confidence Interval** Range.

### How Variance Affect Confidence Interval ?
- IF `Population` contains `Similar` **Data Points** : **Variation** among **Data Points** will be `Low` | `Narrow` **Confidence Interval**.
- Any `Sample` we consider from `Population` will be Similar to other `Sample`and **Estimation** will be very `Close` to **Population Parameters**. 
- IF `Population` contains `Varied` **Data Points** : **Variation** among **Data Points** will be `High` | `Wide` **Confidence Interval**.
- **Different** `Sample` from `Same` **Population** will Differ more and **Estimation** will not be `Close` to **Population Parameters**. 

### How Sample Size Affect Confidence Interval ?
- `Small` **Sample Size** Varies more from each other : `Wider` **Confidence Interval**.
- `More` **Variation** due to **Sampling** or **Sampling Error** with `Small` **Sample Size**.
- `Large` **Sample** Reduce **Variation** : `Narrow` **Confidence Interval**.
- `Large` **Sample** Balance the Unusual Data Points, Similar to each other and **Effect** of Sampling Error is Reduced.

### Confidence Level ( How much Percent Sure you can be ? )
- Express a `Percentage` which we are Sure that **Population Parameters** lies ( `Prediction` will be True )
- `Percentage` of Possibility that the Sample Mean will Represent the True Population.
- Normally `95%` of **Confidence Level** is Considered. 
- `More` Confidence Level : `Wider` Confidence Interval.
- `Low` Confidence Level : `Narrow` Confidence Interval.

### Probability
- `Ratio` of a **Desired Event** to all **Possible Outcomes**.
- e.g. Flip a Coin : P(H) : 1 / 2 ( Desired Event ( H ) : Head and All Possible Outcomes : ( H and T ) : Head and Tail )

### Sample Space
- Sum of all **Probabilities** will equal `100%`

### Every Possible Outcomes

1. Permutation : Interested in `Order` 
- `n!` : n **Factorial** ( 5! : 5 x 4 x 3 x 2 x 1 = 120 )
-  <sub>n</sub>P<sub>r</sub> = `n!` / `(n - r)!` ( `n` : **Total** Number of Objects | `r` : Number of Objects to be **Selected** )
-  e.g. 8 Runners and Select Top 3 : <sub>8</sub>P<sub>3</sub> = `8!` / `(8-3)!`
-  Applications : **Ranking**, **Seating Arrangements** or **Scheduling** ( How many Possible `Outcomes` )

2. Combinations : Not Interested in `Order` | Random Combinations
- -  <sub>n</sub>C<sub>r</sub> = `n!` / \[`r!` * `(n - r)!`\] 
- `n` : **Total** Number of Objects  
- `r` : Number of Objects to be **Selected** One Time )

![Cards](Image/Cards.jpg)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
