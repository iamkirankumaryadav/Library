<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Overfitting

### Low Bias + High Variance = Overfitting

### Low Bias : Low error on train set 
- Model has **memorized** the data including **noise** and **error** with very good **accuracy**.

### High Variance : High error on test set
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
- Lasso ( `L1` ) : Sum of `absolute` of **slope** | coefficient | weight ( **Coefficient** to exactly 0 )
- **Simplify** the model + **feature selection** ( Select only **important** features )
- Ridge ( `L2` ) : Sum of `square` of **slope** | coefficient | weight ( **Penalize** certain value of **slopes** towards zero )
- Able to learn **complex data patterns** | Decreases the **complexity** of model.

### 3. K Fold Cross Validation and Grid Search Cross Validation
- Measure how well each **iteration** of the model performs.
- Until certain iterations, **new iterations** improves the model.
- After some point the **model's ability** to **generalize** gets weak and starts **overfitting**.

### 4. Feature Selection
- Select only **important** features ( Large number of features can **confuse** the model )
- More observations are good for model training but more number of features confuses the model.
- Each feature should be independent.
- Remove **multicollinear** data ( e.g DOB and age can express each other so we can remove one of them )

### 5. Ensembling 
- **Combine** predictions from multiple separate models.
- Train multiple **weak** learners to make them a single **strong** model.
- **Bagging** trains multiple `individual` weak learners in **parallel**.
- **Boosting** trains multiple `weak` learners in **sequence** ( Improving in each steps learning from the mistakes of previous models ) 

### 6. Reduce Layers ( Deep Learning )
- **Removing layers** or **Elements** in the **hidden layers**.

### 7. Dropout Layers ( Deep Learning )
- Randomly `drop` certain features by setting them to `Zero` ( Fully Connected Layer )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
