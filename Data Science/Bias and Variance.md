<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# **Bias | Variance | Underfitting | Overfitting**

Bias | Variance
:--- | :---
Bias: Error on train set | Variance: Error on test set
High Bias (Model is not trained well) | High Variance (Prediction is not good for new unseen data)
High Bias (Creates simple model) | High Variance (Creates complicated model)
Simple models make simplified assumptions while learning | Complicated models learn data with noise
Simple models do not capture **hidden** patterns and relations properly | Model **memorize** patterns and relations + noise + error
Low Bias algorithms (Decision Tree, KNN, SVM) | Low Variance algorithms (Regression, LDA)
High Bias algorithm (Regression) | High Variance algorithms (Decision Tree, KNN, SVM) 

- Error/Residual = Predicted - Actual (Difference between the expected/predicted value and actual value)
- Linear algorithms **learn fast** which often leads to high bias
- Simple the algorithm, the more bias it will introduce (Underfitting)

### **How to reduce Bias?**
- Cross-validation, resampling and ensemble techniques can prevent Bias as well as Variance.
- `K Fold Cross Validations` and `Resampling` | Split the dataset into `K` samples and each set is used as a testing set.
- `Bootstrapping` and `Boosting` | Iteratively `Resampling` a dataset with `replacement`

### **Bias Variance Trade-Off**

- Bias and Variance are inversely proportional to each other.
- A model with low bias will tend to have high variance
- A model with low variance will tend to have a high bias
- Increasing bias decreases variance and increasing variance decreases bias
- ML aims to find the correct balance i.e. low bias and low variance

### **Underfitting: High Bias + Low Variance (Simple Model)**
- High Bias: High error on train dataset (Model is not trained properly)
- Low Variance: Low error on test dataset (Generalized: model can predict a little close to the actual value)
- The model fits the data enough but also captures noise and error at the time of training (Low accuracy)

### **Overfitting: Low Bias + High Variance (Complex Model)**
- **Low Bias:** Low error on train data (Model is **trained** very well including noise)
- **High Variance:** High error on test data (Performs badly on the new unseen data)
- When a massive amount of data trains a model, it tends to learn from noise and inaccurate data.
- Random error and noise get added | Complex model | Too many features relative to the number of observations.
- Poor **predictive** performance | Do not **generalize** well on the **new unseen data**.
- The difference between the prediction on the **new unseen data point** and the **actual data point** is high (High Variance)
- The model tries to fit the training data so closely that it does not **generalize** well to **new unseen data**.

Bias and Variance help us improve the data fitting and training process resulting in more **accurate models**.

### **Total Error = Bias + Variance + Irreducible Error (Noise)**

### **Good Fit Model (Low Bias + Low Variance)**
- Prediction is **close** to the actual
- **Captures** Less noise and error at the time of **training** (Low Bias)
- Generalized enough to work with any **new unseen data** (Low Variance) 

### How to obtain an optimal tradeoff?

1. **Hyperparameter Tuning:**
- Choosing the right set of optimal hyperparameters for training the model.

2. **Regularization**
- L1 and L2 techniques are used to reduce overfitting by discouraging complex models.
- Adding constraints to the model training to prevent the model from overfitting the training data. 

3. **Resampling and Cross-Validation**
- K fold (Balanced dataset) and Stratified K fold (Unbalanced dataset) Cross Validation.

4. **Ensemble Techniques:**
- Combining multiple weak models into a single model.
- Reduces both bias and variance by averaging out the predictions of the individual models.

5. **Data Augmentation:**
- Artificially increasing the size of the training dataset by creating new data points from existing ones.
- This can help the model learn more generalized patterns and reduce overfitting.

6. **Model Selection:**
- Evaluating different models with different complexities and choosing the one that generalizes best to unseen data.

7. **Feature Engineering:**
- Selecting and transforming the features used to train the model. 
- Help reduce bias and variance by providing the model with more relevant information.

# **Bias**

### Different types of bias in ML models.

Bias can lead to the model making biased predictions.

### **1. Data Bias:** 
- Occurs when the data that is used to train the model is not representative of the real world.

### **2. Sampling Bias:**
- Occurs when the data that is used to train the model is not randomly sampled from the population.

### **3. Label Bias:**
- Occurs when the labels on the data are not accurate.

### **4. Algorithmic Bias:**
- Occurs when the algorithm that is used to train the model is biased.
- The algorithm is designed to favour a particular group of people or if the algorithm is not properly trained.

### **5. Interpretation Bias:**
- Occurs when the results of the model are interpreted in a biased way.
- This can happen if the people interpreting the results are not aware of the biases in the model.

### **6. Design Bias:**
- Occurs when the algorithm is designed to favour a particular group of people.

### **7. Training Bias:**
- Occurs when the algorithm is trained on data that is biased.
- This can happen if the data is collected from a specific group of people or if the data is not properly cleaned.

### **8. Evaluation Bias:**
- Occurs when the algorithm is evaluated on data that is biased.

## **How to prevent from Bias?**

### **1. Use diverse dataset:**
- The dataset should represent all of the different groups of people that the model will be used to predict.

### **2. Randomly sample the data:**
- Selecting a random sample of data helps to reduce the impact of any bias that is present in the data.

### **3. Clean the data:**
- Before you train the model, you should clean the data. This means removing any outliers or errors from the data.

### **4. Use the correct algorithm:**
- Fair algorithms should be used to train the model. A correct model will reduce the impact of bias in the model.

### **5. Interpret the results carefully:**
- Don't make biased assumptions. Always be aware of the limitations of the respective model.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
