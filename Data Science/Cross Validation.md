<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Cross Validation
- **Validation** : **Assurance** that your Model is trained well ( **Low Bias** and **Low Variance** ) 
- Whether Model is **Generalized** well for the **New Unseen Data**
- Aim is to reduce **Overfitting**

### 1. Holdout Method ( **Traditional Approach** )
- Remove a Part of **Training Data** before Training and keep it for **Validation**
- Used to **Evaluate** Models Ability to **Generalize** to **Unseen** Data
- By Reducing the **Training Data**, we risk losing important **Patterns | Trends** in Dataset
- Suffers from **High Variance**

### 2. K Fold Cross Validation
- Data is divided into **k** subsets
- One of **k** subset is used as **Validation Set**
- **k - 1** subsets are used as **Training Set**
- **Mean** Error of **k** trials is calculated
- Reduces **Bias** and **Variance**
- Sampling `without` Replacement
- Very High Value of **K** will lead to **Over Fitting** 
- Very Low Value of **K** will work similar to Train Test Split

### 3. Stratified K Fold Cross Validation
- Data is divided into **k** subsets
- Each Subset has **Equal Proportion** of samples of each **Target Class**
- One of **k** subset is used as **Validation Set**
- **k - 1** subsets are used as **Training Set**
- **Mean** Error of **k** trials is calculated
- Reduces **Bias** and **Variance**

### 4. Leave One Out Cross Validation | LOOCV
- Leave **One Data** from the Training Dataset for **Validation**
- Use remaining Data Samples for **Training**
- Repeated for all combinations
- Approach is **Exhaustive**, Need to **Train** and **Validate** the Model for all **Possible Combinations**

[CV](https://amueller.github.io/ml-training-intro/slides/03-cross-validation-grid-search.html#21)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
