<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Overfitting: Low Bias + High Variance**

### **Low Bias (Low error on train set) + High Variance (High error on the test set)**
- The model overfits the data, memorizing noise and errors, achieving high training accuracy.
- However, this prevents the model from learning underlying patterns and relationships.
- Consequently, the model performs well on the training data but poorly on unseen test data.

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
- Regularization discourages the model from overfitting and encourages it to learn more generalized patterns.
- **Lasso (L1)** adds a penalty equal to the sum of the absolute values of the slopes (forces coefficients to exactly 0).
- Lasso simplifies the model by eliminating features that do not impact the target.
- **Ridge (L2)** adds a penalty equal to the sum of the squared values of the slopes (encourages small coefficients).
- Ridge learns complex data patterns and decreases model complexity.
  
### 3. Apply [Cross Validation](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Cross%20Validation.md)
- Until a certain iteration, new iterations will improve the model's accuracy.
- After some point, the model's ability to generalize to unseen data weakens, and the model starts overfitting.
- During training, monitor the model's performance on a validation set.
- Stop training when the validation set performance starts to decline. This prevents the model from memorizing the noise in the training data.

### 4. Feature Selection
- More observations (rows) are good for model training, but more features (columns) can confuse the model. Select only important features .
- Each feature and observation should be independent of each other. Remove irrelevant and redundant features.
- Remove multicollinear data (e.g., Date of birth and age are redundant, so we can remove one of them).

### 5. [Ensembling](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md) 
- Train and combine multiple weak learners into a single, strong, accurate predictive model.
- Bagging trains multiple individual weak learners (decision trees) in parallel.
- Boosting trains multiple weak learners sequentially, improving in each step by learning from the mistakes of previous models. 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
