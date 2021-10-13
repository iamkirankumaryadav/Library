<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Regularization

- **Biasing** data towards particular `small values` near `0`. 
- **Biasing** is achieved by adding a **tuning parameter** to encourage those values.
- Adding `bias` to training data to reduce | balance `variance`, prevent from [overfitting](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Overfitting.md).
- **Simplify** complicated models ( Simple models avoids `overfitting`, but may lead to `underfitting`, so some `tradeoff` is important )
- Reducing the **steepness** of the slope | Shrink the coefficient ( `slope` ) towards `0`.
- Add **penalty** to the **loss term** | Sum ( Actual - Prediction ) <sup>2</sup> | **Sum of Squared Residuals**.
- Encourages **coefficient** | **Weight** towards `0` ( But not exactly `zero` )
- **Penalize** weights that are too large ( Learning Rate | `Lambda` )
- Improves **generalization** ( Performance on new unseen data )
- If lambda is `high` | High `bias` | Underfitting | `Simple` model | More error in train set.
- if Lambda is `low` | High `variance` | Overfitting | `Complicated` model | Not **generalize** well for **new unseen data**.
- `L1` regularization add a `L1` penalty equal to the `absolute` value of magnitude of `slope` | coefficients | weight.
- `L2` regularization add a `L2` penalty equal to the `squared` value of magnitude of `slope` | coefficients | weight.
- `LASSO` reduces **coefficients** exactly to `0` ( **Eliminate feature** )
- `Ridge` reduces **coefficients** to **small value** near 0 ( Not exactly zero | No elimination )

LASSO | Ridge | Elastic
:--- | :--- | :---
Least absolute shrinkage selection operator \| `L1` | Mountain Ridges \| `L2` | Between `L1` and `L2` 
Loss + lambda * \| slope \| | Loss + lambda * slope <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * slope<sup>2</sup>
**Mean absolute deviation** \| `x` - `mean` \| / `N` | **Std deviation** ( `x` - `mean` ) <sup>2</sup> / `n` |
Sum of `absolute` of coefficient ( Weights ) | Sum of `square` of coefficients | Mix of `absolute` and `square`
Can lead coefficient to **exactly** `0` | **Minimize** coefficient but not `0`
Feature **selection** and feature **elimination** | Feature **shrinkage**
**Manhattan** distance ( Sum of all path ) | **Euclidean** distance ( Shortest path )

Loss Function | Cost Function ( Quantifies error between predicted values and expected values )

- `Bias` increases with increase in `lambda` 
- `Variance` increases with decrease in `lambda`.
- **Ideal** value of `lambda` to produces model that **generalizes** the new unseen data well : `Low bias` and `low variance`

# Elastic Net :
- Elastic net combines `L1` and `L2` and does not **eliminates** highly collinear coefficient ( Slope )
- `Learning rate` | Parameter means an **iterative** process, aim is to **minimize** the `loss`. 
- Updates `slope` and `intercept` at every step by reducing the **loss** | **cost function** as much as possible.

### Regularization Improves Regression
- Consider we fit regression model on `100` features | If we train model with `100` features.
- Each coefficient will `memorize` each **observations** ( Learn `pattern` including **noise** )
- The model would have perfect `accuracy` on the `train` set but it will not `generalize` well on `test` data ( New unseen data )
- **Regularization** can prevent **overfitting** by artificially penalizing model **coefficient** ( `slope` | `weight` )
- It can **discourage** `large` coefficients which plays the dominating role.
- It can **remove** features completely ( Setting coefficients to `0` | LASSO )
- In **ridge** first the independent variables are **standardized** ( Same scale ) then **ridge regression** is performed.

> Loss = Sum of square **residual** ( actual - prediction ) <sup>2</sup> 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
