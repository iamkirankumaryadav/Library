<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

### Imbalanced dataset

- **Class** labels should be `balanced` otherwise it predicts a **biased output**.

### A. Stratified sampling
- Sample containing `equal` proportion of each `class labels` to train the model ( 50 Red, 50 Blue and 50 Green )

### 1. Up | Over sampling minority class | Sampling with replacement 

### ( SMOTE : Synthetic minority oversampling technique )

- Randomly **duplicate** the minority class observations in order to **reinforce** the learning of data.
- Resample minority class with `replacement`, setting number of samples to match with `majority` class.
- Combine the `up sampled` data with orignal `majority` class data ( dataframe )

### 2. Down | Under sampling majority class | Sampling without replacement 
- Randomly **drop** majority class observations ( Resampling **without** replacement )
- Resample majority class `without` replacement, setting number of samples to match with `minority` class.
- Combine the `down sampled` data with orignal `minority` class data ( daatframe )

### B. Change evaluation metrics for better performance
- Choosing right evaluation `metrics` is important.
- `F1 Score` : Number between `0` and `1` ( Harmonic mean of `recall` and `precision` )
- `F1 Score` is a **harmonic mean** of `Recall` and `Precision` ( Keep balance between `recall` and `precision` )

### C. Use cross validation 
- Use `stratified k fold cross validation` with equally distributed class labels to train the model.

### D. Use algorithms that supports imbalanced data set ( Ensembled methods )

Random forest classifier : Parameter `class_weights` ( We can specify a higher weight for the **minority** class )

### E. Collect more data for minority class.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
