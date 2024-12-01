<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# **Linear Regression** 📈

<h3><a href='#simple'>Simple Linear</a> | <a href='#multiple'>Multiple Linear</a> | <a href='#ass'>Assumptions</a></h3>

### **Regression**
- Estimating the relationships between the dependent variable and one or more independent variables to make predictions.

#### **Important Terms:**
- Independent Variables | Features Matrix (An array of numbers, one or more rows, one or more columns)
- Dependent Variable | Target Vector (A list of numbers, can be in a single row or column)

### **Linear Regression:**
- Predict a continuous numeric dependent variable based on one or more independent variables.
- Predict a best-fit line (finding a regression line that best fits the data) with the least errors or residuals.
- Residual | Error: Difference between the actual and predicted values for a given data point.
- Learning a linear regression model means estimating the values of the coefficients (Weight, slope and intercept)
- Linear regression is sensitive to over fittings and outliers.
- But can be prevented using [dimensionality reduction](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Unsupervised%20Learning/Dimensionality%20Reduction.md), [regularization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md), [standardization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md) and [cross validation](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Cross%20Validation.md)

![Regression Line](Image/RegressionLine.png)

- Linear regression predicts a target vector's value based on the feature matrix's value.
- The parameters **m** and **c** are **learnt** by the **algorithm** based on the **data point** pairs of (x, y)
- There are few **statistical** <a href="#ass">assumptions</a> as well for **linear regression**. 
- Also there are few [metrics](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Regression%20Metrics.md) to **evaluate** how **good** our **model** learnt from the **data**.
- **y = m * x + c** (m and c are also called as regression coefficients)

![Equation Line](Image/EquationLine.png)

### **m | Slope | Gradient | Steepness | Direction | Weight | Coefficient (of a line)**
- Indicates how much the dependent variable will change if an independent variable changes by one unit.

![Positive Slope](Image/Positive.png)

![Negative Slope](Image/Negative.png)

### **How do we check the relationships between independent and dependent variables?**

Data visualization is one of the best ways to check the relationship, distribution and variance in the dataset.

1. **Scatter Plots:**  
- Plot the independent variable(s) on the x-axis and the dependent variable on the y-axis.
- The pattern of the data points can reveal the direction and strength of the relationship.
- A positive slope suggests a positive relationship (as x increases, y increases)
- A negative slope suggests a negative relationship (as x increases, y decreases)
- A random scatter plot suggests a non-linear relationship.

2. **Correlation Coefficient (r):** 
- The strength and direction of the linear relationship between independent and dependent variables.
- It ranges from -1 (perfect negative correlation) to +1 (perfect positive correlation), with 0 indicating no linear correlation.

3. **Regression Analysis:**
- By fitting a model to your data, you can estimate the effect of changes in the independent variable(s) on the dependent variable.
- The model's coefficients (how much the dependent variable changes on the unit change of an independent variable)

4. **Residual Analysis:** 
- The difference between the actual and predicted values of the dependent variable can reveal potential issues with the model.
- Randomly scattered residuals suggest a good fit, while patterns in the residuals indicate potential problems like non-linearity or outliers.

5. **R_squared | Adjusted R_Squared:**
- Training the model with different feature subsets and evaluating their performance on a validation set.
- The subset with the best performance is chosen.

### **c | Intercept | Bias | Constant | Coefficient**
- The point where the regression line intersects the Y-axis. 
- Value of Y when the value of X and value of coefficients = 0.

### [Residuals](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md) | Error | e | Noise | Actual - Prediction

<h3 name='simple'>Simple Linear Regression</h3>

- Only one **independent variable** and one **dependent variable** (**Continuous Numeric**)
- Use **statistics** to estimate the **coefficients** i.e. slope (m) and intercept (c).

<h3 name='multiple'>Multiple Linear Regression</h3>

- More than one **independent variables** and only one **dependent variable** (**Continuous Numeric**)
- Consider **features** that have **good correlation** with the **dependent variable** (**no multicollinearity**).
- **Multicollinearity:** One independent feature can completely describe the other independent feature.

# **Preparing Data for Linear Regression**

<h3 name='ass'>Assumptions</h3>
  
- **Linearity:** The relationship between the independent variable (x) and the dependent variable (y) is linear.
- **Independence:** The data points should be independent.
- **Normality:** The errors/residuals of the data points should be normally distributed.
- **No Multicollinearity:** The independent variables should not be highly correlated.
- **Homoscedasticity:** The variance of the regression line should remain **constant** throughout.
- **Quantile Quantile Point:** Data points should be close to the regression line.

