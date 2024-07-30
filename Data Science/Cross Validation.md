<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# **Cross-Validation**
- Cross-validation is a resampling technique to evaluate the trained model performance on a limited dataset.
- Cross-validation evaluates how well the model will perform on new unseen fresh data.
- Once the model is trained, we can't assume that it is going to perform well on the **new unseen data**.
- We can't be sure that the model will give the desired **accuracy** and **variance**.
- We need some kind of assurance for the accuracy of the predictions that our model will give. 
- **Validation:** Assurance that your model is trained well (**Low Bias** and **Low Variance**) 
- To evaluate the performance of any model, we need to test it on some new unseen data.
- So based on the performance we can say whether there is underfitting or overfitting.
- Cross-validation gives a more realistic and stable idea of how well the model will perform on new data.

<h3><a href='#hold'>Holdout</a> | <a href='#kfold'>K Fold</a> | <a href='#skfold'>Stratified K Fold</a> | <a href='#loocv'>Leave One Out</a> </h3>

<h3 name='hold'>1. Holdout Method | Train Test Split</h3>

- Split the entire dataset into (70% - 30%) or (80% - 20%) for the training set and testing set.
- The ML model is trained using only the training data. Learns to identify patterns and relationships within the data.
- Once trained, the model's performance is evaluated on the testing set. The model makes predictions on the testing set.
- There is a possibility of **high bias** if we have limited data, it will not train the model properly.

<h3 name='kfold'>2. K Fold Cross Validation</h3>

- The entire dataset is divided into **K** equal sized subsets called folds, 1 of **K** subset is used as **testing set**.
- The process is iterated K times, and **K - 1** subsets are used as training sets. **Mean** error of **K** trials is calculated.
- Reduces **bias** and **variance** (Generally generates low bias model) It's best approach if we have limited input data.
- A very high value of K will lead to overfitting and a very low value of K will work similarly to the train test split.

<h3 name='skfold'>3. Stratified K Fold Cross Validation</h3>

- A variation of K fold cross-validation that ensures folds have the same proportion of samples for each class.
- Data is divided into K equal-sized folds, each subset has equal proportion samples of each **target class labels**.
- Models get **equally** distributed target class labels for **training**.
- One of **K** fold is used as **testing set**, and **K - 1** folds are used as **training set**.
- **Mean** error of **K** trials is calculated. Reduce **bias** and **variance**.
- An accurate way to evaluate the performance of a model on imbalanced data sets is needed.

<h3 name='loocv'>4. Leave One Out Cross Validation | LOOCV</h3>

- K = N (N: Number of data points in the data set) Iterate through each data point in the dataset.
- Leave **one data point** from the dataset for **testing** and use the remaining samples for **training**.
- Approach is **exhaustive**, need to **train** and **validate** the model for all **possible data points**.

[CV](https://amueller.github.io/ml-training-intro/slides/03-cross-validation-grid-search.html#21)


### **Grid Search:**

- Technique used to evaluate the model with every possible combination of hyperparameters within a predefined grid.
- Creates a grid of hyperparameter values and trains the models with each combination.
- Choosing the optimal set of parameters is known as **hyperparameter tuning**.
- Different combinations of hyperparameters are used to improve the **performance metric**
- **Grid Search cross-validation** tries all combinations of parameter grid values for training a model. 
- Returns with the best set of parameters having the best performance score on the test set.
- It is good if the data set is small, it's more time-consuming and requires more resources to run.
- Prone to overfitting, Not suitable for large and complex data.

### **Random Grid Search:**

- Random Grid Search cross-validation randomly chooses the combination of hyperparameter values instead of evaluating all possible combinations.
- It is good if the data set is very large, it's less time-consuming utilizes fewer resources, and is less likely to overfit the training data.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
