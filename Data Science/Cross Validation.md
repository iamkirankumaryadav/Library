<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# **Cross-Validation**
- Cross-validation is a resampling technique to evaluate the trained model performance on a limited dataset.
- A method of evaluating the ML model's performance across random samples (new unseen data) of the datasets.
- After training, we can't assume the model will perform well on new data.
- We can't be sure of the model’s accuracy or variance without testing it.
- We need validation to ensure the model has low bias and low variance.
- **Validation:** Assurance that your model is trained well (**Low Bias** and **Low Variance**) 
- To evaluate performance, test the model on new unseen data.
- Based on the results, we can identify underfitting or overfitting.
- Cross-validation gives a more realistic idea of how the model will perform on new unseen data.

<h3><a href='#hold'>Holdout</a> | <a href='#kfold'>K Fold</a> | <a href='#skfold'>Stratified K Fold</a> | <a href='#loocv'>Leave One Out</a> </h3>

<h3 name='hold'>1. Holdout Method | Train Test Split</h3>

- Split the dataset into 70% - 30% or 80% - 20% for training and testing.
- The model is trained on the training set to learn patterns and relationships.
- After training, the model’s performance is evaluated on the testing set by making predictions.
- With limited data, there’s a risk of high bias, meaning the model may not train well.

<h3 name='kfold'>2. K Fold Cross Validation</h3>

- The dataset is divided into **K** equal sized subsets called folds, 1 fold is used as the testing set.
- The process is repeated K times, using K - 1 folds for training each time. The mean error from all trials is calculated.
- This reduces bias and variance, creating a model with low bias, which is ideal for limited data.
- A very high K can cause overfitting, while a very low K is similar to a simple train-test split.

<h3 name='skfold'>3. Stratified K Fold Cross Validation</h3>

- Stratified K-Fold Cross Validation ensures each fold has an equal proportion of class labels.
- The data is divided into K equal-sized folds, with each fold containing a balanced distribution of class labels.
- This helps models train on equally distributed class labels.
- One fold is used as the testing set, and K - 1 folds are used for training.
- The mean error from K trials is calculated, reducing bias and variance.
- It’s an accurate method for evaluating models on imbalanced datasets.

<h3 name='loocv'>4. Leave One Out Cross Validation | LOOCV</h3>

- K = N (where N is the total number of data points), meaning each data point gets used for testing once.
- Leave one data point out for testing and use the rest for training.
- This approach is exhaustive, as you train and validate the model on all possible data points.

[CV](https://amueller.github.io/ml-training-intro/slides/03-cross-validation-grid-search.html#21)

### **Grid Search:**
- Grid Search CV is used to find the best combination of hyperparameters for a model, especially on small datasets.
- It evaluates the model with every possible combination of hyperparameters within a predefined grid.
- This process is called hyperparameter tuning, finding the optimal set of parameters.
- Different hyperparameter combinations are tested to improve the performance metric.
- Grid Search CV tries all possible combinations and returns the best set of parameters based on the test set performance.
- It’s great for small datasets but is time-consuming and resource-heavy.
- Grid Search can lead to overfitting and isn’t ideal for large or complex datasets.

```python
from sklearn.model_selection import GridSearchCV
from sklearn.svm import SVC

# Define the parameter grid
param_grid = {
    'C': [0.1, 1, 10],
    'kernel': ['linear', 'rbf']
}

# Create a Support Vector Classifier model
svc = SVC()

# Create the Grid Search object
grid_search = GridSearchCV(estimator=svc, param_grid=param_grid, cv=5)

# Fit the model
grid_search.fit(X_train, y_train)

# Print the best parameters and score
print(grid_search.best_params_)
print(grid_search.best_score_)
```              

**How to create the Grid?**
1. Define the Hyperparameter Grid: Create a dictionary with hyperparameter names as keys and potential values as lists.
2. Create a Cross-Validation Object: Choose a cross-validation strategy (Holdout, K-Fold, Stratified K-Fold, or LOOCV).
3. Instantiate the Model: Create an instance of your machine learning model.
4. Create the Grid Search Object: Combine the model, hyperparameter grid, and cross-validation strategy into a GridSearchCV object.
5. Fit the Grid Search Object: Train the model on the full dataset using the chosen hyperparameters and cross-validation strategy.

### **Random Grid Search:**

- Random Grid Search CV randomly selects hyperparameter combinations, instead of testing all possible ones.
- It’s more efficient for large datasets, as it’s faster, uses fewer resources, and is less likely to overfit.

```python
from sklearn.model_selection import RandomizedSearchCV
from sklearn.svm import SVC
from scipy.stats import uniform

# Define the parameter distributions
param_dist = {'C': uniform(loc=0, scale=10), 'kernel': ['linear', 'rbf']}

# Create a Support Vector Classifier model
svc = SVC()

# Create the Randomized Search object
random_search = RandomizedSearchCV(estimator=svc, param_distributions=param_dist, n_iter=10, cv=5)

# Fit the model
random_search.fit(X_train, y_train)

# Print the best parameters and score
print(random_search.best_params_)
print(random_search.best_score_)
```

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
