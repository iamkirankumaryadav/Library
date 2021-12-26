<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# `Imbalanced dataset`

`Class labels` of target should be `balanced` otherwise it predicts a **biased output**.

`Stratified sampling` : Sample containing `equal` proportion of each `class labels` to train the model.  
- e.g. Flower Species 150 : 50 Setosa, 50 Verginica and 50 Versicolor

### 1. Up | Over sampling minority class | Sampling with replacement 

### ( SMOTE : Synthetic minority oversampling technique )

- Randomly **duplicate** the `minority` class observations in order to **reinforce** the learning of data.
- Resample minority class with `replacement`, setting number of samples to match with `majority` class.
- Combine the `up sampled` data with orignal `majority` class data ( dataframe )

### 2. Down | Under sampling majority class | Sampling without replacement 
- Randomly **drop** the `majority` class observations ( Resampling **without** replacement )
- Resample majority class `without` replacement, setting number of samples to match with `minority` class.
- Combine the `down sampled` data with orignal `minority` class data ( daatframe )

### 3. Choose right evaluation metric
- `F1 Score` : Number between `0` and `1` ( Harmonic mean of `recall` and `precision` )
- `F1 Score` keeps balance between `recall` and `precision`

### 4. Use cross validation 
- Use `stratified k fold cross validation` with equally distributed class labels to train the model.

### 5. Use algorithms that supports imbalanced data set ( Ensembled methods )

`Random forest` : Parameter `class_weights` ( We can specify a higher weight for the **minority** class )

### 6. Collect more data for minority class.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
