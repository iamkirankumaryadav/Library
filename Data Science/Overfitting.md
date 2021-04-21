# Overfitting

### Low Bias + High Variance = Overfitting

### Low Bias : Low Error on Train Set 
- Model has **Memorized** the Data including **Noise** and **Error** with very Good **Accuracy**.

### High Variance : High Error on Test Set
- Model Performs **Better** on **Training Data** but it does not **Generalize** Well on the **New Unseen Data** ( **Test Data** ).

### How to Identify Overfitting ? 

### 1. Hold Out Data or Splitting Data Set
- Split the Data Set into Train Set and Test Set.
- Train the Model on Training Set 
- Check Performance on Test Set ( Check whether the Trained Model Generalizes Well on Test Data )

### 2. Test Accuracy Score
- Observing Loss and Accuracy of Model on **Training Set** and **Test Set**
- **model.score( X_train, y_train )**
- **model.score( X_test, y_test )**

### How to Prevent from Overfitting ?

### 1. More Data
- Get More **Training Data**

### 2. Apply Regularization  
- Lasso ( L1 ) : Sum of `Absolute` pf Coefficients | Weights ( Can Lead Coefficient to Exactly 0 )
- Ridge ( L2 ) : Sum of `Squared` of Coefficient | Weights ( **Penalize** Certain Value of **Weights** )
- Able to Learn **Complex Data Patterns**.

### 3. K Fold Cross Validation and Grid Search Cross Validation
- Measure How Well each **Iteration** of the Model Performs.
- Until a certain Number of Iterations, **New Iteration** Improve the Model.
- After some Point The Model's Ability of Generalize gets weak and Starts Overfitting.

### 4. Feature Selection
- Select only the **Important** Features ( Large Number of Features can Confuse the Model )
- Remove **Multicollinear Data** ( e.g DOB and Age can express each other so we can remove one of them )

### 5. Ensembling 
- **Combine Predictions** from Multiple Separate Models.
- **Bagging** Trains Multiple Models in **Parallel**
- **Boosting** Trains Multiple Models in **Sequence** ( Improving Each Step Learning from Previous Mistakes ) 

### 6. Reduce Layers ( Deep Learning )
- **Removing Layers** or Number of **Elements** in the **Hidden Layers**.

### 7. Dropout Layers 
- Randomly Remove Certain Features by Setting them to Zero.
  
