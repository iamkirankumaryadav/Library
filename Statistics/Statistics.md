<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Statistics
<h3><a href='#center'>Measure of Center</a>&nbsp;|&nbsp;<a href='#spread'>Measure of Spread</a></h3>

> Describing **Distributions** using **Numbers**

<h3 name='center'>Measures of Centre | Central Tendency</h3>

1. **Mean** 
- Arithmetic average of Data Points.

2. **Median**  
- The Data Value that is in the **Middle** of an **Ordered** Dataset.
- If Dataset is very large the posistion of **Median** : `( n + 1 ) / 2`

3. **Mode** 
- Most Frequently observed or most Occuring **Data Value** | **Data Point**.

<h3 name='spread'>Measures of Spread</h3>

1. **Range**
- Max - Min

2. **Standard Deviation** (**S**)
- How close the **Data Values** in the Dataset are to the **Mean**
- **Small** Standard Deviation means low **Variability** | Most of the Data points are close to **Mean**
- **Large** Standard Deviation means high **Variability** | Most of the Data points are far away from the **Mean**

3. **Variance** (**S**<sup>2</sup>)

### The **Effect** of **Transforming** Data on **Spread** and **Centre**

- Measures of **Centre** are Affected by every **Mathematical Operations** (+ - * /)
- Measures of **Spread** are only Affected by **Multiplication & Divison** (* and /)

### The **Effect** of **Outliers** on **Spread** and **Centre**

-  A Data Value that is numerically **Distant** from a Dataset.

1. Effect on `Mean`
-  Heavily affected

2. Effect on `Median`
-  **Low** or **No** affect on the **Median**
-  Median only cares about **Centre**.

3. Effect on `Mode`
-  **No** affect on the **Mode** 
-  Mode only cares about **Most Frequent** Data Value.

4. Effect on `Range`
-  **Heavily** affects the **Range** ( Outlier can be very High ( **Max** ) or Low ( **Min** ) value )

6. Effect on `Standard Deviation`
-  **Heavily** affected because **Mean** is considered while Calculating **Standard Deviation**.

### Five Number Summary

> Divide the Data into 4 Equal Quarters

1. Minimum : **Smallest** value in a Dataset.
2. 1<sup>st</sup> **Quartile** ( `Q1` ) | 25<sup>th</sup> **Percentile** : 25% of Data Values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** ( `Q2` ) | 50<sup>th</sup> **Percentile** : **Median** | 50% of Data Values are smaller and 50% are larger the Median.
4. 3<sup>rd</sup> **Quartile** ( `Q3` ) | 75<sup>th</sup> **Percentile** : 75% of Data Values are smaller and 25% are larger.
5. Maximum : **Largest** Value in a Dataset.

> **Five Number Summary** can be visually represented using **Boxplot**.
- Horizontal Line on both ends of Boxplots are **Whiskers**.
- Box is called **Interquartile Range** ( **IQR** ).
- **IQR = Q3 - Q1** 

> Data Value is considered as **Outlier** 
- Data Value **<** Q1 - 1.5 * ( **IQR** ) 
- Data Value **>** Q3 + 1.5 * ( **IQR** ) 

> **Outlier** is represented by dot ( **.** ) in **Boxplot** 

### Percentile
- Describe Percentage ( **%** ) of Data Values that Fall **At** or **Below** another **Data Value**. 

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

- Measures the **Direction** and **Strength** of **Relationship** between two **Quantitative** Variable.
- One Variable can Predict the other Variable.
- Varies between -1 to 1

Amount of R | Strength of Correlation
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
- **Null** Hypothesis ( H0 ) : There is **No Linear Relationship**
- **Alternate** Hypothesis ( H1 ) : There is a **Linear Relationship**
- P Value is Calculated ( if P Value > 0.05 : Then Accept Null Hypothesis else Reject Null Hypothesis )

### Multicollinearity
- Two or More Independent Features **Correlate** Strongly with each other.
- Regression Equation becomes **Unstable** and Create **Confusio** 
- **Remove** One Feature to Prevent from Multicollinearity and make Regression **Stable**.

### Causality
- Relationship between **Cause** and its **Effect**
- One Variable affects other Variable ( Temperature affect Icecream Sale | Sale of Icecream is more in Summer )

### R Squared | R<sup>2</sup>

- How close each Data point **Fits** to **Regression Line**.
- How well the **Regression Line** predicts **Actual Value**.
- Value of R<sup>2</sup> lies between **0** and **1**
- Closer to 1 : Better the Data Points Fit the **Regression Line**.

![R is Low](Image/R007.png)

![R is Low](Image/R090.png)

![R is Low](Image/R1.png)

### Correlation ( R ) and ( R<sup>2</sup> ) are Different.

![Difference](Image/RRS.png)

### Covariance  
- Measures how much two variables vary with each other.

### Confidence Interval ( alpha )
- Gives a **Range** of Values which is likely to contain Population Parameter ( Prediction will be True )
- **Range** of values that you expect your **Estimate** to fall between a certain % of the Time.
- e.g Confidence Interval of 95% : You are Confident that 95 out of 100 Times the Estimation will Falls between **Confidence Interval** Range.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
