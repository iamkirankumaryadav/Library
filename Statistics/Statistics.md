<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Statistics: The Science of Data
- **Definition:** Statistics is the science of collecting, organizing, analyzing, explaining, and presenting data.
- **Purpose:** Helps understand, describe, and draw meaningful insights from data.

## Fundamentals of Statistics:
1. **Data:** Information collected from observations, research, experiments, or surveys.
2. **Population:** The entire group of individuals or objects that we're interested in studying.
3. **Sample:** A subset of the population used to represent the whole group.
4. **Descriptive Statistics:** Summarizing and describing data using the measures.
5. **Measures of Central Tendency:** Mean, Median, and Mode.
6. **Measures of Dispersion:** Range, Variance, and Standard Deviation.
7. **Inferential Statistics:** Drawing conclusions about the population based on the information from samples.
8. **Inference:** A conclusion based on evidence and reasoning.
9. **Descriptive Statistics** gives you a summary of your data.
10. **Inferential Statistics** provides a conclusion for your data**

## Dataset:
- A dataset is a particular sample used for analysis or model building at any given time.
- A dataset can be of different data types such as numerical, categorical, text, image, voice, and video data.

## Data Wrangling / Preprocessing:
- **Definition:** Converting raw data into a clean, structured format ready for analysis.

### Data Wrangling Processes:
- **Data Importing:** Bringing data from external sources into your working environment.
- **Data Cleaning:** Removing errors, duplicates, and inconsistencies from data.
- **Data Structuring:** Organizing data into a standardized, usable format.
- **Data Parsing:** Breaking down complex data into simpler, explainable components.
- **Data Encoding:** Converting categorical or text data into numeric form for analysis.
- **Data Rescaling:** Adjusting data values range to a common scale (e.g., normalization).
- **Handling Dates and Times:** Formatting and standardizing date/time fields for consistency.
- **Managing Missing Values:** Filling, removing, or imputing missing data points.
- **Handling Outliers:** Detecting and treating extreme values that can skew analysis.

## Data Visualization
- **Definition:** The process of visually representing data to analyze relationships, distributions, and detect outliers.

### Purpose:
- Understand patterns and trends
- Identify correlations and anomalies
- Aid in decision-making and storytelling
- **Role in ML:** Used for preprocessing, feature selection, model building, testing, and evaluation.

### Common Techniques (Descriptive Analytics):
- **Scatter Plot:** Shows relationships between two variables
- **Line Graph:** Displays trends over time
- **Bar Plot:** Compares categorical data
- **Histogram:** Shows data distribution
- **Density Plot:** Smooth representation of data distribution
- **Box Plot:** Highlights spread and outliers
- **Pair Plot:** Visualizes relationships among multiple variables
- **Heat Map:** Represents data intensity using color  

## Data Partitioning
- **Definition:** Splitting a dataset into subsets for training, validation, and testing in ML.

### Purpose:
- **Training Set:** Used to train the model.
- **Validation Set:** Used to tune hyperparameters and improve accuracy.
- **Testing Set:** Acts as unseen data to estimate generalization error.
- **Generalization Error:** The expected error when the model is applied to real-world data after deployment.

## Descriptive Statistics
- **Definition:** Techniques to summarize and describe a dataset using measures and aggregations.
- Purpose: Provides a quick snapshot of data characteristics like central tendency, variability, and distribution.

### Central Tendency: 
- **Definition:** A measure that identifies the center or typical value of a dataset (Mean, Median, and Mode).

### Variability or Dispersion: 
- **Definition:** Indicates how spread out or dispersed the data values are around the central point (Range, Variance, and Standard Deviation).

### Distribution:
- **Definition:** Describes how data values are arranged or spread across possible values (Normal distribution, and Skewed distribution).

<h3><a href='#center'>Measure of Center</a>&nbsp;|&nbsp;<a href='#spread'>Measure of Spread</a>&nbsp;|&nbsp;<a href='#distribute'>Measure of Distribution</a></h3>

- Sample is a **representative** of the population
- Larger Sample = Greater Accuracy = More Confidence

<h2 name='center'>Measures of Centre | Central Tendency</h2>

1. **Mean:** Average of the data points 
2. **Median:** Middle data point value of an ordered dataset | Large data set: Median position: `(n + 1) / 2`
3. **Mode:** Most frequent | Most common | Most occurring data point value.

## Outlier and Its Effect
- **Outlier:** A data point that significantly differs from other observations in a dataset.

