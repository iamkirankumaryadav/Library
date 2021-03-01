# Cross Validation
- **Validation** : **Assurance** that your Model is trained well ( **Low Bias** and **Low Variance** ) 
- Whether Model is **Generalized** well for the **New Unseen Data**.
- Aim is to reduce **Overfitting**.

### 1. Holdout Method ( **Traditional Approach** )
- Remove a Part of **Training Data** before Training and keep it for **Validation**.
- By Reducing the **Training Data**, we risk losing important **Patterns | Trends** in Dataset.
- Suffers from **High Variance**.

### 2. K Fold Cross Validation
- Data is divided into **k** subsets.
- One of **k** subset is used as **Validation Set**.
- **k - 1** subsets are used as **Training Set**.
- **Mean** Error of **k** trials is calculated.
- Reduces **Bias** and **Variance**.

### 3. Stratified K Fold Cross Validation
- Data is divided into **k** subsets.
- Each Subset has **Equal Proportion** of samples of each **Target Class**.
- One of **k** subset is used as **Validation Set**.
- **k - 1** subsets are used as **Training Set**.
- **Mean** Error of **k** trials is calculated.
- Reduces **Bias** and **Variance**.

### Leave One Out Cross Validation | LOOCV
- Leave **One Data** from the Training Dataset for **Validation**.
- Use remaining Data Samples for **Training**.
- Repeated for all combinations.
- Approach is **Exhaustive**, Need to **Train** and **Validate** the Model for all **Possible Combinations**. 
