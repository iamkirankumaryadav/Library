<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Statistics

- Statistics is all about making sense of data.
- Statistics is the study of how to collect, organize, analyze, and interpret data/information.
- It can be used to make informed decisions about a wide range of topics.

### Some basic concepts of statistics:
1. `Population`: The entire group of people or things that you are interested in studying.
2. `Sample`: A subset of the population that you can use to conclude.
3. `Variable`: A characteristic of the population that you are interested in measuring.
4. `Data`: The information that you collect about the variables of the population.
5. `Descriptive statistics`: Summarize the data and describe the population.
6. `Inferential statistics`: Make inferences about the population from the sample.
7. `Inference`: A conclusion reached based on evidence and reasoning.

**Descriptive statistics give you a summary of your data, and Inferential statistics gives final conclusion for your data**

### Descriptive Statistics:

- Descriptive statistics are used to **summarize/describe** a dataset in a way that makes it easy to understand. 
- It provides us with techniques to understand the features and characteristics of the data (Quick snapshot)
- Provides a quick overview of data, measures `central tendency`, `variability`, and `distribution` of the data.
- You can get a quick idea of what your data is like without getting down into every single data point.

<h3><a href='#center'>Measure of Center</a>&nbsp;|&nbsp;<a href='#spread'>Measure of Spread</a>&nbsp;|&nbsp;<a href='#distribute'>Measure of Distribution</a></h3>

When we start anything we start from the beginning but with a dataset we start from the `centre`

`Sample` is **representative** of `Population`

Larger Sample = Greater Accuracy = More Confidence

<h3 name='center'>Measures of Centre | Central Tendency</h3>

1. `Mean`: `Average` of data points 
2. `Median`: `Middle` data point value of an ordered dataset | Large data set: `Median` position: `( n + 1 ) / 2`
3. `Mode`: Most frequent | Most common | Most occurring data point value.

`Outlier`:  The data point values that are different or far away from all the other data point values.

- `Mean` calculates `average`, therefore it is affected by an `outlier`
- `Median` concentrates only on `middle` value, therefore there is a very `low` to `no` effect by an `outlier`
- `Mode` concentrates only on the `most frequent` values, there is `no` effect by an `outlier`

### `Central Limit Theorem`
- As the `sample` size increases, the `distribution` approaches towards `Normal Distribution`

<h3 name='spread'>Measures of Spread | Variability</h3>
  
- Relationship of individual data points with their `mean`

How the `observations` are `spread` or `scattered` on each side of the `centre` ( Mean | Median | Mode )

### 1. `Range`