### Impact on Measures:
- **Mean:** Highly affected because it considers all the values in the calculation of average.
- **Median:** Minimal effect since it focuses only on the middle value.
- **Mode:** No effect as it depends on the most frequent value.

## Central Limit Theorem (CLT)
- **Definition:** As sample size **n** increases, the distribution of the sample mean approaches a **normal distribution**, regardless of the population distribution.
- **Condition:** Typically holds when **n > 30**.
- **Importance:** Enables using sample statistics to make inferences about population parameters.

## Population Parameter vs Sample Statistic

### Population Parameter:
- A numerical value that describes a characteristic of the entire population.
- Example: Population mean (μ), population variance (σ²).

### Sample Statistic:
- A numerical value that describes a characteristic of a sample drawn from the population.
- Example: Sample mean ($\bar{x}$), sample variance (s²).

## Z-Test
- **Definition:** A statistical test used to determine if the mean of a sample is significantly different from a known population mean.

### Assumptions:
- Data is normally distributed
- Sample size n > 30
- Population variance is known

### Types:
- **One-Sample Z-Test:** Compares a sample mean to a known population mean.
- **Two-Sample Z-Test:** Compares means of two independent samples.

## T-Test
- **Definition:** A statistical test used to determine whether the means of two groups are significantly different from each other.

### Assumptions:
- Sample size is small (n < 30)
- Population variance is unknown

### Types:
- **One-Sample T-Test:** Compares a sample mean to a known population mean.
- **Two-Sample T-Test:** Compares means of two independent samples.
- **Paired T-Test:** Compares means from the same group at different times (before/after).

Aspect | Z-Test | T-Test
:--- | :--- | :---
Purpose | Tests if sample mean differs from population mean | Tests if means differ (sample vs population or between samples)
Sample Size | Large (n > 30) | Small (n < 30)
Population Variance | Known | Unknown
Distribution | Assumes normal distribution | Approximates normal distribution (via t-distribution)
Types | One-sample, Two-sample | One-sample, Two-sample, Paired

<h2 name='spread'>Measures of Spread | Variability</h2>
  
- Measures the relationship of individual data points with their mean: Indicates how far each value deviates from the average.
- Spread of data around the center (Mean | Median | Mode): Shows how data points are distributed on both sides of the central tendency.

## Range
- **Definition:** The difference between the maximum and minimum values in a dataset.
- Range = Max − Min
- **Limitation:** Highly sensitive to outliers.
- **Example:** For {8, 11, 5, 9, 7, 6, 3616}, here Min = 5 and Max = 3616
- Range = 3616 − 5 = 3611 (Misleading due to outlier)

## Variance (s²)
- **Definition:** Measures how far data points deviate from the mean by calculating the average of squared differences.
- **Purpose:** Indicates the degree of spread in the dataset. Note: Squaring emphasizes larger deviations.

## Standard Deviation (s)
- **Definition:** The square root of variance, measures how far data points are from the mean.

### Interpretation:
- **Small SD:** Low variability | Data points close to mean | Narrow distribution.
- **Large SD:** High variability | Data points far from mean | Wide distribution.
- **Sensitivity:** Affected by outliers because it uses the mean in its calculation.

**Variance** | **Standard Deviation**
:--- | :---
Squared deviation from mean | Square root of variance
Squared units | Same units as the original data
More sensitive to outliers | Less sensitive to outliers

## Coefficient of Variation (%)
- **Definition:** Expresses standard deviation as a percentage of the mean.
- **Coefficient of Variation (%) = (Standard Deviation / Mean) * 100**
- **Propose:** Measures relative dispersion of data points around the mean.
- **Use Case:** Useful for comparing variability across datasets or variables with different scales or means.

![Sample vs Population](Image/Sample.jpg)

## Z Score
- z = (x - mean(x)) / std(x)
- x: Data Points.

## Inferential Statistics
- **Definition:** Drawing conclusions about a population based on data from a sample.
- **Purpose:** Helps make predictions, test hypotheses, and generalize findings.
- **Examples:** Marketing campaigns, clinical drug trials, opinion polls.

## Hypothesis Testing
- **Definition:** A statistical method to make inferences about a population based on sample data.

### Key Components:
- **Null Hypothesis (H₀):** Assumes no significant difference or effect exists.
- **Alternative Hypothesis (H₁):** Suggests a significant difference or effect exists.
- **Z-Score:** Indicates how many standard deviations the sample mean is from the population mean.

## Confidence
- **Definition:** Represents the degree of certainty in an estimate derived from sample data.

