<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Fundamentals for Data Science

<h3> <a href='#data'>Data </a> | <a href='#hyp'>Hypothesis </a> | <a href='#sample'>Sampling </a> </h3>

### Independent | Feature | Matrix |  Regressor | Explanatory | Input | Predictor

### Dependent | Labels | Vector | Regressand | Response | Output

## Vocabulary of Data:

### Quantitative Data
- **Definition:** Data that can be measured and expressed numerically. Quantitative = “How much?” (numbers)
- **Nature:** Objective, structured, statistical.
- Examples: Age, height, weight, test scores, income, temperature.
- Used For: Statistical Analysis, Hypothesis Testing, and Predictive Modeling.

### Qualitative Data
- **Definition:** Data that describes qualities or characteristics; non-numeric. Qualitative = “What kind?” (descriptions)
- **Nature:** Subjective, descriptive, exploratory.
- Examples: Opinions, feelings, experiences, colors, textures, interview responses.
- Used For: Understanding Patterns, Exploring Reasons and Motivations, and Thematic Analysis.

Continuous | Discrete
:--- | :---
Any value | Specific value
Complicated measurement | Easily counted
Height 5'11'', 179.5 cm, Weight 75.5 kg |  # of kids in classroom, # of votes in election

Structured | Unstructured
:--- | :---
Predefined structure (Rows and Columns / Key and Value) | No predefined structure
Quantitative | Qualitative
Excel, JSON, XML, SQL | Image, Text, Video, Audio, PDF, Doc

Nominal | Ordinal
:--- | :---
Cannot be arranged in order | Can be sorted, arranged in order, ranked 

Population | Sample
:--- | :---
Entire available data set | Subset, sample, or representative of the true population

<h3 name='data'>Dataset</h3> 

- A collection of the sample or the entire population.

### Type of Data 
- **Quantitative:** Real numeric: discrete or continuous.
- **Categorical:** Binary, nominal, or ordinal.
 
### Statistical Analysis
- Investigating trends, patterns, and relationships using quantitative data.

### Descriptive Statistics
- Summarize a large array of numbers (rows) into a handful of figures (KPIs) that describe it accurately.
- Understand what your sample data looks like, summarize the characteristics of a variable.
- **Frequency:** Count the observations of each value in a variable (Histogram or Frequency Table)
- **Relative Frequency:** Count of each value as a percentage of total.
- **Cumulative Relative Frequency:** Running total of the relative frequencies.
- **Central tendency:** Represent middle of the values (Mean, Median, and Mode) (Skewness)
- **Variability:** Dispersion of values (Min, Max, Range, IQR, Standard Deviation, and Variance) (Box & Whisker Plot)
- **Standard Deviation:** The average amount of variability (Scatter plot)
- **Variance:** Squared deviations from mean. (Actual - Predicted)<sup>2</sup>

### Skewness
- Skewness is a measure of how symmetrical a distribution is, it specially means lack of symmetry.
- It gives the direction (Right/Left) and magnitude (Positive/Negative + Mean/Median/Mode) of the lack of symmetry.
- No skewness: Data points are normally distributed (Mean = Median = Mode)
- Positive/Right skewness: Long/Extended tail on the right side (Mean > Median > Mode)
- Negative/Left skewness: Long/Extended tail on the left side (Mode > Median > Mean)
- Variance tells us about the amount of variability (Figure/Scale)
- Skewness gives the direction of variability (Compares Mean, Median, and Mode)
- Kurtosis measures the flatness of distribution.

### Variables
- There are two main types of variables in a dataset.
- **Numerical:** Represents numbers that meant to be aggregated.
- **Categorical:** Represents groups that can be used to filter numerical values.

### Inferential Statistics
- Understand the population from the sample.
- Test hypothesis and **draw conclusion** about **population parameters** based on a sample taken from population. 
- Sample is likely to be a **good representation** of population.
- Sample will never be a **perfect representation** of population (Sampling error)
- The way the sample is taken matters (Unbiased/Imbalanced/Balanced sampling)
- Population Parameters (Mean, Median, Mode, Standard Deviation)
- Simple Test (Hypothesis, T-test, Chi<sup>2</sup> test)
- Regression Analysis (Simple Linear, Multiple Linear and Logistic)
- Correlations and Multicollinearity. 
- ANOVA (One way and Two Way)

