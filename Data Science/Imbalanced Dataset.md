<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

### Imbalanced Data Set

- **Class** labels should be `Balanced` otherwise it predicts a **Biased Output**.

### A. Stratified Sampling
- Create a sample containing `equal` proportion of each `class labels` to train the model ( 50 Red, 50 Blue and 50 Green )

### 1. Up | Over Sampling Minority Class | Sampling with Replacement 

### ( SMOTE : Synthetic Minority Oversampling Technique )

- Randomly **duplicate** the minority class observations in order to **reinforce** the learning of data.
- Resample minority class with `replacement`, Setting number of samples to match with `majority` class.
- Combine the `up sampled` data with orignal `majority` class data frame.

### 2. Down | Under Sampling Majority Class | Sampling Without Replacement 
- Randomly **drop** majority class observations ( Resampling **without** replacement )
- Resample majority class `without` replacement, Setting number of samples to match with `minority` class.
- Combine the `down sampled` data with orignal `minority` class data frame.

### B. Change Evaluation Metrics for Better Performance
- Choosing right evaluation metrics is important.
- `F1 Score` : Number between `0` and `1` ( Harmonic Mean of `Recall` and `Precision` )
- **Precision** : Focus on **Positive Predictions**
- **Recall** ( `TPR` ) : Focus on **Positive Predictions**
- **F1 Score** is a **Harmonic Mean** of `Recall` and `Precision` ( Keep a `Balance` between `Recall` and `Precision` for the **Classifier** )

### C. Use Cross Validation 
- Use `Stratified K Fold Cross Validation` with equal class labels to train the model.

### D. Use Algorithms that Supports Imbalanced Data Set ( Ensembled Methods )

### 1. Random Forest Classifier 
- Parameter `class_weights` : We can specify a higher weight for the **Minority Class**.

### E. Manual Methods
- Collect more data for `Minority` Class.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