### Confidence Interval: 
- A range of values, calculated from sample data, that is likely to contain the population parameter with a specified probability (e.g., 95%).
- Different random samples from the same population produce different confidence intervals.
- Some intervals will include the true population parameter, others may not.

### Confidence Level (%):
- Indicates the probability that repeated sampling using the same method will produce intervals containing the true population parameter.
- **Example:** A 95% confidence level means that if we take many samples and compute confidence intervals, about 95% of those intervals will include the true population parameter.
- **Population Parameters:** Metrics like mean, median, mode, range, variance, and standard deviation for the entire population.

### The **Effect** of **Transforming** Data on **Spread** and **Centre**

- Measures of centre are affected by every **mathematical operations** ('+', '-', '*', and '/')
- Measures of spread are affected only by **multiplication & divison** ('*' and '/')

<h2 name='distribute'>Measures of Distribution</h2>

- **Data Distribution:** Describe how data values are spread across the range of possible values.
- **Histograms:** Visualize the frequency distribution of data.
- **Scatter Plot:** Displays how data points are distributed and reveals relationships between variables.

## Empirical Rule (68 - 95 - 99.7 Rule)
- Applies to normally distributed data.
- **68%** of data falls within ±1 standard deviation of the mean.
- **95%** of data falls within ±2 standard deviations of the mean.
- **99.7%** of data falls within ±3 standard deviations of the mean.

## Five Number Summary
- **Definition:** A descriptive statistic that divides a dataset into four equal parts using five key values.

### Components:
- **Minimum:** Smallest data point value in a dataset.
- **Q1 (1st Quartile | 25th Percentile):** 25% of values are smaller, 75% are larger.
- **Q2 (2nd Quartile | 50th Percentile):** Median, splits data into two equal halves.
- **Q3 (3rd Quartile | 75th Percentile):** 75% of values are smaller, 25% are larger.
- **Maximum:** Largest data point value in a dataset.

### Visual Representation:
- **Five Number Summary** can be visually represented using Boxplot.
- **Box:** Interquartile Range (IQR) = Q3 − Q1
- **Whiskers:** Horizontal lines extended on both the ends of box which presents maximum and minimum values are Whiskers.

### Outliers:
- Data point value is considered as an outlier if: 
- Value **<** Q1 - 1.5 * IQR or Value **>** Q3 + 1.5 * IQR
- Outlier is represented as a dot (.) in a Boxplot.

## Correlation (Direction & Strength)
- **Definition:** Measures the relationship between two variables in terms of direction and strength.

### Direction:
- **Positive (+1):** Both variables increase together.
- **Negative (-1):** One variable increases while the other decreases.

### Strength:
- No, Weak, Moderate, Strong, Very Strong (based on correlation coefficient magnitude).

### Correlation Coefficient (r):
- **r = +1:** Perfect positive correlation.
- **r = -1:** Perfect negative correlation.
- **r ≈ 0:** No correlation.

### Interpretation: 
- Higher absolute value of r indicates stronger relationship, correlation does not imply causation.

**Correlation Coefficient** (r) | **Strength of Correlation**
:--- | :---
0.0  | No Correlation
0.1 - 0.3 | Little Correlation
0.3 - 0.5 | Medium Correlation
0.5 - 0.7 | High Correlation
0.7 - 1.0 | Very High Correlation

![Perfect Linear Correlation](Image/Perfect.png)

![Direction of Slope](Image/Direction.png)

![Strength of Slope](Image/Strength.png)

## Correlation Coefficient Significance (T-Test)
- **Purpose:** Tests whether the observed correlation between two variables is statistically significant.

### Hypotheses:
- **Null Hypothesis (H₀):** No linear relationship exists (correlation = 0).
- **Alternative Hypothesis (H₁):** A linear relationship exists (correlation ≠ 0).

### Test Statistic:
- Uses a t-test based on the correlation coefficient and sample size.

### Decision Rule:
- Calculate p-value.
- If p-value > 0.05, accept H₀ (no significant correlation).
- If p-value ≤ 0.05, reject H₀ (significant correlation).

## Multicollinearity
- Occurs when two or more independent variables are highly correlated.
- Causes unstable regression coefficients and unreliable estimates.

### Detection Methods:
- **Correlation Matrix:** Check pairwise correlations between features.
- **Variance Inflation Factor (VIF):** VIF > 10 often indicates multicollinearity.

### Solutions:
- Drop one of the correlated variables.
- Combine correlated variables into a single feature (e.g., PCA).

