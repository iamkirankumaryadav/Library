<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Regularization

- Adding **Bias** to Training Data to Reduce | Balance **Variance**, Prevent from **Overfitting**.
- **Simplify** Complicated Models ( Simple Models avoids **Overfitting**, but may lead to **Underfitting**, So some **Tradeoff** is Important )
- Reducing the **Steepness** of the Slope | **Shrink** the Coefficient ( `Slope` ) towards `Zero`.
- Add **Penalty** to the **Loss Term** | Sum ( Actual - Prediction ) <sup>2</sup> | **Sum of Squared Residuals**.
- Encourages **Coefficient** | **Weight** towards `Zero` ( But not Exactly `Zero` )
- **Penalize** Weights that are too Large ( Learning Rate | `Lambda` )
- Improves **Generalization** Performance ( Performance on New Unseen Data )
- If Lambda is very High | High Bias | Underfitting | Model not Trained well | More Error in Training Set.
- if Lambda is very Low | High Variance | Overfitting | Model will not **Generalize** Well on New Unseen Data. 

LASSO | Ridge | Elastic
:--- | :--- | :---
Least Absolute Shrinkage and Selection Operator ( L1 ) | Mountain Ridges ( L2 ) | Between L1 and L2 
Loss + lambda * \| slope \| | Loss + lambda * slope <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * slope<sup>2</sup>
Sum of `Absolute` of Coefficient ( Weights ) | Sum of `Squared` of Coefficients | Mix of `Absolute` and `Square`
Can lead Coefficient to **Exactly** `Zero` | **Minimize** Coefficient but not `Zero`
Feature **Selection** and Feature **Elimination** | Feature **Shrinkage**

Loss Function | Cost Function ( Quantifies Error between Predicted Values and Expected Values )

- **Bias** Increases with **Increase** in Lambda.
- **Variance** Increases with **Decrease** in Lambda.
- If **Lambda** Value is **High** | Model will be **Simple** | **Underfitting** | **High Bias** | Model will not Learn Enough about Training Data.
- If **Lambda** Value is **Low** | Model will be **Complex** | **Overfitting** | **High Variance** | Model will Learn too much about Training Data.
- Ideal Value of Lambda produces Model that **Generalizes** Well on **New Unseen Data**.

# Elastic Net :
- Elastic Net combines L1 and L2 and does not **Eliminates** Highly Colliner Coefficient ( Slope )
- Learning Rate | Parameter means an **Iterative** Process. 
- Updates `Slope` and `Intercept` at every Step by reducing the **Loss** | **Cost Function** as much as possible.
- Aim is to **Minimize** the `Loss`. 

### Regularization Improves Regression
- Consider we Fit Regression Model on `100` Features | If we Train Model with `100` Features
- Each Coefficient will `Memorize` each Observations ( Learn Pattern including **Noise** )
- The Model would have Perfect `Accuracy` on the Training Data but it will not `Generalize` well on Test Data ( New Unseen Data )
- Regularization can Prevent **Overfitting** by Artificially Penalizing Model **Coefficient** ( Slopes )
- It can **Discourage** Large Coefficients and **Encourage** Small Coefficients.
- It can **Remove** Features Completely ( Setting Coefficients to 0 only if LASSO )
- In **Ridge** First the Independent Variables are **Standardized** ( Same Scale ) then **Ridge Regression** is Performed.

> Loss = Sum of Square **Residual** ( Actual - Prediction ) <sup>2</sup> 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
