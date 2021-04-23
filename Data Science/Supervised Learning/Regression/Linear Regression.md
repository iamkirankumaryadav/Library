<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Linear Regression 📈

<h3><a href='#linreg'>Linear Regression</a> | <a href='#simple'>Simple Linear</a> | <a href='multiple'>Multiple Linear</a> | <a href='#ols'>Ordinary Least Square</a> | <a href='#gd'>Gradient Descent</a> | <a href='#ass'>Assumptions</a></h3>

### Regression

- A **Statistical** Process for **Estimating** the **Relationships** between **Independent** and **Dependent Variables** to make **Predictions**.

### Linear Regression 

- **Target** Variable is **Continuous Numeric**
- The **Best Fit Line** which gives **Least** Number of **Errors** ( Difference between **Actual** and **Predicted** Value ) for given **Data Points**.
- Find the **Slope** ( Steepness of the Line | Angular Motion ) and **Intercept** ( Position of Line | Upward & Downward ) with Least **Residual**. 
- **Sensitive** to Overfitting ( But can be Prevented using some **Dimensionality Reduction**, **Regularization** and **Cross Validation** )

![Regression Line](Image/RegressionLine.png)

- **Learning** a Linear Regression Model means Estimating the Values of the **Coefficient** ( `Slope` and `Intercept` )
- **Predict** Dependent Variable based on One or More Independent Variables.
- **Measure** the Influence of One or More Independent Variable on Dependent Variable.
- **Predict** the Value of a **Feature** based on the Value of Another Feature.

### Y = B1 * X  + B0 or y = m * x + c

![Equation Line](Image/EquationLine.png)

### B1 | m : Slope 

- **Gradient** | **Steepness** in Line | **Direction** of Line | **Weight**
- Indicates how much the **Dependent Variable** changes, if an **Independent Variable**  changes by **One Unit**

![Positive Slope](Image/Positive.png)

![Negative Slope](Image/Negative.png)

### B0 | c : Intercept 

- Bias | Constant | The Place where **Regression Line** Intersects the Y Axis ( Value of Y when Value of X and Value of **Coefficients** = 0 )

### R<sup>2</sup> : Coefficient of Determination | Goodness of Fit

- **Explains** The **Variance** of the Data captured by the Model ( **0.7** to **0.9** is Good value for R<sup>2</sup> ) 
- If R<sup>2</sup> is 0.8 or 80% i.e. Regression Line Explaines 80% of **Variance** in Data | 80% of Prediction is Based on the **Available** Data.
- Larger R<sup>2</sup> indicates a **Better Fit** ( The Model can Explain the **Variation** of **Predictions** with Actual in much Better Way )
- R<sup>2</sup> = 1 corresponds to SSR = 0 ( **Perfect Fit** ) 
- Low R<sup>2</sup> causes **Underfitting**
- High R<sup>2</sup> results into **Overfitting**
- It Shows that Regression Line | **Best Fit Line** Predicts better than **Base Fit Line** ( **Mean** ) 

### [Residuals](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md) | Error ( e )

- **Actual** - **Prediction**

<h3 name='simple'>Simple Linear Regression</h3>

- Only One **Independent Features** and One **Dependent Variable** ( **Continuous Numeric** )
- Use **Statistics** to Estimate **Coefficients** ( `Slope` and `Intercept` )

<h3 name='multiple'>Multiple Linear Regression</h3>

- More than One **Independent Features** and only One **Dependent Variable** ( **Continuous Numeric** )
- Consider **Features** that have **Good Correlation** with **Dependent Variable**.
- Checking **Multicollinearity** is Important.

### Polynomial Regression

- Finding **Best Fit Curve**.

### Logistic Regression

- Dependent Variable is **Categorical**, Used for **Classification**. 
- **Probability** of **Occurence** of **Target Label** is Predicted on the basis of **Threshold** ( `0.5` )
- **Range** Value of **Prediction** lies between `0` to `1` ( **Binary** Classification )

### LASSO
- Use **Shrinkage**, Good for **Multicollinearity**

### Ridge Regression
- Good for Data with **Noise** and **Multicollinearity**.

### Stepwise Regression
- More Advance Technique, Uses Tests to Remove **Predictors**, Can Handle **Large Number** of **Independent Variables**.

<h3 name='ols'>Ordinary Least Squares (OLS)</h3>

- More than One **Independent Features**, **Minimize** the Sum of Squared **Residuals** | **Errors** 
- Sum ( Actual Data Point - Predicted Point ( Regression Line ) <sup>2</sup> )
- Treat Data as **Matrix** ( **Feature Matrix** and **Target Vector** )
- Use **Linear Algebra** | **Equation** of **Line** ( y = m * x + c ) to Estimate | Predict the **Optimal** Value for the **Coefficients**.

<h3 name='gd'>Gradient Descent</h3>

- **Optimizing** the Values of the **Coefficients** ( `Slope` and `Intercept` ) by **Iteratively** Minimizing the **Error** of Model on **Training Data**.
- Starts with Random Values for each **Coefficient**.
- Sum of Squared **Errors** | **Residuals** are Calculated for each Pair of **Independent** and **Dependent** Values.
- **Learning Rate** is used as a `Scale` and the **Coefficients** are updated in the direction towards **Minimizing** the **Error** | **Residuals**.
- The Process is Repeated until a **Minimum SSE | SSR** is Achieved or no further Improvement is Possible.
- **Learning Rate** ( **alpha** ) Parameters that determines the size of Improvement Step on each Iteration.

