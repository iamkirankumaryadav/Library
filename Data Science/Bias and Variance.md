<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Bias | Variance | Underfitting | Overfitting

`Bias` | `Variance`
:--- | :---
Bias : Error on `train` set | Variance : Error on `test` set
`High` Bias ( Model is not trained well ) | `High` Variance ( Prediction is not good for new unseen data )
`High` Bias ( Simple Model is Created ) | `High` Cariance ( Complicated Model is Created )
`Low` Bias ( Model is trained well ) | `Low` Variance ( `Prediction` is `close` to `actual` )
Simple model make **simplified assumptions** while learning | Complicated model learn data with `noise`
Simple model do not capture **Hidden** Patterns and Relations properly | Model **Memorize** Patterns and Relations + Noise + Error
`Low` Bias Algorithms ( Decision Tree, KNN, SVM ) | `Low` Variance Algorithms ( Regression, LDA )
`High` Bias Algorithm ( Regression ) | `High` Variance Algorithm ( Decision Tree, KNN, SVM ) 

- `Error` = `Predicted` - `Actual` ( Difference between the `expected` value and `actual` value )
- `Linear` algorithms **learns fast** which often lead to `high bias`
- Simple the algorithm, more `bias` it will introduce ( Underfitting )

### How to Reduce `Bias` ?
- `K Fold Cross Validations` and `Resampling` | Split dataset into `K` samples and each set is used as testing set
- `Bootstrapping` and `Boosting` | Iteratively `Resampling` a dataset with `replacement`

### Bias Variance `Trade Off`

- `Bias` and `Variance` are `inversely` proportional to each other.
- Increasing `Bias` decreases `Variance` and Increasing `Variance` decreases `Bias`
- Find the **correct balance** : `Low Bias` and `Low Variance`

### `Underfitting` : High Bias + Low Variance ( `Simple` Model )
- `High Bias` : `High` error on `train` dataset
- `Low Variance` : `Low` error on `test` dataset ( **Genralized** )
- The model fails to `fit` the data well enough.

### `Overfitting` : Low Bias + High Variance ( `Complex` Model )
- `Low Bias` : `Low` error on `train` data ( Model is **trained** very well including `noise` )
- `High Variance` : `High` error on `test` data ( Performs bad on `new unseeen` data )
- When a massive amount of data trains a Machine Learning Model, it tends to learn from `noise` and inaccurate data.
- Random error and noise gets added | Complex model | Too many Parameters ( Columns ) relative to the number of observations ( Rows ) 
- Poor **predictive** performance | Do not **genralize** well on the **new unseen data**
- Difference between the prediction on the **new unseen data point** and the **actual data point** is `high` ( High Variance )
- Model tries to `fit` the training data so closely that it does not **generalize** well to **new unseen data**.

`Bias` and `Variance` helps us improve the data fitting | Training process resulting in more **accurate models**.

### Total Error = Bias + Variance + Irreducible Error ( Noise )

### Error due to `Bias `
- Difference between the **expected prediction** of our model and the **correct actual value** which we are trying to `predict`.
- Model fails to **capture** the **relation** between **features** and **target** properly.
- Due to **randomness** in dataset, `Bias` measures how far off these Model's **predictions** are from the **correct actual value**.

### Error dur to `Variance`
- **Variability** of a model **prediction** from an **actual data point**.
- How much the predictions for a given point vary between different Models.

### Good Fit Model ( Low Bias and Low Variance )
- `Prediction` is actually **close** to the `actual`.
- Generalized enough to work with any **new unseen data** ( Low Variance ) 
- **Captures** Less `noise` and `error` at the time of **training** ( Low Bias )

### How to Obtain Optimal Tradeoff
1. **Hyperparameter Tuning** : Choosing a set of `optimal` **hyperparameter** for training.
2. **Regularization** ( `L1` and `L2`) : Technique used to reduce `overfitting` by discouraging  complex models.
3. **Grid Search Cross Validation**.
4. **Bagging** : **Random Forest**.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
