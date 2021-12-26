<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# `Imbalanced dataset`

### `Class labels` of target should be `balanced` otherwise it predicts a `biased` output.

- e.g. Flower Species 150 : 50 Setosa, 50 Verginica and 50 Versicolor

### 1. Up | Over sampling minority class 

### ( SMOTE : Synthetic minority oversampling technique )

- Randomly **duplicate** the `minority` class observations in order to **reinforce** the learning of data.
- Resample minority class by setting number of samples to match with `majority` class.
- Combine the `up sampled` observations with orignal `majority` observations ( dataframe )

### 2. Down | Under sampling majority class
- Randomly **drop** the `majority` class observations ( Resampling **without** replacement )
- Resample majority class by setting number of samples to match with `minority` class.
- Combine the `down sampled` observations with orignal `minority` observations ( daatframe )

### 3. Evaluation Metric :  `F1 Score`
- `F1 Score` : Number between `0` and `1` ( Harmonic mean of `recall` and `precision` )
- `F1 Score` keeps balance between `recall` and `precision`

### 4. `Stratified K Fold Cross Validation`
- Sample containing `equal` proportion of each `class labels` to train the model.  

### 5. `Random Forest` supports imbalanced data set

`Random forest` : Parameter `class_weights` ( We can specify a higher weight for the **minority** class )

### 6. `Collect` more data for `Minority Class`

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
