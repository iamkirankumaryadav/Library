<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Logistic Regression

- `Model` used for `classification`
- Especially `binary` classification | Assign observations to a `discrete` set of classes.
- Predict the `probability distribution` of class which lies within Range `0` and `1`.
- Transforms output using `Sigmoid` function to return a `probability distribution` value ( Mapped to 2 `discrete` classes )
- Explain relationship between one dependent **binary** variable and one or more **nominal** or **ordinal** independent variable.

### Logistic Function  | Sigmoid ( S Shaped Curve ) Function
- Accepts any `real` value and map it into a value between `0` and `1`
- The probability prediction must be transformed to `binary` | dichotomous ( `0` and `1` )
- Threshold | Decision boundary : 0.5 ( `Probability` < `0.5` is considered as `0` else `1` )

### When to Use Logistic Regression
- **Binary** target variable | Better to use with small data set.
- **Fair** data ( Not to many `outliers` or `missing` data in the data set ) 
- Logistic regression is good for **fast training** ( It is not the best performing model )

### Remove Correlated Independent Feature
- The model can `overfit` if you have multiple highly correlated independent features.
- Calculate the pairwise correlations between all independent features and removing highly correlated independent feature.

### Example
- **Linear regression** helps us to predict the student's test score on a scale of 0 - 100 | `Continuous`
- **Logistic regression** helps us to classify whether the student is passed or failed | `Discrete`

### Types of Logistic Regression
1. Binary (Pass(1) | Fail(0))
2. Multiclass or Multinomial (Cats | Dogs | Sheep)
3. Ordinal (Low | Medium | High)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
