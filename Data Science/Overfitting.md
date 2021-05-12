<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Overfitting

### Low Bias + High Variance = Overfitting

### Low Bias : Low Error on Train Set 
- Model has **Memorized** the Data including **Noise** and **Error** with very Good **Accuracy**.

### High Variance : High Error on Test Set
- Model Performs **Better** on **Training Data** but it does not **Generalize** Well on the **New Unseen Data** ( **Test Data** )

### How to Identify Overfitting ? 

### Hold Out Data | Split Data Set | Observe Accuracy and Loss
- **Split** the **Data Set** into `Train Set` and `Test Set`.
- Check whether the Trained Model **Generalizes** Well on **New Unseen Test Data**. 
- **Accuracy** of **Train Set** : `model.score( X_train, y_train )`
- **Accuracy** of **Test Set** : `model.score( X_test, y_test )`

### How to Prevent from Overfitting ?

### 1. More Data
- Get More **Training Data**

### 2. Apply [Regularization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md) 
- Lasso ( `L1` ) : Sum of `Absolute` of **Coefficients** | Weights ( **Coefficient** to Exactly 0 )
- **Simplify** the Model + **Feature Selection**.
- Ridge ( `L2` ) : Sum of `Squared` of **Coefficients** | Weights ( **Penalize** Certain Value of **Weights** )
- Able to Learn **Complex Data Patterns** | Decrease the **Complexity** of Model.

### 3. K Fold Cross Validation and Grid Search Cross Validation
- Measure How Well each **Iteration** of the Model Performs.
- Until a certain Number of Iterations, **New Iteration** Improve the Model.
- After some Point The **Model's Ability** to **Generalize** gets weak and Starts **Overfitting**.

### 4. Feature Selection
- Select only the **Important** Features ( Large Number of Features can **Confuse** the Model )
- Remove **Multicollinear Data** ( e.g DOB and Age can Express each other so we can remove one of them )

### 5. Ensembling 
- **Combine Predictions** from Multiple Separate Models | Train Multiple **Weak Learners** to make them a Single **Strong Model**.
- **Bagging** Trains Multiple `Individual` Learners in **Parallel**.
- **Boosting** Trains Multiple `Weak` Learners in **Sequence** ( Improving in Each Steps Learning from the Mistakes of Previous Models ) 

### 6. Reduce Layers ( Deep Learning )
- **Removing Layers** or Number of **Elements** in the **Hidden Layers**.

### 7. Dropout Layers ( Deep Learning )
- Randomly `Drop` Certain Features by Setting them to `Zero` ( Fully Connected Layer )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
