<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Bias | Variance | Underfitting | Overfitting

`Bias` | `Variance`
:--- | :---
Bias : Error on `train` set | Variance : Error on `test` set
`High Bias` ( Model is not trained well ) | `High Variance` ( Prediction is not good for new unseen data )
`High Bias` ( Creates simple model ) | `High Variance` ( Creates complicated model )
Simple model make `simplified assumptions` while learning | Complicated model learn data with `noise`
Simple model do not capture **hidden** patterns and relations properly | Model **memorize** patterns and relations + noise + error
`Low Bias` algorithms ( Decision Tree, KNN, SVM ) | `Low Variance` algorithms ( Regression, LDA )
`High Bias` algorithm ( Regression ) | `High Variance` algorithms ( Decision Tree, KNN, SVM ) 

- `Error` = `Predicted` - `Actual` ( Difference between the `expected` value and `actual` value )
- `Linear` algorithms **learns fast** which often lead to `high bias`
- Simple the algorithm, more `bias` it will introduce ( Underfitting )

### How to Reduce `Bias` ?
- Cross validation, resampling and ensemble techniques can prevet from Bias as well as Variance.
- `K Fold Cross Validations` and `Resampling` | Split dataset into `K` samples and each set is used as testing set.
- `Bootstrapping` and `Boosting` | Iteratively `Resampling` a dataset with `replacement`

### Bias Variance `Trade Off`

- `Bias` and `Variance` are `inversely` proportional to each other.
- Increasing `Bias` decreases `Variance` and Increasing `Variance` decreases `Bias`
- Find the **correct balance** : `Low Bias` and `Low Variance`

### `Underfitting` : High Bias + Low Variance ( `Simple` Model )
- `High Bias` : `High` error on `train` dataset ( Model is not trained properly )
- `Low Variance` : `Low` error on `test` dataset ( **Genralized** ) ( Model is able to predict little close to actual )
- The model `fit` the data enough but also captures `noise` and `error` at the time of training ( Low Accuracy )

### `Overfitting` : Low Bias + High Variance ( `Complex` Model )
- `Low Bias` : `Low` error on `train` data ( Model is **trained** very well including `noise` )
- `High Variance` : `High` error on `test` data ( Performs bad on `new unseeen` data )
- When a massive amount of data trains a model, it tends to learn from `noise` and inaccurate data.
- Random error and noise gets added | Complex model | Too many features relative to the number of observations
- Poor **predictive** performance | Do not **genralize** well on the **new unseen data**
- Difference between the prediction on the **new unseen data point** and the **actual data point** is `high` ( High Variance )
- Model tries to `fit` the training data so closely that it does not **generalize** well to **new unseen data**.

`Bias` and `Variance` helps us improve the data fitting | Training process resulting in more **accurate models**.

### Total Error = Bias + Variance + Irreducible Error ( Noise )

### Good Fit Model ( Low Bias + Low Variance )
- `Prediction` is actually **close** to the `actual`.
- **Captures** Less `noise` and `error` at the time of **training** ( Low Bias )
- Generalized enough to work with any **new unseen data** ( Low Variance ) 

### How to Obtain Optimal Tradeoff
1. `Hyperparameter Tuning` : Choosing a right set of `optimal` **hyperparameter** for training.
2. `Regularization` ( `L1` and `L2`) : Technique used to reduce `overfitting` by discouraging  complex models.
3. `Cross Validation`
4. `Resampling`
5. `Ensemble Techniques` : `Bagging` and `Boosting`

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