![Error Normal Distribution](Image/ErrorDistribution.png)

![Homoscedasticity](Image/Homo.png)

### **Covariance: Direction**

![Covariance](Image/Covariance.png) 

- Covariance measures how much two variables change together (Direction of the linear relationship)
- **Positive Covariance:** Two variables tend to move in the same direction.
- **Negative Covariance:** Two variables tend to move in opposite directions.

### **Correlation: Strength and Direction**

- Correlation is a standardized version of covariance, that measures the strength and direction of a linear relationship.
- Measure how closely two variables are related to each other and one variable can predict the other variable.
- Varies between -1 (Perfect Negative Correlation) to +1 (Perfect Positive Correlation)

**Amount of R** | **Strength of Correlation**
:--- | :---
0.0  | **No** Correlation
0.1 - 0.3 | **Little** Correlation
0.3 - 0.5 | **Medium** Correlation
0.5 - 0.7 | **High** Correlation
0.7 - 1.0 | **Very High** Correlation

![Perfect Linear Correlation](Image/Perfect.png)

![Strength of Slope](Image/Strength.png)

### **Difference between Covariance and Correlation**

- Covariance reveals how two variables change together only to their direction.
- Correlation determines how closely two variables are related to each other (Strength & Direction)
- Both covariance and correlation measure the relationship and the dependency between two variables.
- Unlike Covariance, Correlation values are standardized.

### **Variance Inflation Factor (VIF)**

- A measure of how much the variance of the regression coefficient is inflated due to collinearity between the independent variables.
- **VIF = 1** indicates that there is no collinearity between the independent variables.
- **VIF > 10** indicates that there is high collinearity between the independent variables.
- We should consider removing the independent variable to reduce the VIF.
- VIF does not tell us which independent variable should be removed.
- VIF can be higher due to more independent features and features with high scales or different scales.
<p><code>VIF = 1 / 1 - R<sup>2</sup></code></p>

### **T-Test: Correlation coefficient for significance**

Correlation Coefficient | Relationship
:--- | :---
0 | No Correlation between two variables
1 | Perfect Positive Correlation (Directly Proportional)
-1 | Perfect Negative Correlation (Indirectly Proportional)

- Compare the mean of two separate groups to observe the significant difference between them.
- Measure of the strength and direction of the relationship between two variables.
- **Null Hypothesis (H0):** There is no difference in the mean.
- **Alternate Hypothesis (H1):** There is a difference in the mean.
- P value is calculated, if the P-Value > 0.05, then the Null Hypothesis (H0) is accepted.
- **One sample t-test:** This compares the mean of one group to a specific hypothesized value.
- **Two sample t-test:** This compares the means of two independent groups.
- Assumptions: The data is normally distributed and the variances of the two groups are similar.

Significance Level | P-value
:--- | :---
95% | 0.05
99% | 0.01
99.9% | 0.1

### **Multicollinearity**
- Generally occurs when there is a high correlation between two or more independent variables.
- One independent variable can be used to predict the other. This creates redundant information.
- Regression equation becomes **unstable** and create **confusion**.
- Observations (Rows) and features (Columns) should be **independent**.
- **Remove** one feature to prevent from **multicollinearity** and make regression **stable**.
- e.g. Experience vs Salary, Height vs Weight, Age of Car vs Car Price.   
- Tolerance | T = 1 - R<sup>2</sup> (T < 0.1 | There is **multicollinearity**) 
- Variance Inflation Factor | VIF = 1 / (1 - R<sup>2</sup>) (VIF > 10 | There is **multicollinearity**)

### **Causality**
- Relationship between **cause** and its **effect**.
- One variable **affects** another variable (Temperature affects ice cream sale | Sale of ice cream is more in summer)

### **Rescale Independent Features**
- Rescale-independent features for more reliable predictions use standardization or normalization.

### **Residual | Error**

![R](Image/R.png)

- The difference between the predicted value and the actual value.

![Residual](Image/Residual.png)

- Error should be as low as possible (Complete removal of error is impossible)

![Difference](Image/Difference.png)

- **Positive Residual:** The actual value is above the regression line.
- **Negative Residual:** The actual value is below the regression line.

![Positive Negative](Image/PN.png)

### Extrapolation

- Making predictions outside the range of data due to the presence of outliers.

![Extrapolation](Image/Extrapolation.png)

![Summary](Image/Summary.png)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
