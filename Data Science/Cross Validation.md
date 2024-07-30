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
- A technique used in ML to find the optimal combination of hyperparameters for a given model trained on the limited dataset.
- Grid Search CV evaluates the model with every possible combination of hyperparameters within a predefined grid.
- Creates a grid of hyperparameter values and trains the models with each combination.
- Choosing the optimal set of parameters is known as **hyperparameter tuning**.
- Different combinations of hyperparameters are used to improve the **performance metric**.
- **Grid Search cross-validation** tries all combinations of parameter grid values for training a model. 
- Returns with the best set of parameters having the best performance score on the test set.
- It is good if the data set is small, it's more time-consuming and requires more resources to run.
- Prone to overfitting, Not suitable for large and complex data.

```python
from sklearn.model_selection import GridSearchCV, train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.datasets import load_digits
from sklearn.metrics import accuracy_score

# Load the Digits dataset
digits = load_digits()
X, y = digits.data, digits.target

# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Define/Instantiate the Random Forest model
rf_model = RandomForestClassifier()

# Define the hyperparameter grid
param_grid = {
    'n_estimators': [50, 100, 150],
    'max_depth': [None, 10, 20],
    'min_samples_split': [2, 5, 10]
}

# Create GridSearchCV object
grid_search = GridSearchCV(estimator=rf_model, param_grid=param_grid, scoring='accuracy', cv=5)

# Fit the grid search to the data
grid_search.fit(X_train, y_train)

# Get the best hyperparameters
best_params = grid_search.best_params_

# Get the best model
best_model = grid_search.best_estimator_

# Evaluate the best model on the test set
y_pred = best_model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)

print(f"Best Hyperparameters: {best_params}")
print(f"Test Set Accuracy: {accuracy}")
```              

**How to create the Grid?**
1. **Define the Hyperparameter Grid:** Create a dictionary where keys are hyperparameter names and values are lists of potential values.
2. **Create a cross-validation object:** Specify the cross-validation strategy (Holdout, K Fold, Stratified K Fold, or LOOCV)
3. **Instantiate the Model:** Create an instance of the machine learning model.
4. **Create the Grid Search Object:** Combine the model, hyperparameter grid, and cross-validation strategy into a GridSearchCV object.
5. **Fit the Grid Search Object:** Train the model on the entire dataset using the specified hyperparameter combinations and cross-validation strategy.

### **Random Grid Search:**

- Random Grid Search cross-validation randomly chooses the combination of hyperparameter values instead of evaluating all possible combinations.
- It is good if the data set is very large, it's less time-consuming utilizes fewer resources, and is less likely to overfit the training data.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
