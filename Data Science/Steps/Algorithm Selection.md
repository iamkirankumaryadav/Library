<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Algorithm Selection

### Why linear regressions is flawed ?
- Simple linear regression model fit a **straight line** ( **Hyperplane** for muliple variables ) 
- Easy to **interpret** and **understand**. 
- Prone to **overfitting** with many features and cannot express non linear relationship.

### Regularization can improve regression
- If we a fit regression model on 100 features ( Training )
- Each coefficient will memorize each observation ( Learn pattern including **noise** )
- The model would have **perfect accuracy** on the training data. 
- But it will not generalize well on test data ( New unseen data )
- Regularization can prevent **overfitting** by artificially penalizing model coefficients | slopes.
- It can **discourage** large coefficients and **encourage** small coefficients.
- It can **remove** features completely ( Setting coefficients | slopes to `0` )

Loss = Sum of **Residual** ( Actual - Prediction ) <sup>2</sup> 

LASSO ( `L1` ) | Ridge ( `L2` ) | Elastic ( `L1` + `L2` )
:--- | :--- | :---
Least absolute shrinkage selection operator | Mountain ridges | Between LASSO and Ridge  
Loss + lambda * \| slope \| | Loss + lambda *  ( slope ) <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * ( slope ) <sup>2</sup>
`Absolute` of coefficient | `Square` of coefficients | Mix of `absolute` and `square`
Can lead coefficient to exactly 0 | Lead to small coefficient but not 0 | No 0
Feature **selection** and feature **elimination** | Feature **shrinkage**

### Decision Trees
- Single decision tree is usually prone to **overfit** with many inputs.

In ensemble techniques **base models** are **decision trees**

Bagging | Boosting
Reduce chance of `Overfitting` | Improve the `prediction` and `classification` of model
Trains large number of `individiual` learners in `parallel` | Trains a large number of `weak` learners in `sequence`
Uses `complex base models` and tries to `simplify` their predictions | Uses `simple base models` and tries to `improve`
each `tree` is `random` subset of features ( **feature selection** ) and observations ( **resmapling** ) | Each tree in the `sequence` tries to `correct` the prediction errors of the previous tree 
Don't have many complicated parameters to tune | More complicated to tune

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
