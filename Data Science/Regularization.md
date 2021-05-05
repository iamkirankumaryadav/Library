<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Regularization

- **Biasing** Data towards particular `Small Values` near `Zero`. 
- **Biasing** is Achieved by Adding a **Tuning Parameter** to encourage those Values.
- Adding **Bias** to Training Data to `Reduce` | `Balance` **Variance**, Prevent from [Overfitting](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Overfitting.md).
- **Simplify** Complicated Models ( Simple Models avoids **Overfitting**, but may lead to **Underfitting**, So some **Tradeoff** is Important )
- Reducing the **Steepness** of the Slope | **Shrink** the Coefficient ( `Slope` ) towards `Zero`.
- Add **Penalty** to the **Loss Term** | Sum ( Actual - Prediction ) <sup>2</sup> | **Sum of Squared Residuals**.
- Encourages **Coefficient** | **Weight** towards `Zero` ( But not Exactly `Zero` )
- **Penalize** Weights that are too Large ( Learning Rate | `Lambda` )
- Improves **Generalization** Performance ( Performance on New Unseen Data )
- If Lambda is `High` | High `Bias` | Underfitting | `Simple` Model | More Error in Train Set.
- if Lambda is `Low` | High `Variance` | Overfitting | `Complicated` Model | Not **Generalize** well for **New Unseen Data**.
- `L1` Regularization add a `L1` Penalty equal to the `Absolute` Value of Magnitude of Coefficients | Weight | Slope.
- `L2` Regularization add a `L2` Penalty equal to the `Square` Value of Magnitude of Coefficients | Weight | Slope.
- `LASSO` reduces **Coefficients** to Exactly `Zero` ( **Feature Selection** )
- `Ridge` reduces **Coefficients** to **Small Value** near Zero ( Not Exactly Zero | No Elimination )

LASSO | Ridge | Elastic
:--- | :--- | :---
Least Absolute Shrinkage Selection Operator \| `L1` | Mountain Ridges \| `L2` | Between `L1` and `L2` 
Loss + lambda * \| slope \| | Loss + lambda * slope <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * slope<sup>2</sup>
**Mean Absolute Deviation** ( `x` - `mean` ) / `N` | **Std Deviation** ( `x` - `mean` ) <sup>2</sup> / `n` |
Sum of `Absolute` of Coefficient ( Weights ) | Sum of `Square` of Coefficients | Mix of `Absolute` and `Square`
Can lead Coefficient to **Exactly** `Zero` | **Minimize** Coefficient but not `Zero`
Feature **Selection** and Feature **Elimination** | Feature **Shrinkage**

Loss Function | Cost Function ( Quantifies Error between Predicted Values and Expected Values )

- `Bias` Increases with **Increase** in `Lambda` and `Variance` Increases with **Decrease** in Lambda.
- **Ideal** Value of `Lambda` produces Model that **Generalizes** Well on **New Unseen Data** ( `Low Bias` and `Low Variance` )

# Elastic Net :
- Elastic Net combines `L1` and `L2` and does not **Eliminates** Highly Collinear Coefficient ( Slope )
- `Learning Rate` | Parameter means an **Iterative** Process, Aim is to **Minimize** the `Loss`. 
- Updates `Slope` and `Intercept` at every Step by reducing the **Loss** | **Cost Function** as much as possible.

### Regularization Improves Regression
- Consider we Fit Regression Model on `100` Features | If we Train Model with `100` Features.
- Each Coefficient will `Memorize` each **Observations** ( Learn `Pattern` including **Noise** )
- The Model would have Perfect `Accuracy` on the `Train` Set but it will not `Generalize` well on `Test` Data ( New Unseen Data )
- **Regularization** can Prevent **Overfitting** by Artificially Penalizing Model **Coefficient** ( `Slope` | `Weight` )
- It can **Discourage** `Large` Coefficients and **Encourage** `Small` Coefficients.
- It can **Remove** Features Completely ( Setting Coefficients to `0` | LASSO )
- In **Ridge** First the Independent Variables are **Standardized** ( Same Scale ) then **Ridge Regression** is Performed.

> Loss = Sum of Square **Residual** ( Actual - Prediction ) <sup>2</sup> 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
