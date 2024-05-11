<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Feature Engineering
 
 FE is all about transforming raw data into features (variables) that are most important for the ML models.

### **Data Wrangling:**
- **Selection:** Choosing the most important features from your dataset. Irrelevant features can confuse the ML models.
- **Cleaning:** Data often contains inconsistencies/errors/noise. FE involves cleaning the data to ensure the ML model's accuracy.
- **Dimensions:** Reduce dimensions to simplify the data, it helps in proper understanding and visualization of the data.

### **Feature Creation:**
- FE involves creating new features from the existing ones which can contribute to better learning.
- Well-engineered features can significantly improve the accuracy and efficiency of ML models.
- **Combination:** Combining existing features to create one new feature.
- **Derivation:** Deriving new features from calculations on existing ones.
- **Binning:** Grouping continuous features into categories (bins) e.g. Income can be binned into low, medium, and high categories.

### **Feature Transformation:**
- Transforming existing features can improve their usability from ML models.
- **Scaling:** Features with different scales can affect/dominate the model learning. Scaling ensures all features are in a similar range.
- **Encoding:** Categorical features need to be converted into numerical values that the model can understand. (OHE and label encoding)

### **Importance:**
- By providing more informative features, models can learn faster and require less training data.
- Make it easier to understand how the features are influencing the model's predictions.
- FE can help you understand which features are most important for your model's predictions.

FE is an iterative process that requires careful consideration of the data, the ML algorithm, and the specific application. 
