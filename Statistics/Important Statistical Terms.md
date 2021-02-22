# Statistical Concepts you should know for Data Science

### 1. P Values

- **Probability** of **Achieving** a result.
- if p value < alpha (0.05 | 5%) we remove that feature.
- if p value > alpha (0.05 | 5%) we keep that feature.

### 2. Z Test

- A **Hypothesis Test** with a **Normal Distribution** that uses a **Z Statistics**.
- We use **Z Test** when we have **Large Sample Size**.

### 3. T Test

- A **Hypothesis Test** with a **T Distribution** that uses a **T Statistics**.
- We use **T Test** when we have **Small Sample Size**.

### 4. Linear Regression and Assumptions

- Model **Relationship** between a **Dependent Variable** and one or nore **Independent Variable**
- Finding the Line of **Best Fit** that represents two or more variables.
- Line of Best Fit is found by minimizing the **Sum of Squared Residuals**
- Residuals : **Predicted** - **Actual**

Assumptions

1. **Linearity** : The Relationship between **X** and **Mean** of **Y** is linear.
2. **Homoscedasticity** : The **Variance** of the **Residual** is the same for any value of **X**.
3. **Independence** : **Observations** are **Independent** of each other.
4. **Normality** : For any value of **X**, **Y** is normally distributed.

### 5. Logistic Regression 

1. Model the **Probability** of a **Discrete** Number of outcomes.
2. Predict whether a person is **Alive** or **Dead** based on their **age**.
3. **Sigmoid** function is used to get **Probability**.
4. **Probability** can be converted to a **Binary Output**, either **1** or **0**.
5. **Gradient Descent** and **Maximum Liklihood** are used to Adjust **Weights**.

### 6. Sampling

1. Simple Random Sampling

- Selecting **Random Data Values** from the Dataset.

2. Systematic Sampling

- **Take** One Data Value, **Skip** a predefined amount (n), **Take** next Data Value.

3. Cluster Sampling

- Divide **Population** into Clusters and Select One entire **Cluster** as Samples.

4. Stratified Sampling

- Divide **Population** into groups of Similar **Attributes**
- Take **Random Samples** from each groups.

### 7. Central Limit Theorem

- The **Distribution** of Sample Mean approximates a **Normal Distribution**.
- Take Sample from Dataset and Calculate its **Mean** of Sample.
- If we Plot frequencies on Graph it will create a **Bell Curve**, also known as a **Normal Distribution**.
- We can improve the **Accuracy** of the **Mean** and **Reduce** the **Standard Devation** of Larger Samples of Data.

### 8. Combinations and Permutations

- Different ways to **Select Objects** from the **Datasets** to form **Subsets**.
- Permutation consider **Order** of Subset.
- Combinaton do not consider **Order** of Subset.

1. Permutation
- A Permutation of n elements is an arrangement of those n elements in a **Definite Order**.
- There are (**n!**) ways to **Arrange** elements in order.
- P<sub>n,r</sub> = n! / (n-r)!
- Number of **r** taken from **n** different elements.

2. Combination
- The Number of ways to choose **r** out of **n** Objects where Order doesn't matters.
- C <sub>r</sub><sup>n</sup> = n! / (n-r)! * r!

### 9. Bayes Theorem

- Conditional Probability Statement
- Probability of event **B** happening given that another event **A** has already happened.
- P(A|B) = P(B|A) * P(A) / P(B)

### 10. Probability Distributions

- **Probabilities** of different possible outcomes in an experiment.
- **Frequency** of **Occurence**.
- The **Likelihood** of an outcome.
- **Y** denotes **Actual Outcome** of an event.
- **y** denotes **One possible outcome**.
- **Mean** and **Variance** are the important terms considered in **Distribution**.

- Variance : How **spread out** the data is? | How **far away** the values are from the mean.
- Population : All Data
- Sample : Part of Data

### Types of **Distribution**.

- **Finite** number of outcomes : Die | Picking a Card : **Discrete** distribution.
- **Infiinite** number of outcomes : Time | Distance : **Continuous** distribution.

How to Read Distribution?

### X ~ U(3,7)
- Variable **X** follows an **Uniform Distribution** ranging from 3 to 7.

### Discrete Events 
- Events with Finite outcomes follows **Uniform Distribution | U(a,b))**. (Only One Coin Flip) 
- Event with Two Outcomes per **Iterations** follows **Binomial Distribution**. (Coin Flip Iterations)
- Events with only Two possible outcomes follows **Bernoulli Distribution**. (True or False | Yes or No | Male or Female)
- Event with Frequency of Occurence (May happen or not) follows **Poisson Distribution** (Number of **Goals** in Football or Number of **Baskets** in Basketball).

### Continuous Events
- Events Normal in Nature. (Average Height of Person) follows **Normal Distribution**.
- Events Normal in Nature but limited Sample follows **T Distribution**.
- **Chi Squared Distribution** : Asymmetric Distribution Starts from 0 and only positive : Measure Goodness of Fit
- Rapid changing Event follows **Exponential Distribution**.
- Forecast and Prediction Events follows **Logistic Distribution**. (Which Team will Win, Weather Forecast)

Uniform Distribution 
- Outcomes with equal **Probability**
- A Die, A Coin

A. **Normal** Distribution | **Gaussian** Distribution | **Bell Shaped Curve** 
- Mean = 0 and Standard Deviation = 1

B. **Poissson** Distrbution | Po(**lambda**)
- Number of **Occurences**.
- The Frequency with which an Event occurs within a specific interval. 
- e.g. a Fire Fly lights up 3 times in 10 Seconds.

