<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Overfitting: Low Bias + High Variance**

### **Low Bias (Low error on train set) + High Variance (High error on the test set)**

- The model memorizes the data too well with certain assumptions including noise/error with very good accuracy on the training set.
- But the model loses the ability to learn the hidden patterns and relationships.
- The model performs better on the training dataset, but it does not generalize well on the new unseen test set.

## **How to identify overfitting?** 

### Train Test Split | Observe Accuracy (Score)
- Split the dataset into train and test sets (80/20 to 70/30 train test split)
- Check whether the trained model generalizes well on the new unseen test dataset. 
- Calculate the accuracy score of the train set: **model.score(X_train, y_train)** and test set: **model.score(X_test, y_test)**
- If the accuracy of the train set is better and the accuracy of the test set is worse then it's an overfitting scenario.

## **How to prevent from overfitting?**

### 1. Collect more relevant data for training.
- With more relevant data (observations), the model can learn the underlying patterns and relationships in a better way.
- **Data Augmentation:** Artificially expand your dataset. creating new data points by applying transformations.

### 2. Apply [Regularization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md) 
- Slope | Coefficient | Weight | Gradient (All are same)
- Regularization discourages the model from overfitting and encourages one to learn more generalized patterns.
- **Lasso (L1)** adds a penalty equal to the sum of the absolute value of slope (Force coefficients to exactly 0)
- Lasso simplifies the model by eliminating the features that do not create any impact on the target.
- **Ridge (L2)** adds a penalty equal to the sum of the squared value of slope (Encourage small coefficients)
- Ridge learn complex **data patterns** | Decreases the complexity of model.

### 3. Apply [Cross Validation](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Cross%20Validation.md)
- Until certain iterations the new iterations will improve the accuracy of the model.
- After some point the **model's ability** to **generalize** unseen data gets weak and model starts **overfitting**.
- During training, monitor the model's performance on a validation set.
- Stop training when the performance on the validation set starts to decline. This prevents the model from memorizing noise in training data

### 4. Feature Selection
- More observations (rows) are good for model training but more features (columns) confuse the model.
- Select only **important** features (Large number of features can **confuse** the model)
- Each feature and observation should be independent of each other. Remove irrelevant and redundant features.
- Remove **multicollinear** data (e.g DOB and age can express each other so we can remove one of them)

### 5. [Ensembling](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md) 
- Train and combine multiple weak learners into a single strong accurate predicting model.
- **Bagging** trains multiple individual weak learners (Decision tree) in **parallel**.
- **Boosting** trains multiple weak learners in **sequence** (Improving in each step by learning from the mistakes of previous models) 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
