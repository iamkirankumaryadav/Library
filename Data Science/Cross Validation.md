<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Cross Validation
- **Validation** : **Assurance** that your Model is trained well ( **Low Bias** and **Low Variance** ) 
- Whether Model is **Generalized** well for the **New Unseen Data**
- Aim is to reduce **Overfitting**

<h3><a href='#hold'>Holdout</a> | <a href='#kfold'>K Fold</a> | <a href='#skfold'>Stratified K Fold</a> | <a href='#loocv'>Leave One Out</a> </h3>

<h3 name='hold'> 1. Holdout Method ( Traditional Approach | Train Test Split )</h3>

- Split the Data Set in ( 70% - 30% ) or ( 80% - 20% ) for Training | Validation | Testing 
- Keep a Part of **Data Set** for **Validation** and Use rest of the Data Set for Training
- Used to **Evaluate** Models Ability to **Generalize** New **Unseen** Data

<h3 name='kfold'> 2. K Fold Cross Validation</h3>

- Data is divided into **k** subsets
- One of **k** subset is used as **Validation Set**
- **k - 1** subsets are used as **Training Set**
- **Mean** Error of **k** trials is calculated
- Reduces **Bias** and **Variance**
- Sampling `without` Replacement
- Very High Value of **K** will lead to **Over Fitting** 
- Very Low Value of **K** will work similar to Train Test Split

<h3 name='skfold'> 3. Stratified K Fold Cross Validation</h3>

- Data is divided into **k** Subsets
- Each Subset has **Equal Proportion** of samples of each **Target Class**
- One of **k** subset is used as **Validation Set**
- **k - 1** subsets are used as **Training Set**
- **Mean** Error of **k** trials is calculated
- Reduces **Bias** and **Variance**

<h3 name='loocv'> 4. Leave One Out Cross Validation | LOOCV</h3>

- Leave **One Data** from the Training Dataset for **Validation**
- Use remaining Data Samples for **Training**
- Repeated for all combinations
- Approach is **Exhaustive**, Need to **Train** and **Validate** the Model for all **Possible Combinations**

[CV](https://amueller.github.io/ml-training-intro/slides/03-cross-validation-grid-search.html#21)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
