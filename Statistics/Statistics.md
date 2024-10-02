<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Statistics: The Science of Data
The science of collecting, organizing, analyzing, interpreting, and presenting data.

### Key concepts of statistics:
1. **Data:** Information gathered from observations, research, experiments, or surveys.
2. **Population:** The entire group of individuals or objects that we're interested in studying.
3. **Sample:** A subset of the population used to represent the entire group.
4. **Descriptive statistics:** Summarizing and describing data using the measures.
5. **Inferential statistics:** Make inferences about the population based on the information from a sample.
6. **Inference:** A conclusion reached based on evidence and reasoning.

### Dataset
- A dataset is a particular instance/sample of data that is used for analysis or model building at any given time.
- A dataset can be of different data types such as numerical, categorical, text, image, voice, and video data.

### Data Wrangling
- The process of converting data from its raw form to a tidy form ready for analysis.
- An important step in data preprocessing and includes several processes:
- Data importing, cleaning, structuring, parsing, encoding, rescaling, handling dates and times, missing values, and outliers.

### Data Visualization
- One of the main tools used to analyze and study relationships between different variables.
- Descriptive Analytics: Scatter plots, line graphs, bar plots, histograms, qqplots, smooth densities, boxplots, pair plots, heat maps, etc.
- Data visualization is also used in ML for data preprocessing and analysis, feature selection, model building, testing, and evaluation.

### Data Partitioning
- In ML, the dataset is often partitioned into training and testing sets.
- The model is trained on the training dataset and then tested on the testing dataset.
- The testing dataset thus acts as the unseen dataset, which can be used to estimate generalization error.
- **Generalization Error:** The error expected when the model is applied to a real-world dataset after the model has been deployed.

**Descriptive Statistics gives you a summary of your data and Inferential Statistics provides a conclusion for your data**

### Descriptive Statistics:
- Descriptive statistics are used to **summarize/describe** a dataset using the measures (mean, median, mode, standard deviation). 
- It provides us with techniques to understand the features and characteristics of the data (Quick snapshot)
- Provides a quick overview of data, and measures central tendency, variability, and distribution of the data.

<h3><a href='#center'>Measure of Center</a>&nbsp;|&nbsp;<a href='#spread'>Measure of Spread</a>&nbsp;|&nbsp;<a href='#distribute'>Measure of Distribution</a></h3>

- Sample is a **representative** of the population
- Larger Sample = Greater Accuracy = More Confidence

<h3 name='center'>Measures of Centre | Central Tendency</h3>

1. **Mean:** Average of the data points 
2. **Median:** Middle data point value of an ordered dataset | Large data set: Median position: `( n + 1 ) / 2`
3. **Mode:** Most frequent | Most common | Most occurring data point value.

### Outlier: 
- The data point that differs or is far away from all the other data points in a sample or population.
- Mean: Calculates the average, therefore it is affected by an outlier.
- Median: Concentrates only on middle values, therefore there is a very low to no effect by an outlier.
- Mode: Concentrates only on the most frequent values, there is no effect by an outlier.

### Central Limit Theorem
- As the sample size increases, the distribution approaches towards normal distribution.
- The larger the sample size, the better the approximation to a normal distribution.
- CLT allows us to use information from samples to reference populations.

<h3 name='spread'>Measures of Spread | Variability</h3>
  
- Measures the relationship of individual data points with their mean.
- How the data points are spread or scattered on each side of the centre (Mean | Median | Mode)

### 1. Range

