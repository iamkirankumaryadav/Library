<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Statistical Concepts you should know for Data Science

<h3> <a href='#data'>Data </a> | <a href='#hyp'>Hypothesis </a> | <a href='#sample'>Sampling </a> </h3>

### Independent | Feature | Regressor | Explanatory | Input | Predictor

### Dependent | Labels | Regressand | Response | Output

### Vocabulary of Data:

1. `Continuous` (Height, Weight, 2.5, float) vs `Discrete` (Car Model, Number of Legs or Hands, 100, No. on Dice, Integer, String)
2. Structured vs Unstructured
3. Nominal vs Ordinal
4. Population vs Sample

<h3 name='data'> Data Set </h3> 

- A **collection** of `sample` or entire `population`

### Type of Data 
- `Quantitative` ( Real numeric : Discrete or continuous )
- `Categorical` ( Binary, nominal or ordinal )
 
### Statistical Analysis
- Investigating `trends`, `patterns`, and `relationships` using `quantitative` data.

### Descriptive Statistics

- Reduce large array of numbers (rows) into a handful of figures (KPI's) tha describe it accurately.
- Understand what your sample data looks like, summarize the characteristics of a `variable`
- `Frequency`: Count the observations of each value in a variable ( Histogram or Frequency Table )
- `Relative Frequency`: Count of each value as a percentage of total.
- `Cumulative Relative Frequency`: Running total of the relative frequencies.
- `Central tendency`: Represent middle of the values ( `Mean`, `Median` and `Mode` ) ( Skew )
- `Variability`: Dispersion of values ( `Min`, `Max`, `Range`, `IQR`, `Standard Deviation` and `Variance` ) ( Box & Whisker Plot )
- `Standard Deviation`: The average amount of `variability` ( Scatter Plot )
- `Variance`: Squared deviations from mean. ( Actual - Predicted ) <sup>2</sup>

### Variables

- There are two main type of variables in a dataset.
- `Numerical`: Represents numbers that meant to be `aggregated`.
- `Categorical`: Represents groups that can be used to `filter` numerical values.

### Inferential Statistics
- **Understand** the Population from the `Sample`.
- Test `Hypothesis` and **Draw Conclusion** about **Population Parameters** based on a `Sample` taken from Population. 
- `Sample` is likely to be a **Good Representation** of `Population`.
- `Sample` will never be a **Perfect Representation** of `Population` ( Sampling Error )
- Way the Sample is taken Matters ( Unbiased Sampling )
- Population Parameters ( Mean, Median, Standard Deviation, Difference between Means )
- Simple Test ( Hypothesis, T test, Chi<sup>2</sup> test )
- Regression Analysis ( Simple Linear, Multiple Linear and Logistic )
- Correlation 
- ANOVA ( One way and Two Way )

![Inferential Statistics vs Descriptive Statistics](Image/InferentialvsDescriptive.jpg)

Descriptive Statistics | Inferential Statistics 
:--- | :---
**Organizing** and **Summarizing** Data using **Numbers** and **Graphs** | Using **Sample** Data to draw a certain **Conclusion** for Population
Describe **Characteristics** of **Sample** or **Population** | Draw **Conclusion** of Population Data 
**Collecting**, **Organizing**, **Summarizing** and **Presenting** Data | Drawing **Conclusions**, performing **Estimations** and making **Predictions** 
Measure of **Central Tendency** and **Dispersion** | **Hypothesis Test, ANOVA**
Data set is **Small** | Dataset is **Large** 

### Quantitative Data
- Process of Collecting and Analyzing **Numerical** Data
- Find **Trends**, **Patterns**, **Relationship** and **Correlation**
- Dealing with Measuring **Central Tendency** and **Measures of Spread** 
- Analysis is done on **Sample** that Generalize Results for **Population**

### Qualitative Data
- Process of Collecting and Analyzing **Non Numerical** Data
- Text, Image, Video or Audio
- Gather **Insights** by converting in  form of **Array**

Quantitative Data | Qualitative Data
:--- | :---
Numerical Data | Non Numerical Data
Confirm or Test ( Hypothesis ) | Understand ( Concepts )
Find **Trends**, **Relations** and **Patterns** | Find **Insights**
Numeric Data ( Central Tendency and Measures of Spreads ) | Text, Image, Video or Audio

### Level of Measurements

1. **Nominal** : Data can only be Categorized ( No Order )
2. **Ordinal** : Data can be Categorized and Ranked ( Order )
3. **Interval** : Data can be Categorized, Ranked, and Evenly Spaced
4. **Ratio** : Data can be Categorized, Ranked, Evenly Spaced, and has a Natural Zero.

![Level of Measurement](Image/Levels.png)

<h3 name='hyp'> Hypothesis Test</h3> 

- Leverage the `central limit theorem` to draw conclusions about what `population` looks like based on `sample`.
- Test Specific **Prediction** or **Claim**
- An **Assumption** | An **Idea** that is Proposed so that it can be **Tested** to See if it might be **True**
- We Test the Liklihood of Statement being **True** in order to decide whether to **Accept** or **Not Accept** the **NULL Hypothesis**

NULL Hypothesis | Alternative Hypothesis 
:--- | :---
H<sub>0</sub> | H<sub>a</sub>
Statement about a **Population** Parameter | Statement directly **Contradicts** the NULL Hypothesis
H<sub>0</sub> : U = U<sub>0</sub> | H<sub>a</sub> : U != U<sub>0</sub> or H<sub>a</sub> : U < U<sub>0</sub> or H<sub>a</sub> : U > U<sub>0</sub>

![Hypothesis Test](Image/Hypothesis.png)

### Type I and Type II Error

**Type I** Error : The **Null Hypothesis** is **True** but **Rejected**

**Type II** Error : The **Null Hypothesis** is **False** but **Fails** to **Reject**

![Error Type](Image/ErrorType.jpg)

### 1. P Values ( Significance Value )

- **Probability** Value of **Achieving** a result. ( **H0** | Null Hypothesis to be **True** and **Accepted** )
- More **Likely** Observation around Mean | Median | Mode
- Determine **Strength** | **Significance** of Research Results in **Hypothesis Test**.
- if P value < alpha ( 0.05 | 5% ) we **remove** that feature. ( **Reject** Null Hypothesis )
- if P value > alpha ( 0.05 | 5% ) we **keep** that feature. ( **Accept NULL Hypothesis** : **H0** )
- **P Value** lies between `0` to `1`.
- Two Tail Test, Left Tail Test and Right Tail Test.
- **Confidence Interval** : `95%` and **Significance Level** as : `5%`

**Significance** Level ( **Alpha** )
- At what point the **Null Hypothesis** is **Rejected**.
- Significance Level is usually ( 5% or 1% )
- Alpha <= 1% | High Significance
- Alpha <= 5% | Significant
- Alpha > 5% | No Significant ( Accept Null Hypothesis )

### 2. Z Test

- A **Hypothesis Test** with a **Normal Distribution** that uses a **Z Statistics**.
- We use **Z Test** when we have **Large Sample Size** ( **Data Size** > 30 )
- Used when Data Points are **Independent** and Data is **Normally** Distributed ( Data is Selected Randomly ).

### 3. T Test

- A **Hypothesis Test** with a **T Distribution** that uses a **T Statistics**.
- We use **T Test** when we have **Small Sample Size** ( **Data Size** < 30 )
- Data is **not** distributed Normally and Data is not selected **Randomly**.
- **T Distribution** has **Small Peak** and **Fat Tails**.
- Used to Compare the `Means` of Two Groups.

### Types of T Test 
1. One Sample : Groups come from a Same Population ( Compare `Means` and `Standard Deviations` )
2. Paired Sample : Group from Same Population ( Before and After Experiment )
3. Two Sample : Groups come from Different Populations ( Two Different People from Two Different Cities )

### 4. ANOVA Test

- Analysis of `Variance`
- Used to Test Categorical Variable ( Atleast 3 Different Categories )
- Analyze the Difference between the **Means** of more than Two Groups
- One Way ANOVA uses one **Independent Variable**
- Two Way ANOVA uses two **Independent Variables**

### Assumptions of ANNOVA Test
- Observations are **Independent** and **Dependent Feature** follows **Normal** Distribution.
- **Variation** for each Group in Category should be **Similar**.

### 5. Assumptions of Linear Regression

1. **Linearity** : The Relationship between **X** and **Mean** of **Y** is linear.
2. **Homoscedasticity** : The **Variance** of the **Residual** is the same for any value of **X**.
3. **Independence** : **Observations** are **Independent** of each other.
4. **Normality** : For any value of **X**, **Y** is normally distributed.

### 6. Logistic Regression 

1. Model the **Probability** of a **Discrete** Number of outcomes.
2. Predict whether a person is **Alive** or **Dead** based on their **age**.
3. **Sigmoid** function is used to get **Probability**.
4. **Probability** can be converted to a **Binary Output**, either **1** or **0**.
5. **Gradient Descent** and **Maximum Liklihood** are used to Adjust **Weights**.

<h3 name='sample'> 6. Sampling</h3>

1. Simple Random Sampling

- Selecting **Random Data Values** from the Dataset.
- Each Data Value has `Equal` Chance of being Selected.
- e.g. Select any Random Data Point.

2. Systematic Sampling

- **Take** One Data Value, **Skip** a predefined amount (n), **Take** next Data Value.
- Choose a Data Point at **Regular Intervals**
- e.g. Selecting every 10th Data Point from 100.

3. Cluster Sampling

- Divide **Population** into Clusters and Select One or more **Clusters** as Samples.
- Used when the Data Set is **Very Large**.

4. Stratified Sampling

- Divide **Population** into groups of Similar **Attributes** with Equal Proportion.
- Take **Random Samples** from each groups.
- e.g. If Company has 400 Males and 300 Feamles, Choosing 40 Males and 30 Females. 

![Sampling](Image/Sampling.png)

### 7. Central Limit Theorem

- The **Distribution** of Sample Mean approximates a **Normal Distribution**.
- If we Plot frequencies on Graph it will create a **Bell Curve**, also known as a **Normal Distribution**.
- We can improve the **Accuracy** of the **Mean** and **Reduce** the **Standard Devation** of Larger Samples of Data.

### 8. Combinations and Permutations

- Different ways to **Select Objects** from the **Datasets** to form **Subsets**.
- Permutation consider **Order** of Subset.
- Combinaton do not consider **Order** of Subset.

1. Permutation
- A Permutation of n elements is an arrangement of those n elements in a **Definite Order**.
- There are ( **n!** ) ways to **Arrange** elements in order.
- P<sub>n,r</sub> = n ! / ( n-r )!
- Number of **r** taken from **n** different elements.

2. Combination
- The Number of ways to choose **r** out of **n** Objects where Order doesn't matters.
- C <sub>r</sub><sup>n</sup> = n ! / ( n-r ) ! * r !

### 9. Bayes Theorem

- **Conditional** Probability Statement
- Probability of event **B** happening given that another event **A** has already happened.
- P ( A | B ) = ( P ( B | A ) * P ( A ) ) / P( B )

### 10. Probability Distributions
- If the sample data fits a probability distribution, use it as a model for the entire population.
- **Probabilities** of different possible outcomes in an experiment.
- **Frequency** of **Occurence**.
- The **Likelihood** of an outcome.
- **Y** denotes **Actual Outcome** of an event.
- **y** denotes **One possible outcome**.
- **Mean** and **Variance** are the important terms considered in **Distribution**.
- Variance : How **spread out** the data is? | How **far away** the values are from the mean.
- Population : All Data
- Sample : Part of Data

### 11. Chi Squared Test
- Measure **Goodness** of **Fit** : **Sample** Data matches a **Population**
- A **Very Small** Chi Square Test Statistic means Observed Data **Fits** your expected Data **Extremely Well**.
- A **Very Large** Chi Square Test Statistic means Data does not **Fits** Well.
- A Test for **Independence** of two Categorical Variables and returns **Probability**.
- Derive **Statistical Significance** of Relationship between the Variables.
- Test whether the **Evidence** in the **Sample** is Strong enough to **Generalize** that relationship for a **Population**.
- Difference between **Expected** and **Observed**
- Probability = 0 indicates both Categorical Variable are **Dependent**.
- Probability = 1 indicates both Categorical Variable are **Independent**.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
