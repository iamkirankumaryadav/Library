# Linear Regression

**Learning** a Linear Regression Model means Estimating the Values of the **Coefficient** 

### Y = X * B1 + B0

**B1** : Slope | Gradient | Steepness in Line 

**B0** : Intercept | Bias | Constant

### Simple Linear Regression
- Single Input | Independent Feature 
- Use Statistics to Estimate Coefficients
- Mean | Median | Standard Deviations | Correlation and Covariance

### Ordinary Least Squares (OLS)
- More than One Independent Features
- Minimize the Sum of Squared Residuals | Errors 
- Sum(Square(Distance between the Actual Data Point and the Predicted Point (Regression Line)))
- Treat Data as Matrix
- Use Linear Algebra to Estimate | Predict the Optimal Value for the Coefficients.

### Gradient Descent
- A Process of Optimizing the Values of the Coefficients by Iteratively Minimizing the **Error** of Model on Training Data.
- Starts with Random Values for each Coefficient
- Sum of Squared Errors (**SSE**) are Calculated for each Pair of Independent and Dependent Values.
- **Learning Rate** is used as a Scale and the coefficients are updated in the direction towards minimizing the Error.
- The Process is Repeated until a minimum SSE is Achieved or no further improvement is possible.
- Learning Rate (alpha) Parameters that determines the size of Improvement Step on each Iteration.

### Regularization
- Seek to Minimize SSE of the Model on Training Data 
- Reduce **Complexity** of Model (**Overfitting**)
- Add some Bias on Training Data for Decreasing Variance on Test Data 

1. **LASSO** (L1) : OLS is modified to minimize the **Absolute** Sum of Coefficients : Cost Function + (Lambda) * |Slope|
2. **Ridge** (L2) : OLS is modified to minimize the **Squared** Sum of Coefficients : Cost Function + (Lambda) * Square(Slope)

Used when there is Collinearity (One Independent Feature can completely Describe Other Independent Feature) in Data 

# Preparing Data for Linear Regression

### 1. Linear Assumptions
- Assume that the Relationship between Independent and Dependent Features is **Linear**.
- You may need to **Transform** Data to make the Relationship **Linear**.

