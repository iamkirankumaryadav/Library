<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

### Imbalanced Data Set

- **Class Labels** should be `Balanced` otherwise it Predicts a **Biased Output** or Classify Biased to only one Class Label.

### A. Stratified Sampling
- Create a Sample containing `Equal` number of Each `Class Labels` to Train the Model

### 1. Up Sample or Over Sampling Minority Class | Sampling with Replacement ( SMOTE : Synthetic Minority Oversampling Technique )
- Randomly **Duplicate** the Minority Class Observations in order to **Reinforce** the Learning of Data.
- Resample Minority Class with Replacement, Setting Number of Samples to Match with Majority Class.
- Combine the Up Sampled Data with Orignal Majority Class Dataframe.

### 2. Down Sample or Under Sampling Majority Class | Sampling Without Replacement 
- Randomly **Removing** Majority Class Observations ( Resampling **without** Replacement )
- Resample Majority Class `without` Replacement, Setting Number of Samples to Match with Minority Class.
- Combine the Down Sampled Data with Orignal Minority Class Dataframe.

### B. Change Evaluation Metrics for Better Performance
- Choosing Right Evaluation Metrics is Important
- **F1 Score** : Number between 0 and 1 ( Harmonic Mean of Recall and Precision )
- **Precision** : Focus on **Positive Predictions**
- **Recall** ( TPR ) : Focus on **Positive Predictions**
- **F1 Score** is a **Harmonic Mean** of Recall and Precision ( Keep a Balance between Recall and Precision for the **Classifier** )

### C. Use Cross Validation 
- Use **Stratified K Fold Cross Validation** with Equal Class Labels to Train the Model

### D. Use Algorithms that Supports Imbalanced Data Set ( Ensembled Methods )

### 1. Random Forest Classifier 
- Parameter **class_weights** : We can Specify a Higher Weight for the **Minority Class**.

### E. Manual Methods
- Collect more Data for Minority Class.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
