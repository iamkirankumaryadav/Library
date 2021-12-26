<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# `Overfitting` : `Low Bias + High Variance`

### `Low Bias` : Low error on `train` set 

- Simple model.
- Model **memorize** the data including **noise** and **error** with very good **accuracy** for **training set**.

### `High Variance` : High error on `test` set
- Model has just memorized the data, it was not able to learn the `hidden patterns` and `relationships`
- Model performs **better** on **training** dataset but it does not **generalize** well on the **new unseen** test set.

### `Identify` Overfitting 

### Train Test Split | Observe Accuracy ( Score )
- `Split` the **dataset** into `train` and `test` set.
- Check whether the trained model `generalizes` well on **new unseen** test set. 
- `Accuracy` of `train` set : `model.score(X_train, y_train)`
- `Accuracy` of `test` set : `model.score(X_test, y_test)`
- If `accuracy` of `train` set is better and `accuracy` on `test` set is worst ( `Overfitting` )

### `Prevent` from Overfitting

### 1. Collect more data for training.

### 2. Apply [Regularization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md) 

- Slope | Coefficient | Weight | Gradient ( All are same )
- Lasso ( `L1` ) : Sum of `absolute` of `slope` ( **Coefficient** to exactly 0 )
- **Simplify** the model + **feature selection** ( Select only **important** features )
- Ridge ( `L2` ) : Sum of `square` of `slope` ( **Penalize** slope values towards 0 )
- Able to learn **complex data patterns** | Decreases the **complexity** of model.

### 3. Apply [Cross Validation](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Cross%20Validation.md)
- Measure how well each **iteration** of the model performs.
- Until certain iterations, **new iterations** improves the accuracy of model.
- After some point the **model's ability** to **generalize** gets weak and model starts **overfitting**.

### 4. Feature Selection

- More observations are good for model training but more number of features confuses the model.
- Select only **important** features ( Large number of features can **confuse** the model )
- Each `feature` and `observation` should be `independent` of each other.
- Remove **multicollinear** data ( e.g DOB and age can express each other so we can remove one of them )

### 5. [Ensembling](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md) 
- **Combine** predictions from multiple `weak` models into single strong accurate predicting model.
- Train multiple **weak** learners to make them a single **strong** accurate predicting model.
- **Bagging** trains multiple `individual` weak learners ( Decision tree ) in **parallel**.
- **Boosting** trains multiple `weak` learners in **sequence** ( Improving in each steps learning from the mistakes of previous models ) 

### 6. Reduce Layers ( Deep Learning )
- **Removing layers** or **elements** in the **hidden layers**.

### 7. Dropout Layers ( Deep Learning )
- Randomly `drop` certain features by setting them to `0` ( Fully Connected Layer )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
