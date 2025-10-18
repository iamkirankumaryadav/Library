<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Overfitting: Low Bias + High Variance**

### **Low Bias (Low error on train set) + High Variance (High error on the test set)**
- The complex model overfits by memorizing noise and errors, leading to high training accuracy.
- This prevents the model from learning the true patterns and relationships in the data.
- As a result, it performs well on training data but poorly on new, unseen test data.

## **How to identify overfitting?** 

### Train Test Split | Observe Accuracy (Score)
- Split the dataset into train and test sets (80/20 or 70/30 train-test split).
- Check whether the trained model generalizes well to the new, unseen test dataset.
- Calculate the accuracy score of the training set: `model.score(X_train, y_train)` and test set: `model.score(X_test, y_test)`.
- If the training set accuracy is much higher than the test set accuracy, it indicates overfitting.

## **How to prevent from overfitting?**

### 1. Collect more relevant data for training.
- With more relevant data (observations), the model can better learn the underlying patterns and relationships.
- **Data Augmentation:** Artificially expand your dataset by creating new data points through transformations.

### 2. Apply [Regularization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md) 
- Slope | Coefficient | Weight | Gradient (All are the same)
- A technique to prevent overfitting in ML models.
- Regularization discourages the model from overfitting and encourages it to learn more generalized patterns.
- **Lasso (L1)** adds a penalty equal to the sum of the absolute values of the slopes (Shrink few coefficients to 0).
- Lasso simplifies the model by eliminating features that do not impact the target.
- **Ridge (L2)** adds a penalty equal to the sum of the squared values of the slopes (Encourages small coefficients).
- Ridge simplifies the model by reducing model complexity. Shrinks coefficients but keep all features.
- Regularization is like a speed limit, without it model drives fast (overfits), with it, the model stay safe and balanced.
  
### 3. Apply [Cross Validation](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Cross%20Validation.md)
- Until a certain iteration, newer iterations improve the model's accuracy.
- After a certain point, the model's ability to generalize to unseen data weakens, and it begins overfitting.
- Monitor the model's performance on a validation set. Stop training when validation error increases (Early Stopping).

### 4. Feature Selection
- More observations are good for model training, but more features can confuse the model. Select only important features .
- Each feature and observation should be independent of each other. Remove irrelevant and redundant features.
- Remove multicollinear data (e.g., Date of birth and age are redundant, so we can remove one of them).

### 5. [Ensembling](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md) 
- Trains and combines multiple weak learning models into a single, strong, accurate predictive model.
- Bagging trains multiple individual weak learners (decision trees) in parallel.
- Boosting trains multiple weak learners sequentially, improving at each step by learning from the mistakes of previous models. 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