![Inferential Statistics vs Descriptive Statistics](Image/InferentialvsDescriptive.jpg)

Descriptive Statistics | Inferential Statistics 
:--- | :---
Organizing and summarizing data using numbers and graphs | Using sample data to draw a certain conclusion for the population
Describe characteristics of sample or population | Draw some conclusion on population data 
Collecting, organizing, summarizing and presenting data | Drawing conclusions, performing estimations and making predictions
Measure of central tendency and dispersion | Hypothesis Test, ANOVA
Dataset is small | Dataset is large (True population is considered)

### Quantitative Data
- Process of collecting and analyzing numerical data.
- Find trends, patterns, relationships and correlations.
- Dealing with measuring central tendency, measures of spread/dispersion, distribution and skewness of data. 
- Analysis is done on the sample that generalizes/concludes results for the true population.

### Qualitative Data
- Process of collecting and analyzing non-numerical data.
- Text, Image, Video or Audio.
- Gather insights by converting them in the form of **array**.

Quantitative Data | Qualitative Data
:--- | :---
Numerical data | Non-numerical data
Confirm or Test (Hypothesis) | Understand (Concepts)
Find trends, relationships, and patterns | Find insights
Numeric data that can be summarized (Central tendency and measures of spreads) | Text, Image, Video or Audio

### **Level of Measurements**

1. **Nominal**: Data can only be categorized (No Order/Rank/Sort)
2. **Ordinal**: Data can be categorized, ranked, and arranged in order.
3. **Interval**: Data can be categorized, ranked, and evenly spaced.
4. **Ratio**: Data can be categorized, ranked, evenly spaced, and can be a natural zero.

![Level of Measurement](Image/Levels.png)

<h3 name='hyp'>Hypothesis Test</h3> 

- Leverage the **central limit theorem** to conclude what population looks like based on sample.
- Test specific **prediction** or **claim**.
- An **assumption** | An **idea** that is proposed so that it can be **tested** to see if it might be **true**
- We test the likelihood of statement being **true** in order to decide whether to **accept** or **not accept** the **NULL Hypothesis**

**NULL Hypothesis** | **Alternative Hypothesis** 
:--- | :---
H<sub>0</sub> | H<sub>a</sub>
Statement about a **population** parameter | Statement directly **contradicts** the NULL hypothesis.
H<sub>0</sub> : U = U<sub>0</sub> | H<sub>a</sub> : U != U<sub>0</sub> or H<sub>a</sub> : U < U<sub>0</sub> or H<sub>a</sub> : U > U<sub>0</sub>

![Hypothesis Test](Image/Hypothesis.png)

### Type I and Type II Error

**Type I Error** : The **Null Hypothesis** is **true** but **rejected** (False Positive)

**Type II Error** : The **Null Hypothesis** is **false** but **fails** to **reject** (False Negative)

![Error Type](Image/ErrorType.jpg)

### 1. P Values (Significance Value)

- **Probability** value of **achieving** a result. (**H0** | Null Hypothesis to be **true** and **accepted**)
- More likely observation around Mean | Median | Mode
- Determine **strength** | **significance** of research results in **Hypothesis Test**.
- if P value < alpha ( 0.05 | 5% ) we **remove** that feature. ( **Reject** Null Hypothesis )
- if P value > alpha ( 0.05 | 5% ) we **keep** that feature. ( **Accept NULL Hypothesis** : **H0** )
- **P Value** lies between `0` to `1`.
- Two tail test, left tail test and right tail test.
- **Confidence Interval** : `95%` and **Significance Level** as : `5%`

**Significance** Level (**Alpha**/Percentage)
- At what point the **Null Hypothesis** is **rejected**.
- Significance Level is usually (5% or 1%)
- Alpha <= 1% | High Significance
- Alpha <= 5% | Significant
- Alpha > 5% | No Significant (Accept Null Hypothesis)

### 2. Z Test
- A **Hypothesis Test** with a **Normal Distribution** that uses a **Z Statistics**.
- We use **Z Test** when we have **large sample size** (**Data Size** > 30)
- Used when data points are **independent** and data is **Normally** Distributed (Data is Selected Randomly) .

### 3. T Test
- A **Hypothesis Test** with a **T Distribution** that uses a **T Statistics**.
- We use **T Test** when we have a very **small sample size** (**Data Size** < 30)
- Data is **not** distributed Normally and data is not selected **Randomly**.
- **T Distribution** has **small peak** and **fat tails**.
- Used to compare the `Means` of two groups.

