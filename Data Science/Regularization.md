<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Regularization
- Regularization is a technique used to prevent the ML model from **overfitting** and improve the generalization.
- Overfitting occurs when a model learns the training data too well including its noise and outlier.
- Regularization adds a penalty to the model for being too complex (e.g., having large weights or too many features).
- Adding a penalty to the loss function which encourages the model to stay simple and generalize better.
- It encourages the model to have smaller coefficients and prevents overfitting the training data.
- Reduces the **steepness** of the slope | Shrink or discourage the slope towards 0.
- High lambda | High bias | Underfitting | Simple Model | More error in train set.
- Low Lambda | High variance | Overfitting | Complicated Model | Not generalize well for **new unseen data**.
- LASSO (L1) regularization adds a penalty equal to the sum of the absolute value of the slope (weight).
- LASSO discourage **coefficients** exactly to 0 (Eliminate the irrelevant features from the model)
- Ridge (L2) regularization adds a penalty equal to the sum of the squared value of the slope (weight).
- Ridge discourage **coefficients** towards 0 (Not exactly zero | Does not eliminate entirely)

**Regularization and Cross-Validation, a good options if we have a limited amount of data**

**LASSO** | **Ridge** 
:--- | :--- 
Least absolute shrinkage selection operator (L1) | Mountain Ridges (L2) 
Loss + lambda * \| slope \| | Loss + lambda * slope <sup>2</sup> 
**Mean absolute deviation** \| x - mean \| / N | **Std deviation** (x - mean) <sup>2</sup> / n 
The sum of the absolute value of the slope | Sum of the squared value of the slope 
Can lead coefficient to **exactly** 0 | **Minimize** coefficient towards 0 without elimination
**Manhattan** distance (Sum of all path) | **Euclidean** distance (Shortest path)

### Lambda
- The **bias** increases with an increase in **lambda** value.
- The **variance** increases with a decrease in the **lambda** value.

### Regularization improves regression
- Consider we fit the regression model on 100 features | If we train the model with 100 features.
- Each coefficient will memorize each **observation** (Instead of learning pattern including noise)
- The model would have perfect accuracy on the train set but it will not generalize well on test data.
- It can **discourage** large coefficients which plays the dominating role.
- It can **remove** features completely (Setting coefficients to 0 | LASSO) and reduce the complexity.
- In ridge first the independent variables are **standardized** then **ridge regression** is performed.

> Loss = Sum of squared **residuals** (actual - prediction) <sup>2</sup>

### Loss function
- A function that measures the difference between the predicted output of a model and the actual output.
- The loss function is used to guide the learning process of the model during training and testing.
- The goal of the model is to minimize the loss function, the model tries to make its predictions closer to the actual output.
- Regression: Mean Squared Error Loss Function | Classification: Cross Entropy Loss Function
- The loss function helps us to understand the model's predictions and improve the model's accuracy.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

