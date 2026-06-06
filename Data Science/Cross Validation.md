<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Cross-Validation
- A resampling technique to evaluate the trained model performance on a new, unseen data.
- A method of evaluating the model's performance across random samples of new, unseen data.
- Prevent overfitting and ensure the model generalizes well to unseen data.
- After training, we can't assume the model will perform well on new data.
- The model might underfit the data (High Bias) or Overfit the data (High Variance).
- We can't be sure of the model’s accuracy or variance without evaluation.
- We need validation to ensure the model has low bias and low variance.
- We need the assurance that the model is trained well (Low Bias and Low Variance) 

### Key Idea:
- Initially, more iterations improves accuracy.
- After a point, performance starts declining, model starts overfitting.

### Action:
Stop training when validation error starts increasing (Early Stopping).

### Benefit:
Reduces the risk of memorizing noise, outliers, random patterns in training data.

<h3><a href='#hold'>Holdout</a> | <a href='#kfold'>K Fold</a> | <a href='#skfold'>Stratified K Fold</a> | <a href='#loocv'>Leave One Out</a> </h3>

<h2 name='hold'>1. Holdout Method | Train Test Split</h2>

- Split the dataset into 70% - 30% or 80% - 20% for training and testing.
- The model is trained on the training set to learn patterns, relationships, and trends.
- After training, the model’s performance is evaluated on the testing set by making predictions.
- With limited data, there’s a risk of high bias, meaning the model may not train well.
- Simple to understand, easy to implement, fast to train and evaluate, works well with large datasets.
- Not good for small dataset, can lead to underfitting (high bias) or overfitting (high variance).

<h2 name='kfold'>2. K Fold Cross Validation</h2>

- The dataset is divided into K equal sized subsets called folds, 1 fold is used as the testing set.
- The process is repeated K times, using K - 1 folds for training. Mean error from all trials are calculated.
- This reduces bias and variance, creating a model with low bias, which is ideal for limited data.
- A very high K can cause overfitting, while a very low K is similar to a simple train-test split.
- Uses entire dataset efficiently, every data point is used for both training and testing, works well with small datasets.

<h2 name='skfold'>3. Stratified K Fold Cross Validation</h2>

- Stratified K-Fold Cross Validation ensures each fold has an equal proportion of class labels.
- The data is divided into K equal-sized folds, with each fold containing a balanced distribution of class labels.
- This helps the model to train on equally distributed class labels.
- One fold is used as the testing set, and K - 1 folds are used for training.
- The mean error from all the trials is calculated, reducing bias and variance.
- Maintains balanced class distribution that works best for evaluating models on imbalanced datasets.

```python
# Automatically adjusts weights for each class to handle imbalance:
model = LogisticRegression(class_weight='balanced')

# Ensures that the train and test sets have the same class distribution:
train_test_split(X, y, test_size=0.2, stratify=y)
```

<h2 name='loocv'>4. Leave One Out Cross Validation | LOOCV</h2>

- K = N (Total number of data points), each data point gets used for testing once.
- Leave one data point out for testing and use the rest for training.
- This approach is exhaustive, as you train and validate the model on all possible data points.
- Useful for small datasets, very slow process, computationally expensive, can have high variance.

[CV](https://amueller.github.io/ml-training-intro/slides/03-cross-validation-grid-search.html#21)

### Grid Search
```
✅ Technique to find the best combination of hyperparameter values, especially on small datasets.
✅ Evaluates every possible combination of hyperparameter values within a predefined grid.
✅ Selects the combination that gives the best performance metrics scores.
✅ It’s great for small datasets but is time-consuming and resource-heavy.
```

### 🔄 How Grid Search CV Works
```
1️⃣ Define possible hyperparameter values.
    Example:
    Learning Rate = [0.01, 0.1, 1]
    Max Depth = [3, 5, 7]

2️⃣ Create all possible combinations.

3️⃣ Train and validate the model for each combination using Cross-Validation (CV).

4️⃣ Compare the performance scores.
    Examples: Accuracy, Precision, Recall, F1 Score, RMSE, etc.

5️⃣ Choose the combination with the best score.
    ✅ Best Hyperparameters Found
```

### 🎯 Why Use Grid Search CV?
```
It helps:
✅ Find the best hyperparameters
✅ Improve model accuracy
✅ Reduce manual trial and error
✅ Automate hyperparameter tuning
```

### ⚠️ Drawbacks of Grid Search CV
```
⏳ Slow
    Grid Search tests every combination.

    If there are many hyperparameters, the number of combinations grows very quickly.
    
    Example: 5 values × 5 values × 5 values × 5 values = 625 combinations 😲

💻 Computationally Expensive
    Requires lots of training runs
    Consumes more CPU/GPU resources
    Takes significant time on large datasets

📈 Risk of Overfitting
    Repeated hyperparameters tuning on the same validation data, makes model too specialized to that data.

🚫 Not Ideal for Large Datasets
    For very large datasets or many hyperparameters, Grid Search becomes impractical.
```

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

### Random Grid Search
```
✅ Randomly evaluates different hyperparameter combinations instead of trying every possible combination.
✅ More efficient for large datasets, as it’s faster, uses fewer resources, and is less likely to overfit.
```
```python
from sklearn.model_selection import RandomizedSearchCV
from sklearn.svm import SVC
from scipy.stats import uniform

# Define the parameter distributions
param_dist = {
    'C': uniform(loc=0, scale=10),
    'kernel': ['linear', 'rbf']
}

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
