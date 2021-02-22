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
