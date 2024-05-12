<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **Imbalanced dataset**

### **Class labels of the target variable should be balanced otherwise it predicts a biased output.**

- e.g. Flower Species 150 : 50 Setosa, 50 Verginica and 50 Versicolor

### Here, Observations, Samples, and Rows represent the same thing.

### **1. Up | Oversampling minority class** 

### **(SMOTE: Synthetic minority oversampling technique)**
- Randomly duplicate the minority class samples to **reinforce** the learning of data.
- Resample minority class by setting the number of samples to match with the majority class.
- Combine the upsampled minority samples with the original majority samples (data frame)

### **2. Down | Under sampling majority class**
- Randomly drop the majority class samples (Resampling **without** replacement)
- Resample the majority class by setting the number of samples to match with minority class.
- Combine the downsampled majority samples with the original minority samples (data frame)

### **3. Evaluation Metric: F1 Score**
- F1 Score: Falls between 0 and 1 (Harmonic mean of recall and precision)
- F1 Score keeps the balance between recall and precision.

### **4. Stratified K Fold Cross Validation**
- Samples containing an equal proportion of each class label to train the model.  

### **5. Random Forest handles imbalanced dataset**
- Parameter **class_weights** (We can specify a higher weight for the minority class)

### **6. Collect more data for Minority Class**

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