### Learning Rate
- Determine the **Step Size** at each **Iteration** while moving towards a **Minimum Loss Function** ( Minimum `Error` )
- **Step Size** is Decided on the Basis of How Far or Close is the **Global Minima**.
- Handles the Rate of **Convergence** and **Overshooting** ( High Learning Rate )

### Regularization
- Seek to **Minimize SSE | SSR** of the Model on **Training Data**, Reduce **Complexity** of Model ( **Overfitting** )
- Add some **Bias** on Training Data for Decreasing **Variance** on Test Data.

1. **LASSO** ( L1 ) : OLS is modified to minimize the **Absolute** Sum of Coefficients : Cost Function + ( Lambda ) * | Slope |
2. **Ridge** ( L2 ) : OLS is modified to minimize the **Squared** Sum of Coefficients : Cost Function + ( Lambda ) * Square( Slope )

Used when there is Collinearity ( One Independent Feature can completely Describe Other Independent Feature ) in Data. 

# Preparing Data for Linear Regression

<h3 name='ass'>Assumptions<h3>
  
- **Linearity** : There should be **Linear Relationship** between **Dependent Variable** and **Independent Variables**
- **Independence** : **Residuals** | **Errors** should be **Independent** of each other.
- **Normality** : **Errors** | **Residuals** of the **Data** should be **Normally Distributed**. 
- There should be Minimal **Multicollinearity** between **Independent Variables**
- Error should be **Normally** Distributed ( P Value > 0.05  ) | Quantile Quantile Point : Data Points should be Close to Line
- **Homoscedasticity** : **Variance** around the **Regression Line** should be **Same** for all values of the **Independent Variable**

![Error Normal Distribution](Image/ErrorDistribution.png)

- **Homoscedasticity** : **Variance** along the Line of **Best Fit** should remain **Constant** as we move along the line.
- Error Term in the Regression Model is **Constant**.
- **Variance** is Same for all **Data Points**.

![Homoscedasticity](Image/Homo.png)

- **Multicollinearity** : Two or more **Independent** Variables **Correlate** strongly with each other. ( Age - DOB )
- Observations and Features should be **Independent**  

### Covariance

- **Relationship** between Two Variables.
- **Positive** Covaraince : Two Variables tends to Move in **Same Direction**.
- **Negative** Covaraince : Two Variables tends to Move in **Opposite Direction**.
- **Direction** of the **Linear Relationship** between Variables.

### Correlation

- Measures **Strength** and **Direction** of **Relationship** between two **Quantitative** Variable.
- One Variable can Predict the other Variable, Varies between `-1` ( Perfect Negative ) to `1` ( Perfect Positivehat )

Amount of R | **Strength** of **Correlation**
:--- | :---
0.0  | **No** Correlation
0.1 - 0.3 | **Little** Correlation
0.3 - 0.5 | **Medium** Correlation
0.5 - 0.7 | **High** Correlation
0.7 - 1.0 | **Very High** Correlation

![Perfect Linear Correlation](Image/Perfect.png)

![Direction of Slope](Image/Direction.png)

![Strength of Slope](Image/Strength.png)

### Test Correlation Coefficient for Significance ( T Test ) 
- **Null** Hypothesis ( H0 ) : There is **No Linear Relationship**
- **Alternate** Hypothesis ( H1 ) : There is a **Linear Relationship**
- P Value is Calculated ( if P Value > 0.05 : Then **Accept** Null Hypothesis else **Reject** Null Hypothesis )

### Multicollinearity
- Two or More Independent Features **Correlate** Strongly with each other.
- Regression Equation becomes **Unstable** and Create **Confusion**. 
- **Remove** One Feature to Prevent from **Multicollinearity** and make Regression **Stable**.
- **Tolerance** ( `T` ) = 1 - R<sup>2</sup> ( T < 0.1 | There is **Multicollinearity** ) 
- **Variance Inflation Factor** ( `VIF` ) = 1 / ( 1 - R<sup>2</sup> ) ( VIF > 10 | There is **Multicollinearity** )

### Causality
- Relationship between **Cause** and its **Effect**.
- One Variable **Affects** other Variable ( Temperature affect Icecream Sale | Sale of Icecream is more in Summer )

### 2. Remove Noise 
- Remove **Outliers** 

### 3. Remove Collinearity
- If Independent Features are **Highly** Correlated, Linear Regression will **Overfit** your Data.
- Pairwise Correlations for Independent Features and Remove the Correlated.

### 4. Gaussian Distributions
- More Reliable Predictions.
- Using **Transform** makes Data more Gaussian.

### 5. Rescale Independent Features
- **Rescale** Independent Features for more **Reliable** Predictions use **Standardization** or **Normalization**.

### 6. Residuals 

![R](Image/R.png)

- The Difference between **Predicted Value** from the **Actual Value**.
- Check the **Residual** | **Error** of the Regression Line.

![Residual](Image/Residual.png)

- Should be as low as Possible ( Complete Removal of Error is Impossible )

![Difference](Image/Difference.png)

- **Positive** Residual : Actual Value is **above** the Regression Line.
- **Negative** Residual : Actual Value is **below** the Regression Line.

![Positive Negative](Image/PN.png)

### Extraploation

- Making **Predictions** outside **Range** of Data.

![Extrapolation](Image/Extrapolation.png)

![Summary](Image/Summary.png)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