## Causality
- Focuses on the cause-and-effect relationship between variables.
- One variable influences another (e.g., temperature affects ice cream sales).
- Helps answer “What causes what?” to predict outcomes and make better decisions.
- **Example:** Higher temperature → Increased cold drink sales.

## R Squared | R<sup>2</sup> | Coefficient of Determination
- Measures how well the regression line fits the data. How well the **Regression line** predicts almost **actual value**.
- Indicates how much of the variance in the dependent variable is explained by the model.

### Range: 0 to 1
- **Closer to 1:** Better fit, model explains most of the variance.
- **Closer to 0:** Poor fit, model explains little variance.
- Example: R² = 0.85 | 85% of the variation in the target variable is explained by the independent variables.

![R is Low](Image/R007.png)

![R is Low](Image/R090.png)

![R is Low](Image/R1.png)

![Difference](Image/RRS.png)

## Covariance (Direction)
- Definition: Measures how two variables change together.
- Purpose: Understand the directional relationship between two datasets.

### Types:
- **Positive Covariance:** Variables move in the same direction.
- **Negative Covariance:** Variables move in opposite directions.

### Example:
- Height & Weight → Positive covariance (both increase together).
- Price & Demand → Negative covariance (price ↑, demand ↓).

## Sampling Facts: 
- A sample is never a perfect representation of the population.
- Different samples from the same population can produce different means.
- Variations often occur due to sampling error.
- Example: If you take two random samples of 100 people from a city, their average income may differ slightly because of sampling variability.

## P-value
- **Definition:** Probability of observing results as extreme as the actual data, assuming the null hypothesis is true.
- **Purpose:** Determines statistical significance of results.

### Interpretation:
- **p ≤ 0.05:** Strong evidence against the null | Reject NULL Hypothesisi (H₀).
- **p ≥ 0.05:** Weak evidence against the null | Fail to reject NULL Hypothesis (H₀).
- **p ≤ 0.01:** Very strong evidence against the NULL Hypothesis (H₀).
- Example:If p = 0.03, there’s a 3% chance results occurred under the NULLL Hypothesis → reject H₀.

### Scenario: Coin Flip 
- Imagine you have a fair coin (Head/Tails)
- **Normal scenario:** If you flip a fair coin, it will end up in any random combinations of heads or tails.
- **Exceptional case:** But it ends up in 10 Heads, now you suspect it might be biased towards Heads.

Here's how p-value can help you test the suspicion:
- **Null Hypothesis (H0):** The coin is fair (One side is the head and another side is the tail)
- **Alternate Hypothesis (Ha):** The coin is biased (It will fall on either head)
- **Observed Data:** You flip the coin, say, 10 times. Surprisingly, you get Heads every single time!
- **Test Statistic:** This would be the number of heads observed, which in this case is 10 out of 10 flips.
- In a fair case, it'll not be always possible to get 10 Heads every time.
- The p-value tells you how often you'd expect to see 10 heads in a row! in those hypothetical repetitions.
- We can say that there is only less than 5% or 1% chance it may happen.
- If **p-value >= 0.05** i.e. Here it's a normal scenario (Fair coin, NULL hypothesis accepted)
- If **p-value <= 0.05** i.e Very rare scenario of getting H only (The coin is biased)

## Types of Statistical Tests
- Statistical tests are used to make inferences about a population based on a sample of data. 

### Parametric Tests
- Parametric tests assume that the data is normally distributed and that the population parameters are known or can be estimated.

**1. T-test:**
- T-test compares the means of groups.
- **One-sample t-test:** Compares the mean of a single sample to a known population mean.
- **Independent samples t-test:** Compares the means of two independent groups.
- **Paired samples t-test:** Compares the means of two related groups (e.g., before-after measurements).   

**2. ANOVA (Analysis of Variance):**
- Used to compare means of more than two groups.
- **One-way ANOVA:** Compares the means of multiple groups on a single independent variable.
- **Two-way ANOVA:** Compares the means of multiple groups on two independent variables.

**Z-test:**
- Compares population means when the population standard deviation is known.
- Often used in hypothesis testing and confidence interval estimation.

### Non-parametric Tests
- Non-parametric tests do not assume that the data is normally distributed.
- They are often used when the sample size is small or the data is skewed.

**1. Chi-Square Test:**
- Used to analyze categorical data.
- **Chi-square goodness-of-fit test:** Compares observed frequencies to expected frequencies.
- **Chi-square test of independence:** Tests the association between two categorical variables.
