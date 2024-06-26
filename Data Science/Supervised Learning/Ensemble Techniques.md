<p align='right'><a href='https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md'>Back to ML Models</a></p>

# Ensemble Techniques | Method

### **Why Ensemble?**

- Ensemble learning combines multiple models to create a more accurate and robust model.
- The individual models in an ensemble are called base/weak learners.
- The base learners can be decision trees, support vector machines, or neural networks.
- It helps to reduce variance, bias, underfitting and overfitting.
- Ensemble learning can also be used to improve the accuracy of models that are trained on small datasets.
 
Bagging (Bootstrap Aggregation) | Boosting
:--- | :---
`Parallel` | `Series` ( Iterative ) 
Decrease `variance` ( Solve `overfitting` ) | Decrease `bias` ( Improve **training** )
Each model receives equal weight | Weights are assigned based on their **performance**
Samples randomly ( Sample with replacement ) | Samples by increasing weight for **wrong** predictions
Models are built **independently** | Models are improved versions of previously built models
Less time to train | More time to train ( Exhaustive approach )
**Easy** to tune | **Hard** to tune
**Least** chance of `overfitting` | **Easy** to overfit ( Memorize the data + noise )
Samples are drawn randomly with **replacement** | Samples + Observations that are **misclassified** by **previous models**
Random Forest | AdaBoost (**Ada**ptive **Boost**ing), Gradient Boosting and XGBoost

### `Information Gain` (Which feature can explain the split better ?)

- Measures `quality` of the split, `High IG` is better (Explains the further split in a better way)
- `IG` decides which feature will become the next node and will split the data in better way.

### `Entrophy` (Randomness | Uncertainty)

- **Low entropy:** Better (Simple | No Confusion | Easy to conclude data)
- **High entropy:** Hard to conclude (Creates confusion)

Random Forest helps identify important features by analyzing how each feature contributes to splitting the data during the decision-making process of its constituent trees. Here's a breakdown:

1. **Decision Tree Building Blocks:** Random Forest is an ensemble method that combines multiple decision trees. Each tree makes predictions by splitting the data based on features (attributes) that best differentiate between the target classes (outcomes).

2. **Feature Importance:** At each split in a decision tree, the algorithm considers how well a particular feature separates the data into distinct groups regarding the target variable. This is measured using metrics like Gini impurity, Information Gain, Entropy (classification) or variance reduction (regression).

3. **Random Forest's Advantage:** Random Forest builds many trees, and each tree randomly selects a subset of features at each split point. This randomness helps prevent overfitting and ensures a wider range of features are considered across all trees.

4. **Tracking Feature Importance:** Throughout the forest creation process, Random Forest keeps track of how often each feature is chosen for splitting and how well it separates the data. Features that consistently contribute to good splits are considered more important.

5. **Feature Importance Scores:** After building the forest, Random Forest provides a feature importance score for each feature (**feature_importance_**). This score reflects how much a particular feature has been used for splitting across all the trees in the forest. Higher scores indicate greater importance in predicting the target variable.

**Random Forest acts like a team of analysts, each analyzing the data from a slightly different perspective. By combining their insights (feature importance scores), you gain a more comprehensive understanding of which features are most critical for making accurate predictions.**

### `Gini Index` (Check for impurity in the dataset)

- A low Gini index is better.
- **Pure:** All data belongs to the same class in a subset (Gini Index : 0)
- **Impure:** Data is a mixture of different classes in a subset.

![Ensembles](Image/Ensembles.png)

### Benefits of Ensemble Methods

1. Used for `classification` and `regression`
2. Easily handles `outliers` and `missing` values.
3. Accepts various types of inputs (**continuous**, **discrete** and **ordinal**)
4. Less likely to `overfit` and easy to **tune**.
5. Output **feature importance** (Important features for **prediction**)

### A. Bagging (Bootstrap Aggregation)

![Ensemble Bagging](Image/EnsembleBagging.svg)

