<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Regularization

Similar Terms:
Coefficient or weights means slope and intercept.

- Regularization is a technique used to prevent `overfitting`.
- Overfitting occurs when a model learns the training data too well and is unable to generalize the new unseen data.
- Regularization adds a penalty to the loss function that simplifies the model.
- It encourage the model to have smaller coefficients and will prevent from overfitting the training data.
- Adds `bias` to training data to reduce or balance the `variance`, this prevents from [overfitting](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Overfitting.md).
- **Simplify** complicated models ( Simple models avoids `overfitting`, but may lead to `underfitting`, so some `tradeoff` is important )
- Reducing the **steepness** of the slope | Shrink or encourage the `slope` towards `0`.
- Add **penalty** to the **loss term** | Sum ( Actual - Prediction ) <sup>2</sup> | **Sum of Squared Residuals**.
- `Penalize` weights that are too large ( Learning Rate | `Lambda` )
- Improves `generalization` ( Performance on new unseen data )
- High `lambda` | High `bias` | `Underfitting` | `Simple` model | More error in train set.
- Low `Lambda` | High `variance` | `Overfitting` | `Complicated` model | Not **generalize** well for **new unseen data**.
- `LASSO` | `L1` regularization adds a penalty equal to the sum of `absolute` value of `slope`
- `LASSO` reduces **coefficients** exactly to `0` ( **Eliminate feature** )
- `Ridge` | `L2` regularization adds a penalty equal to the sum of `squared` value of `slope`
- `Ridge` reduces **coefficients** to **small value** near 0 ( Not exactly zero | No elimination )

LASSO | Ridge | Elastic
:--- | :--- | :---
Least absolute shrinkage selection operator \| `L1` | Mountain Ridges \| `L2` | Between `L1` and `L2` 
Loss + lambda * \| slope \| | Loss + lambda * slope <sup>2</sup> | Loss + lambda1 * \| slope \| + lambda2 * slope<sup>2</sup>
**Mean absolute deviation** \| `x` - `mean` \| / `N` | **Std deviation** ( `x` - `mean` ) <sup>2</sup> / `n` |
Sum of `absolute` of slope | Sum of `squared` of slope | Mix of `absolute` and `square`
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
- It can **remove** features completely ( Setting coefficients to `0` | LASSO ) and reduce the complexity.
- In **ridge** first the independent variables are **standardized** ( Same scale ) then **ridge regression** is performed.

> Loss = Sum of square **residual** ( actual - prediction ) <sup>2</sup>

### `loss function` 

- A function that measures the difference between the predicted output of a model and the actual output.
- The loss function is used to guide the learning process of the model.
- The goal of the model is to minimize the loss function, the model tries to make its predictions closer to the actual output.
- Regression: Mean Squared Error Loss Function.
- Classification: Cross Entrophy Loss Function.
- The loss function helps us to understand the model's predictions and using this information we can improve the model.
- We can use regularization to prevent the model from overfitting the training data.
- By minimizing the loss function, we can improve the accuracy of the model.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
