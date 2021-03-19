# Regularization

- Adding **Bias** during Training
- Prevent Overfitting
- Simplify Models ( Simple Models avoids **Overfitting**, but may lead to **Underfitting**, So some Tradeoff is Important )
- Reducing the **Steepness** of the Slope. 
- Shrink the Coefficient (Slope) towards Zero.
- Add Penalty to the Loss Term | Sum ( Actual - Prediction ) <sup>2</sup> | **Sum of Squared Residuals**
- Encourages Weight Values towards 0 ( But not Exactly 0 )
- Penalize Weights that are too Large ( Learning Rate )
- It Improves the **Generalization** Performance ( Performance on New Unseen Data )

LASSO | RIDGE
:---  | :---
L1 | L2
Loss + \| Slope \| | Loss + \( Slope \) <sup>2</sup>
**Eliminate** Features | **Reduce** Impact of Features
 

Loss Function | Cost Function ( Quantifies Error between Predicted Values and Expected Values )

- Bias Increases with Increase in Lambda.
- Variance Increases with Decrease in Lambda.
- If **Lambda** Value is **High** | Model will be **Simple** | **Underfitting** | **High Bias** | Model will not Learn Enough about Training Data.
- If **Lambda** Value is **Low** | Model will be **Complex** | **Overfitting** | **High Variance** | Model will Learn too much about Training Data.


Ideal Value of Lambda produces Model that Generalizes Well on New Unseen Data, Ideal Value of Lambda is Data Dependent, so need some Tuning.  

# Lasso ( L1 ) | Slope | :
- Loss Function ( Sum of Squared Error ) + lambda * | Slope |
- LASSO ( Least Absolute Shrinkage and Selection Operator ) | Add Absolute Sum of Coefficient to Cost Function,
- Lasso tends to make Coefficients to Absolute Zeros which Reduces Features.
- Lasso Encourages Simple Sparse Model ( Model with Few Parameters )
- Lasso Removes Variable if there is Multicollinearity ( Lasso Eliminates the Coefficient ( Variable ) )

# Ridge ( L2 ) ( Slope ) <sup>2</sup> :
- Loss Function ( Sum of Squared Error ) + lambda * Square ( Slope )
- Ridge decreases | Minimizes the Complexity of Model 
- But does not Reduce Number of Variables ( Do not Remove any Irrelevant Feature ). 
- Ridge Never Sets the Value of Coefficient to Absolute Zero.
- Analyze Data that Suffers from Multicollinearity.
- Performs L2 Regularization.

# Elastic Net :
- Elastic Net combines L1 and L2 and does not Eliminates Highly Colliner Coefficient ( Slope )

- Learning Parameter means an Iterative Process that Updates Slope and Intercept at every Step by reducing the Loss | Cost Function ( Distances between Predictions and Actual Value ) as much as possible.

- Main Aim is to Minimize the Loss. 