- **Range:** Max - Min, the difference between the highest and the lowest data point values in the dataset.
- Very high data point values can mislead the range (e.g. {8, 11, 5, 9, 7, 6, 3616) Outlier.
- Here the lowest data point value is 5 and the highest data point value is 3616.

### 2. Variance (s<sup>2</sup>)
- An average of the squared distances from the mean. Variability of the data point values from its mean.

### 3. Standard Deviation (s: Square Root of Variance)
- Distance of the **data points** from its **mean** in the **data set**. The square root of the **variance**.
- Small std means low **variability** | Most of the **data points** are close to the **mean** | Narrow distribution.
- Large std means high **variability** | Most of the **data points** are far from the **mean** | Wider distribution.
- Standard deviation calculates the mean, so it is affected by an outlier.

**Variance** | **Standard Deviation**
:--- | :---
Squared deviation from mean | Square root of variance
Squared units | Same units as the original data
More sensitive to outliers | Less sensitive to outliers

### Coefficient of variation (%)
- Measures standard deviation as a percentage of the mean.
- **Coefficient of Variation (%) = (Standard Deviation / Mean) * 100**
- Measures the dispersion of data points around the mean.
- Used to compare the standard deviation of variables with significantly different means.

![Sample vs Population](Image/Sample.jpg)

### Z Score
- z = (x - mean(x)) / std(x)
- x: Data Points.

### Inferential Statistics
- Making inferences from the samples and concluding about a population.
- Examples: Marketing campaigns, clinical drug trials, opinion polls, etc.

### Hypothesis Testing:
- This is like guessing about the population based on your sample information.
- Null Hypothesis (H₀): You assume there's no significant difference between your sample and the population.
- Alternative Hypothesis (H₁): This is the actual guess about the population. There might be a difference!

### Confidence
- While sampling, different samples can be **randomly** selected from the same **population**.
- Each sample can often produce a different confidence interval.
- Some confidence intervals may include the true population parameters.

### Confidence Level (Percentage)
- Measure the possibility that all samples will represent the true population if the same method is repeated multiple times. 
- A 95% **confidence level** implies that 95% of the time the sample will represent the true population parameters.
- Population parameters: Mean, median, mode, range, variance, and standard deviation of the actual population.

### Confidence Intervals (Range of upper bound and lower bound)
- A range of values where we believe the true population values will lie within that range.
- If **prediction** falls within the interval range then the hypothesis is true and represents the **population**.

### The **Effect** of **Transforming** Data on **Spread** and **Centre**

- Measures of centre are affected by every **mathematical operations** ('+', '-', '*', and '/')
- Measures of spread are affected only by **multiplication & divison** ('*' and '/')

<h3 name='distribute'>Measures of Distribution</h3>

- Describe how the data is spread out or distributed across different values.
- Histograms help us to visualize the frequency distribution of data.
- Scatter plots help us to visualize the distribution of data.

### Empirical Rule
- 68 % of the data points in a given **normally distributed data set** fall within 1 **standard deviations**.
- 95 % of the data points in a given **normally distributed data set** fall within 2 **standard deviations**.
- 99.7 % of the data points in a given **normally distributed data set** fall within 3 **standard deviations**.

### Five Number Summary
- Divide the dataset into 4 equal quarters.
- **Minimum:** Smallest data point value in a dataset.
- 1<sup>st</sup> **Quartile** (Q1) | 25<sup>th</sup> **Percentile**: 25% of data point values are smaller and 75% are larger.
- 2<sup>nd</sup> **Quartile** (Q2) | 50<sup>th</sup> **Percentile**: **Median** | 50% of data point values are smaller and 50% are larger.
- 3<sup>rd</sup> **Quartile** (Q3) | 75<sup>th</sup> **Percentile**: 75% of data point values are smaller and 25% are larger.
- **Maximum:** Largest data point value in a dataset.
- **Five Number Summary** can be visually represented using Boxplot.
- Horizontal lines on both the ends of boxplot are Whiskers.
- Box is called Interquartile Range (IQR)
- IQR = Q3 - Q1
- Data point value is considered as an outlier if: 
- Data point value **<** Q1 - 1.5 * IQR
- Data point value **>** Q3 + 1.5 * IQR
- Outlier is represented by a dot (.) in a Boxplot.

### Percentile 

Describe the percentage % of data point value that falls at or below another data point value. 

1. 25<sup>th</sup> **Percentile** | 1<sup>st</sup> **Quartile** 
- 25% of data point values are **as small** or smaller.
- 75% of data point values are **as large** or larger.

2. 50<sup>th</sup> **Percentile** | 2<sup>nd</sup> **Quartile** | Median
- 50% of data point values are **as small** or smaller.
- 50% of data point values are **as large** or larger.

3. 75<sup>th</sup> **Percentile** | 3<sup>rd</sup> **Quartile**
- 75% of data point values are **as small** or smaller.
- 25% of data point values are **as large** or larger.

Percentage and Percentile are **different**.

### **Correlation (Direction & Strength)**
- Shows the extent (strength) to which two variables are related to each other.
- Measures the **direction** and **strength** of relationship between the features/variable.
- **Direction:** Positive (+1) or Negative (-1)
- **Strength:** No, Little, Medium, High, Very High.
- One variable can predict the other variable.
- Correlation Coefficient: -1 (Perfect Negative Correlation)
- Correlation Coefficient: 1 (Perfect Positive Correlation)

**Correlation Coefficient** (r) | **Strength of Correlation**
:--- | :---
0.0  | No Correlation
0.1 - 0.3 | Little Correlation
0.3 - 0.5 | Medium Correlation
0.5 - 0.7 | High Correlation
0.7 - 1.0 | Very High Correlation

Correlation is not equal to causation

![Perfect Linear Correlation](Image/Perfect.png)

![Direction of Slope](Image/Direction.png)

![Strength of Slope](Image/Strength.png)

### Correlation Coefficient for Significance (T-Test) 
- **Null** Hypothesis (H0): There is **No Linear Relationship**
- **Alternate** Hypothesis (H1): There is a **Linear Relationship**
- P-Value is Calculated ( if P Value > 0.05: Then Accept Null Hypothesis else Reject Null Hypothesis )

### **Multicollinearity**
- Two or more independent features **correlate** strongly with each other.
- It create a **confusing effect**, regression equation becomes **unstable** and results **unreliable estimates**.
- Choose an independent variable (Drop one feature) or combine variables (Create a new feature)

### Causality
- Causality is all about understanding the relationship between the cause and its effect.
- One variable affects other variables (Temperature affects ice creams/cold-drink sales)
- What causes what, we can predict what can happen next and make better decisions.

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

### **Covariance (Direction)**
- Covariance is a measure of how two variables change together.
- Helps us understand the relationship between two sets of data points.
- `Positive Covariance`: Two variables tend to move in the `same` direction. 
- `Negative Covariance`: Two variables tend to move in `opposite` directions.

### Sampling Facts: 
- **A sample is never a perfect representation of the population.**
- **Different samples of the same population will give different mean.**
- Sometimes it can be due to the sampling error, we will get variations due to the error.

### **P-Value**
- Imagine you have a coin (Head/Tails)
- The normal scenario: If you flip the coin, fairly it will end up in random heads or tails, 5 Heads and 5 Tails or any combination.
- But it ends up in 10 Heads, now you suspect it might be biased towards Heads.

Here's how p-value can help you test that suspicion:
1. **Null Hypothesis (H0):** The coin is fair (One side is the head and another side is the tail)
2. **Alternate Hypothesis (Ha):** The coin is biased (It will fall on either head)
3. **Observed Data:** You flip the coin, say, 10 times. Surprisingly, you get Heads every single time!
4. **Test Statistic:** This would be the number of heads observed, which in this case is 10 out of 10 flips.
- P-value is the probability of getting a result as extreme as 10 heads in 10 flips, assuming the coin is fair (H0).
- In a fair case, it'll not be always possible to get 10 Heads every time.
- The p-value tells you how often you'd expect to see 10 heads in a row! in those hypothetical repetitions.
- We can say that there is only less than 5% or 1% chance it may happen.
- If p-value > 0.05 i.e. Here it's a normal scenario (Fair coin, NULL Hypothesis Accepted)
- If p-value < 0.05 i.e Very rare scenario of getting H only (The coin is biased)
