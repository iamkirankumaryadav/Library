<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Linear Regression 📈

<h3><a href='#linreg'>Linear Regression</a> | <a href='#simple'>Simple Linear</a> | <a href='multiple'>Multiple Linear</a> | <a href='#ols'>Ordinary Least Square</a> | <a href='#gd'>Gradient Descent</a> | <a href='#ass'>Assumptions</a></h3>

### Regression

- A **statistical** process for **estimating** the **relationships** between **independent variables** and **dependent variable** to make **predictions**.

### Linear Regression 

- **Target** variable is **continuous numeric** values.
- The **best fit line** which gives **least** number of **errors** ( Difference between **actual** and **predicted** value ) for given **data points**.
- Find the **slope** ( Steepness of the line | Angular motion ) and **intercept** ( Position of line | Upward & downward ) with least **residual**. 
- **Sensitive** to `overfitting` ( But can be prevented using **Dimensionality Reduction**, **Regularization** and **Cross Validation** )

![Regression Line](Image/RegressionLine.png)

- **Learning** a linear regression model means estimating the values of the **coefficient** ( `Slope` : `m` and `Intercept` : `c` )
- **Predict** dependent variable based on one or more independent variables.
- **Measure** the influence of one or more independent variable on dependent variable.
- **Predict** the value of a **feature** based on the value of another feature.
- The parameters `m` and `c` are **learnt** by the **algorithm** based on the **data point** pairs of ( x, y )
- There are few **statistical** <a href="#ass">assumptions</a> as well for **linear regression**. 
- Also there are ways to **evaluate** how **good** our **model** learnt from the **data**, using **RMSE** and **R**<sup>2</sup>.

`Y` = `B1` * `X`  + `B0` 

`y` = `m` * `x` + `c` ( m and c are also called as coefficients )

![Equation Line](Image/EquationLine.png)

### B1 | m : Slope 

- **Gradient** | **Steepness** in Line | **Direction** of Line | **Weight**
- Indicates how much the **dependent variable** changes, if an **independent variable**  changes by **one unit**.

![Positive Slope](Image/Positive.png)

![Negative Slope](Image/Negative.png)

### B0 | c : Intercept 

- Bias | Constant | The place where **regression line** intersects the Y axis ( Value of Y when value of X and value of **coefficients** = 0 )

### R<sup>2</sup> : Coefficient of Determination | Goodness of Fit

- **Explains** the **variance** of the data captured by the model ( **0.7** to **0.9** is good value for R<sup>2</sup> ) 
- If R<sup>2</sup> is 0.8 or 80% i.e. regression line explaines 80% of **variance** in data | 80% of prediction is based on the **available** data.
- Larger R<sup>2</sup> indicates a **better fit** ( The model can explain the **variation** of **predictions** with actual in much better way )
- R<sup>2</sup> = 1 corresponds to SSR = 0 ( **Perfect fit** ) 
- Low R<sup>2</sup> causes **underfitting**
- High R<sup>2</sup> results into **overfitting**
- It shows that regression line | **Best fit line** predicts better than **base fit line** ( **Mean** ) 

### [Residuals](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md) | Error ( e )

- **Actual** - **Prediction**

<h3 name='simple'>Simple Linear Regression</h3>

- Only one **independent features** and one **dependent variable** ( **Continuous Numeric** )
- Use **statistics** to estimate **coefficients** ( `Slope` and `Intercept` )

<h3 name='multiple'>Multiple Linear Regression</h3>

- More than one **independent features** and only One **dependent variable** ( **Continuous Numeric** )
- Consider **features** that have **good correlation** with **dependent variable**.
- Checking **multicollinearity** is important.

### Polynomial Regression

- Finding **best fit curve**.

### Logistic Regression

- Dependent variable is **categorical**, used for **classification**. 
- **Probability** of **occurence** of **target label** is predicted on the basis of **threshold** ( `0.5` )
- **Range** value of **prediction** lies between `0` to `1` ( **Binary** classification )

### LASSO
- Use **shrinkage** ( Exactly 0 ), Good for **multicollinearity**.
- Completely eliminates the features.

### Ridge Regression
- Good for data with **noise** and **multicollinearity**.
- Try to learn the complicated model.

### Stepwise Regression
- More advance technique, Uses tests to remove **predictors**, can handle **large number** of **independent variables**.

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

<h3 name='ass'>Assumptions</h3>
  
- **Linearity** : There should be **Linear Relationship** between **Dependent Variable** and **Independent Variables**
- **Independence** : **Residuals** | **Errors** should be **Independent** of each other.
- **Normality** : **Errors** | **Residuals** of the **Data** should be **Normally Distributed** ( P Value > 0.05  )
- There should be Minimal **Multicollinearity** between **Independent Variables**.
- Quantile Quantile Point : **Data Points** should be **Close** to **Line**.
- **Homoscedasticity** : **Variance** around the **Regression Line** should be **Same** for all values of the **Independent Variable**.

![Error Normal Distribution](Image/ErrorDistribution.png)

- **Homoscedasticity** : **Variance** along the Line of **Best Fit** should remain **Constant** as we move along the line.
- Error Term in the Regression Model is **Constant**.
- **Variance** is Same for all **Data Points**.

![Homoscedasticity](Image/Homo.png)

- **Multicollinearity** : Two or more **Independent** Variables **Correlate** strongly with each other. 
- e.g. Experience vs Salary, Height vs Weight, Age of Car vs Car Price.
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
