# Overfitting

### Low Bias + High Variance = Overfitting

### Low Bias : Low Error on Train Set 
- Model has **Memorized** the Data including **Noise** and **Error** with very Good **Accuracy**.

### High Variance : High Error on Test Set
- Model Performs **Better** on **Training Data** but it does not **Generalize** Well on the **New Unseen Data** ( **Test Data** ).

### How to Identify Overfitting

### 1. Metrics 
- Observing Loss and Accuracy of Model on **Training Set** and **Test Set**
- **model.score( X_train, y_train )**
- **model.score( X_test, y_test )**



### How to Prevent from Overfitting ?

### 1. More Data
- Get More **Training Data**

### 2. Apply Regularization  
- Lasso ( L1 ) : Sum of `Absolute` Coefficient ( Can Lead Coefficient to Exactly 0 )
- Ridge ( L2 ) : Sum of `Squared` Coefficient
- Elastic Net : L1 + L2

### 2. Reduce Layers ( Deep Learning )
- **Removing Layers** or Number of **Elements** in the **Hidden Layers**.

### 3. Dropout Layers 
- Randomly Remove Certain Features by Setting them to Zero.
  
