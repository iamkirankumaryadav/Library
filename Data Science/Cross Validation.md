<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Cross Validation

- Once model is trained, we just can't assume that it is going to perform well on the **new unseen data**.
- We cant be sure that the model will give the desired **accuracy** and **variance**.
- We need some kind of **assurance** for the **accuracy** of the **predictions** that our model will give. 
- **Validation** : **Assurance** that your model is trained well ( **Low Bias** and **Low Variance** ) 
- Whether model is **Generalized** well for the **new unseen data**.
- To evaluate the performance of any model, we need to test it on some new unseen data.
- So based on the performance we can say whether our model is **Underfitting** or **Overfitting**.
- `Cross Validation` is one of the technique used to test the performance.

<h3><a href='#hold'>Holdout</a> | <a href='#kfold'>K Fold</a> | <a href='#skfold'>Stratified K Fold</a> | <a href='#loocv'>Leave One Out</a> </h3>

<h3 name='hold'> 1. Holdout Method ( Traditional Approach | Train Test Split )</h3>

- Split the data set in ( 70% - 30% ) or ( 80% - 20% ) for `Training`, `Validation` and `Testing`
- Keep a part of **data set** for **validation** and use rest of the data set for training.
- Used to **evaluate** models ability to **generalize** the new **unseen** data.
- There is a possibility of **high bias** if we have limited data.
- We would miss some information about the data which we have not used for training.

<h3 name='kfold'> 2. K Fold Cross Validation</h3>

- Data is divided into **K** subsets.
- One of **K** subset is used as **validation set**.
- **K - 1** subsets are used as **training set**.
- **Mean** error of **K** trials is calculated.
- Reduces **Bias** and **Variance** ( Generally generates less biased model )
- Sampling `without` Replacement ( Every observation from the data set is used for training and testing )
- Best approach if we have limited input data.
- Very high value of **K** will lead to **Overfitting** ( Low **bias** but large **variance** )
- Very low value of **K** will work similar to Train Test Split.

<h3 name='skfold'> 3. Stratified K Fold Cross Validation</h3>

- Data is divided into **K** subsets.
- Each subset has **equal proportion** of samples of each **target class labels**.
- Models get **equally** distributed data for **training** and **testing**.
- One of **K** subset is used as **validation set**.
- **K - 1** subsets are used as **training set**.
- **Mean** error of **K** trials is calculated.
- Reduce **Bias** and **Variance** ( Try to creates a better model with best accuracy )

<h3 name='loocv'> 4. Leave One Out Cross Validation | LOOCV</h3>

- K = N ( N : Number of Data Points in the Data Set )
- Leave **One Data** from the Dataset for **Validation**
- Use remaining Data Samples for **Training**
- Repeated for all combinations
- Approach is **Exhaustive**, Need to **Train** and **Validate** the Model for all **Possible Combinations**

[CV](https://amueller.github.io/ml-training-intro/slides/03-cross-validation-grid-search.html#21)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
