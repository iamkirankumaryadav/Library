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


  
