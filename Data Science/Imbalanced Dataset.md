<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Imbalanced dataset**

### **Class labels of the target variable should be balanced otherwise it predicts a biased output.**

- e.g. Flower Species 150 : 50 Setosa, 50 Verginica and 50 Versicolor

**Here, observations, samples, and rows represent the same thing.**

### **1. Up | Oversampling minority class** 

### **(SMOTE: Synthetic minority oversampling technique)**
- Randomly duplicate the minority class samples to **reinforce** the learning of data.
- Resample minority class by setting the number of samples to match with the majority class.
- Combine the upsampled minority samples with the original majority samples.

### **2. Down | Under sampling majority class**
- Randomly remove/drop the majority class samples to make the class distribution balanced.
- Resample the majority class by setting the number of samples to match with minority class.
- Combine the downsampled majority samples with the original minority samples.

### **3. Evaluation Metric**
- Precision, Recall | True Positive Rate (TPR), and F1 Score are better metrics for imbalanced dataset.
- **F1 Score:** Harmonic mean of recall and precision (keeps the balance between recall and precision)

### **4. Cross Validation**
- **Stratified K Fold Cross Validation:** Samples with an equal proportion of each class label to train the model.  

### **5. Algorithms less sensitive to class imbalance:**
- Random Forest and KNN can perform well with imbalanced data.
- RF combines predictions from multiple models trained on different resampled versions of data.
- Parameter **class_weights** (We can specify a higher weight for the minority class)
- Force the model to pay more attention while learning from the minority class samples.

### **6. Collect more data for Minority Class**

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
