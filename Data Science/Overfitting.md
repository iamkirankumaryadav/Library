<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Overfitting

### Low Bias + High Variance = Overfitting

### Low Bias : Low Error on Train Set 
- Model has **memorized** the data including **noise** and **error** with very good **accuracy**.

### High Variance : High Error on Test Set
- Model performs **better** on **Training** dataset but it does not **Generalize** well on the **new unseen** dataset ( **Test Data** )

### How to Identify Overfitting ? 

### Hold Out Data | Split Data Set | Observe Accuracy and Loss
- **Split** the **data Set** into `Train Set` and `Test Set`.
- Check whether the trained model **Generalizes** well on **new unseen** test data. 
- **Accuracy** of **Train Set** : `model.score( X_train, y_train )`
- **Accuracy** of **Test Set** : `model.score( X_test, y_test )`
- If **Accuracy** of **Train Set** is better and **Accuracy** on **Test Set** is worst ( There is an `Overfitting` in the model )

### How to Prevent from Overfitting ?

### 1. More Data
- Get more data for **training**.

### 2. Apply [Regularization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md) 
- Lasso ( `L1` ) : Sum of `Absolute` of **Slope** | Coefficient | Weight ( **Coefficient** to Exactly 0 )
- **Simplify** the Model + **Feature Selection**.
- Ridge ( `L2` ) : Sum of `Square` of **Slope** | Coefficient | Weight ( **Penalize** certain value of **slopes** towards zero )
- Able to learn **complex data patterns** | Decreases the **complexity** of model.

### 3. K Fold Cross Validation and Grid Search Cross Validation
- Measure how well each **iteration** of the model performs.
- Until certain iterations, **New iterations** improves the model.
- After some point the **model's ability** to **Generalize** gets weak and starts **overfitting**.

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
