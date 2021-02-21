# Ensemble Techniques

> Combining Multiple Models.

### A. Bagging (Bootstrap Aggregation)

- Dataset is divided and passed as sample of Datasets to **Multiple Base Learners**. (Base Learner can be any **ML Algorithm**)
- We can use Different **Algorithms** and Different **Training Set**.
- Dataset is passed with **Row Sampling** with **Replacement** (**Bootstrap**)
- Each Learning Model will be trained on its particular sample of Data.
- Voting Classifier is used to find the Final Result (**Aggregation**)
- Combine Weak Base Learners into **Strong Learner** in terms of **Classifier** or **Prediction**.
- Improves **Accuracy**. 

### 1. Random Forest

- Dataset is divided and passed as sample of Datasets to **Multiple Base Learners** (Decision Tree)
- Training Sample consist of **Row Sampling** and **Column Sampling** with **Replacemen**.

- If I Create Decision Tree to its complete depth, problem of **Overfitting** will occur. 
- But when we combine Multiple Decision Trees, **High Variance** gets converted to **Low Variance**, i.e. Reduces **Overfitting**

- Regressor : **Mean** or **Median** of Output of Decision Trees.
- Classifier : **Majority Vote**.

### B. Boosting

- Base Learners are Created **Sequentially** and the Sample of Data Sets are passed for Training.
- If the portion of Dataset is Incorrectly classified then that portion is transfered to next Base Learner.

### 1. ADABOOST

- In ADABOOST **weights** is assigned with Samples
- Base Learners are Decision Trees.
- Decision Trees are Created with only **One Depth** (**Stumps**)
- The Stump will Less **Entrophy** is Selected First.

### 2. Gradient Boostinf

### 3. XGBoost
