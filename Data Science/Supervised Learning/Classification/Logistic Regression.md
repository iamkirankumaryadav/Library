<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Logistic Regression

- **Classification** Algorithm | Especially `Binary` Classification | Assign Observations to a `Discrete` Set of Classes.
- Predict the `Probability Distribution` of Class which lies within Range `0` and `1`.
- Transforms Output using `Sigmoid` Function to Return a `Probability Distribution` Value ( Mapped to 2 or more `Discrete` Classes )
- Explain Relationship between One Dependent **Binary** Variable and One or more **Nominal**, **Ordinal**, **Interval** or **Ratio** Independent Variable.

### Logistic Function  | Sigmoid ( S Shaped Curve ) Function
- Accepts any `Real` Value and Map it into a Value between `0` and `1`
- The Probability Prediction must be Transformed to Binary | Dichotomous ( `0` and `1` )

### When to Use Logistic Regression
- **Binary** Target Variable
- Better to Use with Small Data Set
- **Fair** Data ( Not to Many Outliers or Missing Data in the Data Set ) 
- Logistic Regression is good for **Fast Training** ( It is not the Best Performing Data )

### Prepare Data for Logistic Regression

Assumptions made by **Logistic Regression** about Distribution and Relationships in Data == Assumptions in **Linear Regression**.homoscedasticity

### 1. Binary Output Variable
- Predict Probability of Instance | Binary Classification Problems

### Remove Noise 
- Removing Outliers and Miss Classified Instances from Training Data 

### Gaussian Distribution
- A Linear Algorithm (With Non Linear Transform on Output)

### Remove Correlated Independent Feature
- The Model can Overfit if you have Multiple Highly Correlated Independent Features
- Calculate the Pairwise Correlations between all Independent Features and removing Highly Correlated Independent Feature.

### Sparse (Lot of Zeros)

### Example
- **Linear Regression** Helps us to Predict the Student's Test Score on a Scale of 0 - 100 (Continuous)
- **Logistic Regression** Helps us to Predict whether the Student is Passed or Failed (Discrete)

### Types of Logistic Regression
1. Binary (Pass(1) | Fail(0))
2. Multi (Cats | Dogs | Sheep)
3. Ordinal (Low | Medium | High)

Decision Boundary | **Threshold**

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
