# Regularization

- Adding **Bias** to Training Data to Balance **Variance**
- Prevent **Overfitting**
- **Simplify** Complicated Models ( Simple Models avoids **Overfitting**, but may lead to **Underfitting**, So some **Tradeoff** is Important )
- Reducing the **Steepness** of the Slope | **Shrink** the Coefficient ( Slope ) towards `Zero`
- Add **Penalty** to the Loss Term | Sum ( Actual - Prediction ) <sup>2</sup> | **Sum of Squared Residuals**
- Encourages Weight Values towards `Zero` ( But not Exactly `Zero` )
- Penalize Weights that are too Large ( Learning Rate )
- It Improves the **Generalization** Performance ( Performance on New Unseen Data )

LASSO | RIDGE
:---  | :---
L1 Regularization | L2 Regularization
Loss + \| Slope \| | Loss + \( Slope \) <sup>2</sup>
Absolute Sum of Coefficients | Square of Coefficient
**Eliminate** Features ( Multicollinearity ) | **Reduce** Impact of Features ( Never Set to Zero )
 

Loss Function | Cost Function ( Quantifies Error between Predicted Values and Expected Values )

- Bias Increases with Increase in Lambda.
- Variance Increases with Decrease in Lambda.
- If **Lambda** Value is **High** | Model will be **Simple** | **Underfitting** | **High Bias** | Model will not Learn Enough about Training Data.
- If **Lambda** Value is **Low** | Model will be **Complex** | **Overfitting** | **High Variance** | Model will Learn too much about Training Data.
- Ideal Value of Lambda produces Model that **Generalizes** Well on **New Unseen Data** 
- Ideal Value of Lambda dependents on Data, so need some Tuning.  

# Elastic Net :
- Elastic Net combines L1 and L2 and does not Eliminates Highly Colliner Coefficient ( Slope )
- Learning Parameter means an Iterative Process that Updates Slope and Intercept at every Step by reducing the Loss | Cost Function ( Distances between Predictions and Actual Value ) as much as possible.
- Main Aim is to Minimize the Loss. 

### Regularization can Improve Rgeression
- If we a Fit Regression Model on 100 Features ( Training )
- Each Coefficient will Memorize each Observations ( Learn Pattern including **Noise** )
- The Model would have Perfect Accuracy on the Training Data but it will not Generalize well on Test Data ( New Unseen Data )
- Regularization can Prevent **Overfitting** by Artificially Penalizing Model Coefficient
- It can **Discourage** Large Coefficients
- It can **Remove** Features Completely ( Setting Coefficients to 0 )
- It can **Encourage** Small Coefficients

> Loss = Sum of Square **Residual** ( Actual - Prediction ) <sup>2</sup> 

LASSO | Ridge | Elastic
:--- | :--- | :---
Least Absolute Shrinkage and Selection Operator ( L1 ) | Mountain Ridges ( L2 ) | Between L1 and L2 
Loss + lambda * \| slope \| | Loss + lambda * slope <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * slope<sup>2</sup>
`Absolute` of Coefficient | `Square` of Coefficients | Mix of `Absolute` and `Square`
Can lead Coefficient to Exactly Zero | Lead to Small Coefficient but not Zero | No Zero 
Feature **Selection** and Feature **Elimination** | Feature **Shrinkage**