- Multiple **decision trees** come together to make a combined prediction.
- Dataset is divided into **subsets** | **samples** and passed to multiple **base** learners in `parallel`
- Sample is passed as `row sampling` with `replacement` (This process is called as `bootstrap`)
- Each **learning model** is trained **independently** on its particular **sample** of data.
- **Test sample** is passed to each **model** for the **output**, **Final prediction** is based on **voting**.
- **Voting classifier** is used to find the final result (This process is called as `aggregation`)
- Combine **weak base learners** into **strong learners**.
- `Regression`: `Mean` is calculated.
- `Classification`: `Majority` voted class label.
- Using many trees protects individual decision trees from `overfitting`

### 1. Random Forest 

- **Ensemble** learning method constructs a **collection** of `decision trees` in `parallel` 
- `Aggregate` the `predictions` of each tree to **determine** the `final prediction`
- Dataset is divided as **subsets** | **samples** and passed to multiple `base` learners ( `Decision Tree` )
- Training sample consist of **row sampling** with **replacement**.
- Creating a `decision tree` to its complete `Depth` may cause `overfitting`
- But when we combine **multiple** `decision trees`, **High variance** gets converted to **low variance**, i.e. Reduces `overfitting`
- Can be used for **classification** and **regression**.
- Regressor : **Mean** or **Median** of all the decision trees.
- Classifier : **Majority vote** from all **decision trees**.
- Easily handles **outliers**, **missing data** and **skewness**.
- Accept **continuous** as well as **categorical** inputs.
- Help to understand **important features**. (Parameter: `feature_importance`)

### B. Boosting

![Ensemble Boosting](Image/EnsembleBoosting.svg)

- An ensemble method that **aggregates** a number of **weak learners** in **sequence** to create one **strong model**.
- **Boosting** effectively learns from its previous mistakes with each iteration.
- `Decision trees` are created with only **one depth** or only **one split** (**Stumps**)
- Base learners | Weak learners are created **sequentially** and the **samples** are passed for training.
- **Samples** are created using **row sampling** and **column sampling**.
- **Boosting** combines **weak learners sequentially** by correcting **previous errors** (Forcing them to improve)
- **Weight** is attached with each and every **instance** | **row** | **record**.
- If the **sample** of dataset is **missclassified** then that **sample** is transfered to next **base learner** for **retraining**.
- **Weights** are **adjusted** before each **training** intervals. 
- **Miss classified instances** are focused with **high weights** and **high priority**.

### 1. ADABOOST

- In `ADABOOST` **weights** are only assigned with **incorrect values** in samples.
- **Sequential tree** growing  with **weighted samples**.
- **Base learners** are **decision trees**.
- `Decision trees` are created with only **one depth** or only **one split** (**Stumps**)
- The `stump` with **low entrophy** or **high information gain** is selected first.
- `ADABOOST` allows us to capture the **non-linear relationships**.

### 2. Gradient Boosting

- Uses **gradient descent approach**, Minimize a **loss** function (Overall prediction error)
- Uses the **loss function** of base model (**Decision Tree**) for minimizing the overall **error** of Model.
- An **iterative** approach, **Combine** weak learners to create a **strong** learner by focusing on mistakes of **prior iterations**.

![Gradient Boosting](Image/GB.png)

### 3. XGBoost | Extreme Gradient Boosting

- **Regularized** form of **gradient boosting**, Uses Advanced **Regularization** (`L1` and `L2`)
- Uses **2**<sup>nd</sup> Order **Partial Derivative** for Approximation.
- **High Performance**, Faster than Gradient Boosting.
- Choose a Better **Learning Rate** that suits our Model.
- Even Works Better for **Unstructured Data**.

### Hard Voting vs Soft Voting

- Hard Voting : **Majority voting** is more important.
- Soft Voting : **Predictive probability** of class is important, **Mean** of `probability` is calculated for each class.

### Activation Function
- A function that takes in the **weighted sum** of all the inputs from **previous layer** (+ Adds **bias**) and generates output for **next layer**.
