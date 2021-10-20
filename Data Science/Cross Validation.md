<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Cross Validation

- `Resampling technique` used to evaluate model performance on a limited dataset.
- Once model is trained, we just can't assume that it is going to perform well on the **new unseen data**.
- We can't be sure that the model will give the desired `accuracy` and `variance`
- We need some kind of `assurance` for the `accuracy` of the `predictions` that our model will give. 
- `Validation` : **Assurance** that your model is trained well ( **Low Bias** and **Low Variance** ) 
- To evaluate the performance of any model, we need to test it on some new unseen data.
- So based on the performance we can say whether there is `underfitting` or `overfitting`
- `Cross Validation` is one of the technique used to test the performance.

<h3><a href='#hold'>Holdout</a> | <a href='#kfold'>K Fold</a> | <a href='#skfold'>Stratified K Fold</a> | <a href='#loocv'>Leave One Out</a> </h3>

<h3 name='hold'> 1. Holdout Method ( Traditional Approach | Train Test Split )</h3>

- Split the data set in ( 70% - 30% ) or ( 80% - 20% ) for `training`, `validation` and `testing`
- Keep a part of **data set** for **validation** and use rest of the data set for training.
- Used to **evaluate** models ability to **generalize** the new **unseen** data.
- There is a possibility of **high bias** if we have limited data.
- We would miss some information about the data which we have not used for training.

<h3 name='kfold'> 2. K Fold Cross Validation</h3>

- Data is divided into **K** subsets.
- One of **K** subset is used as **validation set**.
- **K - 1** subsets are used as **training set**.
- **Mean** error of **K** trials is calculated.
- Reduces **bias** and **variance** ( Generally generates low bias model )
- Sampling `without` replacement ( Every observation from the data set is used for training and testing )
- Best approach if we have limited input data.
- Very high value of **K** will lead to **Overfitting**.
- Very low value of **K** will work similar to train test split.

<h3 name='skfold'> 3. Stratified K Fold Cross Validation</h3>

- Data is divided into `K` subsets.
- Each subset has **equal proportion** of samples of each **target class labels**.
- Models get **equally** distributed target class labels for **training**.
- One of **K** subset is used as **validation set**.
- **K - 1** subsets are used as **training set**.
- **Mean** error of **K** trials is calculated.
- Reduce **bias** and **variance** ( Try to creates a better model with best accuracy )

<h3 name='loocv'> 4. Leave One Out Cross Validation | LOOCV</h3>

- K = N ( N : Number of data points in the data set )
- Leave **one data** from the dataset for **validation** and use the remaining data samples for **training**.
- Approach is **exhaustive**, need to **train** and **validate** the model for all **possible data points**.

[CV](https://amueller.github.io/ml-training-intro/slides/03-cross-validation-grid-search.html#21)

### Grid Search
- One must select the correct algorithm with the correct combination of `hyperparameters` to train model.
- The process of choosing the optimal set of parameters is known as `hyperparameter tuning`
- Different combination of hyperparameters is used to improve the `performance metric`
- `Grid Search` cross validation is a technique to select the best model. 
- Parameterized by a grid of `hyperparameters`
- `Grid Search` cross validation tries all combinations of parameters `grid` for a model. 
- Returns with the best set of parameters having the `best performance` score.

`Random Grid Search` cross validation : The algorithm will randomly choose the combination of parameters. 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
