# Regularization

- Adding Bias during Training
- Prevent Overfitting
- Simplify Models (Simple Models avoids Overfitting, but may lead to Underfitting, So some Tradeoff is Important)
- Reducing the Steepness of the Slope. 
- Shrink the Coefficient (Slope) towards Zero.
- Add Penalty to the Loss Term Sum ( Actual - Prediction ) <sup>2</sup>
- Encourages Weight Values towards 0 (But not Exactly 0)
- Penalize Weights that are too Large (Learning Rate)
- It Improves the Generalization Performance (Performance on New, Unseen Data)

LASSO | RIDGE
 :---:  | :---:
 L1 | L2
 Loss + |Slope| | Loss + (Slope)<sup>2</sup>
 Eliminate Features | Reduce Impact of Features
 

Loss Function | Cost Function (Quantifies Error between Predicted Values and Expected Values)

- If Lambda Value is High | Model will be Simple | Underfitting | Bias will Increase | Model will not Learn Enough about Training Data.
- If Lambda Value is Low | Model will be Complex | Overfitting | Variance will Increase | Model will Learn too much about Training Data.
- Bias Increases with Increase in Lambda.
- Variance Increases with Decrease in Lambda.

Ideal Value of Lambda produces Model that Generalizes Well on New Unseen Data, Ideal Value of Lambda is Data Dependent, so need some Tuning.  

# Lasso (L1) |Slope| :
- Loss Function (Sum of Squared Error) + lambda * |Slope|
- LASSO (Least Absolute Shrinkage and Selection Operator) | Add Absolute Sum of Coefficient to Cost Function,
- Lasso tends to make Coefficients to Absolute Zeros which Reduces Features.
- Lasso Encourages Simple Sparse Model (Model with Few Parameters)
- Lasso Removes Variable if there is Multicollinearity (Lasso Eliminates the Coefficient(Variable))

# Ridge (L2) Square(Slope) :
- Loss Function (Sum of Squared Error) + lambda * Square(Slope)
- Ridge decreases | Minimizes the Complexity of Model 
- But does not Reduce Number of Variables (Do not Remove any Irrelevant Feature). 
- Ridge Never Sets the Value of Coefficient to Absolute Zero.
- Analyze Data that Suffers from Multicollinearity.
- Performs L2 Regularization.

# Elastic Net :
- Elastic Net combines L1 and L2 and does not Eliminates Highly Colliner Coefficient (Slope)

- Learning Parameter means an Iterative Process that Updates Slope and Intercept at every Step by reducing the Loss | Cost Function (Distances between Predictions and Actual Value) as much as possible.

- Main Aim is to Minimize the Loss. 

# How to Prevent Overfitting?

### 1. Cross Validation
- Use Initial Training Data to generate Multiple Mini Train Test Splits (Use Splits to Tune your Model)

#### Standard K Fold Cross Validation
- Partition the Data into K Subsets (Folds)
- Iteratively Train the Algorithm on (K-1) Folds.
- Using Remaining Fold as Test Set. 
- Allows Hyperparameter Tuning
- Keep test Set as Trulu Unseen Dataset.

### 2. Train with More Relevant Data

### 3. Remove Irrelevant Features and Duplicate Observations.

### 4. Early Stopping
   Up until Certain Iterations, New Iterations improve the Model.
   Model's Ability to Generalize can Weaken as it begins to Overfit Training Data.

### 5. Ensembling
- Combining Predictions from Multiple Seperate Models.

A.Bagging (Reduce Chance of Overfitting)
- Trains Large Number of Strong Learners in Parallel
- Select Majority | Mode

B.Boosting (Improve Flexibity of Simple Models)
- Trains Large Number of Weak Learners in Series | Sequence 
- Each One in Series Focuses on Learning from the Mistakes of Earlier.
- Combines All the Weak Learners into a Single Strong Learner.

# Standardization 

- Subtracting from Mean and Dividing by Standard Deviation.
