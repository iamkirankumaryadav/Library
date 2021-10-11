<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Logistic Regression

- `Model` used for `classification`
- Especially `binary` classification | Assign observations to a `discrete` set of classes.
- Predict the `probability distribution` of class which lies within Range `0` and `1`.
- Transforms output using `Sigmoid` function to return a `probability distribution` value ( Mapped to 2 `discrete` classes )
- Explain relationship between one dependent **binary** variable and one or more **nominal** or **ordinal** independent variable.

### Logistic Function  | Sigmoid ( S Shaped Curve ) Function
- Accepts any `Real` Value and Map it into a Value between `0` and `1`
- The Probability Prediction must be Transformed to `Binary` | Dichotomous ( `0` and `1` )
- Threshold | Decision Boundary : 0.5 ( `Probability` < `0.5` is Considered as `0` else `1` )

### When to Use Logistic Regression
- **Binary** Target Variable | Better to Use with Small Data Set
- **Fair** Data ( Not to Many `Outliers` or `Missing` Data in the Data Set ) 
- Logistic Regression is good for **Fast Training** ( It is not the Best Performing Technique )

### Remove Correlated Independent Feature
- The Model can Overfit if you have Multiple Highly Correlated Independent Features
- Calculate the Pairwise Correlations between all Independent Features and removing Highly Correlated Independent Feature.

### Example
- **Linear Regression** Helps us to Predict the Student's Test Score on a Scale of 0 - 100 (Continuous)
- **Logistic Regression** Helps us to Predict whether the Student is Passed or Failed (Discrete)

### Types of Logistic Regression
1. Binary (Pass(1) | Fail(0))
2. Multi (Cats | Dogs | Sheep)
3. Ordinal (Low | Medium | High)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
