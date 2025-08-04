<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Imbalanced dataset**

### Class labels of the target variable should be balanced otherwise, the model may produce biased predictions.

- e.g. Flower Species 150 : 50 Setosa, 50 Verginica and 50 Versicolor

**Here, observations, samples, and rows represent the same thing.**

### **1. Up | Oversampling minority class** 

### **(SMOTE: Synthetic minority oversampling technique)**
- Duplicate minority class samples randomly to reinforce learning.
- Resample the minority class to match the number of samples in the majority class.
- Combine the upsampled minority class with the original majority class.

### **2. Down | Under sampling majority class**
- Remove/drop some majority class samples to balance the distribution.
- Resample the majority class to match the number of minority class samples.
- Combine the downsampled majority class with the original minority class.

### **3. Evaluation Metric**
- Precision, Recall, True Positive Rate (TPR), and F1 Score are better metrics for imbalanced datasets.
- F1 Score: The harmonic mean of recall and precision, balancing both metrics.

### **4. Cross Validation**
- Stratified K-Fold Cross Validation: Ensures each fold has the same proportion of class labels for training.

### **5. Algorithms less sensitive to class imbalance:**
- Random Forest and KNN can perform well with imbalanced data.
- Random Forest combines predictions from multiple models trained on different resampled datasets.
- Use the class_weights parameter to assign higher weight to the minority class.
- This forces the model to pay more attention to learning from minority class samples.

### **6. Collect more data for Minority Class**

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
