# Algorithm Selection

### Why Linear Regressions is Flawed ?
- Simple Linear Regression Model fit a **Straight Line** ( **Hyperplane** for Muliple Variables ) 
- Easy to Interpret and Understand
- Prone to Overfitting with many Features and cannot Express Non Linear Relationship

### Regularization can Improve Rgeression
- If we a Fit Regression Model on 100 Features ( Training )
- Each Coefficient will Memorize each Observations ( Learn Pattern including **Noise** )
- The Model would have Perfect Accuracy on the Training Data 
- But it will not Generalize well on Test Data ( New Unseen Data )
- Regularization can Prevent **Overfitting** by Artificially Penalizing Model Coefficient
- It can Discourage Large Coefficients
- It can Remove Features Completely ( Setting Coefficients to 0 )
- It can Encourage Small Coefficients

LASSO | Ridge | Elastic
:--- | :--- | :---
Least Absolute Shrinkage and Selection Operator ( L1 ) | Mountain Ridges ( L2 ) | Between L1 and L2 
Loss + lambda * \| slope \| | Loss + lambda * slope <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * slope<sup>2</sup>
`Absolute` of Coefficient | `Square` of Coefficients | Mix of `Absolute` and `Square`
Can lead Coefficient to Exactly Zero | Lead to Small Coefficient but not Zero | No Zero 
Feature Selection and Feature Elimination | Feature Shrinkage


### Decision Trees
- Prone to **Overfit** with many inputs
- Cannot express **Non Linear Relationship** easily

> **Base Models** are **Decision Trees**

Bagging | Boosting
:--- | :---
Reduce Chance of **Overfitting** | Improve the **Predictive Fexibility** of Simple Model
Trains Large Number of `Strong` Learners in `Parallel` | Trains a Large number of `Weak` Learners in `Sequence`
Combines all Strong Learners for Predictions | Combines **Weak** Learner into **One Strong Learner** 
Uses `Complex Base Models` and tries to `Smooth out` their Predictions | Uses `Simple Base Models` and tries to `Boost` their Aggregate complexity
Each `Tree` is `Random` Subset of Features ( **Feature Selection** ) and Observations ( **Resmapling** ) | Each Tree in the `Sequence` tries to `Correct` the Prediction Errors of the Previous Tree 
Don't have many Complicated Parameters to Tune | More Complicated to Tune
