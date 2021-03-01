# Ensemble Techniques

> Combining Multiple **Models** (Homogeneous | Heterogeneous).

### A. Bagging (Bootstrap Aggregation)

![Ensemble Bagging](Image/EnsembleBagging.svg)

- Dataset is divided as **Subsamples** and passed to **Multiple Base Learners**.
- **Parallel** Tree growing **Subsamples**
- Dataset is passed with **Row Sampling** with **Replacement** (**Bootstrap**)
- Each Learning Model will be trained on its particular sample of Data
- Voting Classifier is used to find the Final Result (**Aggregation**)
- Combine Weak Base Learners into **Strong Learner** in terms of **Classifier** or **Prediction**
- Test Sample is passed to each Model for the Output
- Improves **Accuracy**. 

### 1. Random Forest

- Dataset is divided and passed as sample of Datasets to **Multiple Base Learners** (Decision Tree)
- Training Sample consist of **Row Sampling** and **Column Sampling** with **Replacement**.

- If I Create Decision Tree to its complete depth, problem of **Overfitting** will occur. 
- But when we combine Multiple Decision Trees, **High Variance** gets converted to **Low Variance**, i.e. Reduces **Overfitting**

- Regressor : **Mean** or **Median** of Output of Decision Trees.
- Classifier : **Majority Vote**.

### B. Boosting

![Ensemble Boosting](Image/EnsembleBoosting.svg)

- Base Learners are Created **Sequentially** and the Sample of Data Sets are passed for Training.
- **Weight** is attached with each and every **Instance** | Row | Record.
- If the portion of Dataset is Incorrectly classified then that portion is transfered to next Base Learner for Training again.
- Weights are **Adjusted** before each Training and Miss Classified Instances are focused with High Priority.
- Test Sample is passed to each Model for the Output.

### 1. ADABOOST

- In ADABOOST **weights** is assigned with Samples
- Base Learners are **Decision Trees**.
- Decision Trees are Created with only **One Depth** (**Stumps**)
- The Stump will Less **Entrophy** is Selected First.

### 2. Gradient Boosting

### 3. XGBoost | Extreme Gradient Boosting


### Hard Voting vs Soft Voting

- Hard Voting : **Majority Voting** is more important.
- Soft Voting : **Predictive Probability** of Class is important, **Mean** of Probability is Calculated for each Class.
