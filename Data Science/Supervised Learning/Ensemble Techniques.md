# Ensemble Techniques

> Combining Multiple Models.

### A. Bagging (Bootstrap Aggregation)

- Dataset is divided and passed as sample of Datasets to **Multiple Base Learners**.
- Dataset is passed with **Row Sampling** with **Replacement** (**Bootstrap**)
- Each Learning Model will be trained on its particular sample of Data.
- Voting Classifier is used to find the Final Result (**Aggregation**)

### 1. Random Forest

- Dataset is divided and passed as sample of Datasets to **Multiple Base Learners** (Decision Tree)
- Training Sample consist of **Row Sampling** and **Column Sampling** with **Replacemen**.

- If I Create Decision Tree to its complete depth, problem of **Overfitting** will occur. 
- But when we combine Multiple Decision Trees, **High Variance** gets converted to **Low Variance**, i.e. Reduces **Overfitting**

- Regressor : **Mean** or **Median** of Output of Decision Trees.
- Classifier : **Majority Vote**.

### B. Boosting

### 1. ADABOOST

### 2. Gradient Boostinf

### 3. XGBoost