### Types of T Test 
1. One Sample: Groups come from a same population (Compare `Means` and `Standard Deviations`)
2. Paired Sample: Group from same population (Before and After Experiment)
3. Two Sample: Groups come from different populations (Two different people from two different cities)

### 4. ANOVA Test

- Analysis of `Variance`
- Used to test categorical variable (Atleast 3 Different Categories)
- Analyze the difference between the **Means** of more than two groups
- One way ANOVA uses one **Independent Variable**
- Two way ANOVA uses two **Independent Variables**

### Assumptions of ANNOVA Test
- Observations are **independent** and **dependent feature** follows **Normal** Distribution.
- **Variation** for each group in category should be **similar**.

### 5. Assumptions of Linear Regression

1. **Linearity**: The relationship between **X** and **mean** of **Y** is linear.
2. **Homoscedasticity**: The variance of the **residual** is the same for any value of **X**.
3. **Independence**: **Observations** are **independent** of each other.
4. **Normality**: For any value of **X**, **Y** is normally distributed.

### 6. Logistic Regression 

1. Model the **probability** of a **discrete** number of outcomes.
2. Predict whether a person is **alive** or **dead** based on their **age**.
3. **Sigmoid** (H0) function is used to get **probability**.
4. **Probability** can be converted to a **binary output** with the logit function, either **1** or **0**.
5. **Gradient descent** and **maximum liklihood** are used to adjust **weights**.

<h3 name='sample'> 6. Sampling</h3>

1. Simple Random Sampling

- Selecting **random data values** from the dataset.
- Each data value has `equal` chance of being selected.
- e.g. Select any random data point.

2. Systematic Sampling

- **Take** one data value, **skip** a predefined amount (n), **take** next data value.
- Choose a data point after **regular intervals**
- e.g. Selecting every 10th Data Point from 100.

3. Cluster Sampling

- Divide **population** into clusters and select pne or more **clusters** as samples.
- Used when the data set is **very large**.

4. Stratified Sampling

- Divide **population** into groups of similar **attributes** with equal proportion.
- e.g. If Company has 400 Males and 300 Feamles, Choosing 40 Males and 30 Females. 

![Sampling](Image/Sampling.png)

### 7. Central Limit Theorem

- The **distribution** of sample mean approximates a **normal distribution**.
- If we plot frequencies on graph it will create a **Bell Curve**, also known as a **Normal Distribution**.
- We can improve the **accuracy** of the **Mean** and reduce the **Standard Devation** of larger samples of data.

### 8. Combinations and Permutations

- Different ways to **select objects** from the **datasets** to form **subsets**.
- Permutation consider **order** of subset.
- Combinaton do not consider **order** of subset.

1. Permutation
- A Permutation of n elements is an arrangement of those n elements in a **definite order**.
- There are ( **n!** ) ways to **arrange** elements in order.
- P<sub>n,r</sub> = n ! / ( n-r )!
- Number of **r** taken from **n** different elements.

2. Combination
- The number of ways to choose **r** out of **n** Objects where order doesn't matters.
- C <sub>r</sub><sup>n</sup> = n ! / ( n-r ) ! * r !

### 9. Bayes Theorem

- **Conditional** probability statement
- Probability of event **B** happening given that another event **A** has already happened.
- P ( A | B ) = ( P ( B | A ) * P ( A ) ) / P( B )

### 10. Probability Distributions
- If the sample data fits a probability distribution, use it as a model for the entire population.
- **Probabilities** of different possible outcomes in an experiment.
- **Frequency** of **occurence**, the **likelihood** of an outcome.
- **Y** denotes **actual outcome** of an event, **y** denotes one possible outcome.
- **Mean** and **variance** are the important terms considered in **distribution**.

### 11. Chi Squared Test
- **Measure goodness of fit:** Sample data matches with the true population.
- A very small Chi Square Test Statistic means observed data fits your expected data extremely well.
- A very large Chi Square Test Statistic means data does not fits well.
- A test for independence of two categorical variables and returns probability.
- Derive statistical significance of relationship between the variables.
- Test whether the evidence in the sample is strong enough to generalize** that relationship for a true population.
- Difference between expected and observed
- Probability = 0 indicates both categorical variables are **dependent**.
- Probability = 1 indicates both Categorical variables are **independent**.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
