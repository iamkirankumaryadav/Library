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