- `Range`: `Max` - `Min`, the difference between the lowest and highest data point values in the data set.
- `Very high` data point value can mislead the `Range` ( e.g. {8, 11, 5, 9, 7, 6, 3616 ) `Outlier`
- Here the lowest data point value is `5` and the highest data point value is `3616`

### 2. Variance ( s <sup>2</sup> )

- An average of the squared distances from the **mean**.
- `Variability` of the data point values from its mean.

### 3. Standard Deviation (s: Square Root of Variance)
- Distance of the **data points** from its **mean** in the **data set**. The square root of the **variance**.
- `Small` std means `low` **variability** | Most of the **data points** are `close` to **mean** | `Narrow` distribution
- `Large` std means `high` **variability** | Most of the **data points** are `far away` from the **mean** | `Wider` distribution
- Standard deviation calculates `mean`, so it is affected by an `outlier`

Variance | Standard Deviation
:--- | :---
Squared deviation from mean | Square root of variance
Squared units | Same units as the original data
More sensitive to outliers | Less sensitive to outliers

### Coefficient of variation

- Measures `standard deviation` relative to the mean.
- Used to compare the standard deviation of variables with significantly different means.

![Sample vs Population](Image/Sample.jpg)

### Z Score
- `z = ((x - mean) / std)`
- `x`: Data Points.

### Inferential Statistics

-  Allows you to conclude a larger population from a smaller sample.
-  Making Inferences from Samples:
- Imagine you want to understand if a new product will be liked by people or not.
- It's not practical to test it on every person in the world. So, you select a representative sample of people (maybe 100) and allow half to taste (50 people) while using a regular one on the other half (control group).
- By comparing the average people's increase in the usage of product to the control group, you can infer whether the product will be truly liked by the entire population.

### Hypothesis Testing:
- This is like guessing the population based on your sample.
- Null Hypothesis (H₀): You assume there's no significant difference between your sample and the population.
- Alternative Hypothesis (H₁): This is the actual guess about the population. There might be a difference!

### Confidence
- While `sampling`, different `samples` can be **randomly** selected from the same **population**.
- Each **sample** can often produce a different `Confidence Interval`
- Some `confidence intervals` include the true `population parameter**` (`Centre` and `Spread`) and others do not.

### Confidence Level (Percentage)
- `Percentage` of all possible samples that can be expected to be present in the true population parameter, it the same method is repeated multiple times. 
- `95%` **confidence level** implies that `95%` of the confidence intervals would include the true `population parameter`
- Here population parameter means the mean, median, mode, range, variance, and standard deviation of the actual population.

### Confidence Intervals
- A `range` of values we are sure that our population `values` will lie within that range.
- If the `sample` doesn't fit a distribution, use the `central limit theorem` to make estimates about `population` parameters.

### The **Effect** of **Transforming** Data on **Spread** and **Centre**

- Measures of `centre` are affected by every **mathematical operations** ( `+` `-` `*` `/` )
- Measures of `spread` are affected only by **multiplication & divison** ( `*` and `/` )

<h3 name='distribute'>Measures of Distribution</h3>

- Describe how the data is spread out or distributed across different values.
- `Histograms` and `Frequency distributions` are graphical representations that help us visualize the distribution of data.

### `Empirical Rule`
- `68 %` of the data points in a given **normally distributed data set** fall within `1` **standard deviations**.
- `95 %` of the data points in a given **normally distributed data set** fall within `2` **standard deviations**.
- `99.7 %` of the data points in a given **normally distributed data set** fall within `3` **standard deviations**.

### Five Number Summary

> Divide the Data into 4 Equal `Quarters`

1. `Minimum`: Smallest data point value in a dataset.
2. 1<sup>st</sup> **Quartile** ( `Q1` ) | 25<sup>th</sup> **Percentile**: 25% of data point values are smaller and 75% are larger.
3. 2<sup>nd</sup> **Quartile** ( `Q2` ) | 50<sup>th</sup> **Percentile**: **Median** | 50% of data point values are smaller and 50% are larger.
4. 3<sup>rd</sup> **Quartile** ( `Q3` ) | 75<sup>th</sup> **Percentile**: 75% of data point values are smaller and 25% are larger.
5. `Maximum`: Largest data point value in a dataset.

> **Five Number Summary** can be visually represented using `Boxplot`
- Horizontal lines on both the ends of boxplot are `Whiskers`
- Box is called `Interquartile Range` ( `IQR` )
- `IQR` = `Q3` - `Q1`

> Data point value is considered as `Outlier` if : 
- Data point value **<** `Q1` - `1.5` * `IQR`
- Data point value **>** `Q3` + `1.5` * `IQR`
- `Outlier` is represented by a dot ( `.` ) in `Boxplot`

### Percentile 

Describe the percentage `%` of data point value that falls `at` or `below` another data point value. 

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

- Shows the extent to which two variables are related to each other.
- Measures the `direction` ( Positive or Negative ) and `strength` ( `-1` to `1` ) of **relationship** between two **quantitative** variables.
- One variable can `predict` the other variable.
- Correlation Coefficient: `-1` ( Perfect `Negative` Correlation )
- Correlation Coefficient: `1` ( Perfect `Positive` Correlation )

Correlation Coefficient `R` | Strength of `Correlation`
:--- | :---
0.0  | No Correlation
0.1 - 0.3 | Little Correlation
0.3 - 0.5 | Medium Correlation
0.5 - 0.7 | High Correlation
0.7 - 1.0 | Very High Correlation

`Correlation` is not equal to `causation`

![Perfect Linear Correlation](Image/Perfect.png)

![Direction of Slope](Image/Direction.png)

![Strength of Slope](Image/Strength.png)

### Test Correlation Coefficient for Significance ( T-Test ) 
- **Null** Hypothesis ( `H0` ) : There is **No Linear Relationship**
- **Alternate** Hypothesis ( `H1` ) : There is a **Linear Relationship**
- P-Value is Calculated ( if P Value > `0.05`: Then Accept Null Hypothesis else Reject Null Hypothesis )

### Multicollinearity
- Two or more independent features **correlate** strongly with each other.
- Regression equation becomes **unstable** and create **confusion**.
- **Remove** one feature to prevent from **multicollinearity** and make regression **stable**.

### Causality
- Relationship between the **cause** and its **effect**.
- One variable affects other variables ( Temperature affects ice cream sale | Sale of ice cream is more in summer )

### R Squared | R<sup>2</sup>

- How close each data point **fits** to **regression line**. 
- How well the **Regression line** predicts almost **actual value**.
- Value of R<sup>2</sup> lies between `0` and `1`.
- Closer to `1`: Better the data points fit the **Regression line**.

![R is Low](Image/R007.png)

![R is Low](Image/R090.png)

![R is Low](Image/R1.png)

Correlation `R` and Coefficient of Determination `R` <sup>2</sup> are `Different`.

![Difference](Image/RRS.png)

### `Covariance`  

- Covariance is a measure of how two variables change together.
- Helps us understand the relationship between two sets of data points.
- `Positive Covariance`: Two variables tend to move in the `same` direction. 
- `Negative Covariance`: Two variables tend to move in `opposite` directions.

### Sampling Fact 
- A `sample` is never a **perfect representation** of the `population`.
- `Different` **samples** of `same` **population** will give **different** `mean` ( Sampling **Error** | **Variation** due to sampling )

### Confidence Interval (alpha: upper bound and lower bound)
- Express a `range` of values within which we are sure that **population parameters** lie ( `Prediction` will be true )
- Population `parameters`: `mean`, `median`, **difference** between `means`, `range`, `variance` and `standard deviation`. 
- `Mean` of population lies between this interval `range` ( **Confidence Interval** )
- `Base` **estimate** is the **sample** `mean` ( Variation and sample size affects the width of **confidence interval** )
- If **prediction** falls within the `range` of **confidence interval** then it is `true` and represents the **population**.
- The confidence interval is expressed as two numbers, an upper and a lower bound.
- `Confidence Interval`: `95%`: You are **confident** that, if you repeated this sampling process many times, `95` out of `100` times the estimation will fall within the **confidence interval** range.

### **P-Value**

- Imagine you have a coin,
- The normal scenario: If you flip the coin, fairly it will end up in random heads or tails, 5 Heads and 5 Tails or any combination.
- But it ends up in 10 Heads, now you suspect it might be biased towards Heads. Here's how `p-value` can help you test that suspicion:

1. **Null Hypothesis (H0):** The coin is fair (heads and tails are equally likely).

2. **Observed Data:** You flip the coin, say, 10 times. Surprisingly, you get Heads every single time!

3. **Test Statistic:** This would be the number of heads observed, which in this case is 10 out of 10 flips.

4. **P-value:**
- This is the probability of getting a result as extreme as 10 heads in 10 flips, assuming the coin is fair (H0).
- In a fair case, it'll not be always possible to get 10 Heads every time.
- The p-value tells you how often you'd expect to see 10 heads in a row! in those hypothetical repetitions.
- We can say that there is only a 5% chance it may happen.
- If p-value > 0.05 i.e. Here it's a normal scenario (Fair coin, NULL Hypothesis Accepted)
- If p-value < 0.05 i.e Very rare scenario of getting H only (The coin is biased)
