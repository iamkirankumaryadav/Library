<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Feature Engineering
 
 FE is the art of transforming raw data into features that are most important for ML models.

### **Data Wrangling:**
- **Selection:** Choosing the most important features from your dataset. Irrelevant features can confuse the ML models.
- **Cleaning:** Data often contains inconsistencies/errors. FE involves cleaning the data to ensure its accuracy.

### **Feature Creation:**
- ML models will not accept the data in raw format (It should be numerical)
- FE involved creating new features from the existing ones.
- **Combination:** Combining existing features to create one new feature.
- **Derivation:** Deriving new features from calculations on existing ones.
- **Binning:** Grouping continuous features into categories (bins) can be useful. e.g. Income can be binned into low, medium, and high categories.

### **Feature Transformation:**
- Transforming existing features can improve their usability from ML models.
- **Scaling:** Features with different scales can affect/dominate the model learning. Scaling ensures all features are in a similar range.
- **Encoding:** Categorical features need to be converted into numerical values that the model can understand. (OHE and label encoding)

### **Feature Engineering Importance:**

1. Improve model performance:
- Helps in selecting and transforming relevant features from the raw data.
- Which can significantly improve the accuracy and generalize the ML models.
- The model can focus on the most important features by removing redundant or irrelevant features.
- Leading to better prediction performance.

2. Reduces Noise and Dimensionality:
- Raw data often contains noise and irrelevant information that can confuse ML algorithms.
- Reduce noise and dimensionality by eliminating redundant or irrelevant features.
- Improve the signal-to-noise ratio and make the data more suitable for ML tasks.

3. Enhances Interpretability:
- Make it easier to understand how the features are influencing the model's predictions.

### Common Feature Engineering Techniques

1. Data Cleaning and Preprocessing:
- Data cleaning involves identifying and correcting errors or inconsistencies in the data. 
- Preprocessing involves normalizing and scaling the data to ensure consistent representation.
- Ensure the data is in a suitable format for further feature engineering and ML algorithms.

2. Feature Selection:
- Identifying and selecting the most relevant and informative features from the data.

3. Feature Transformation:
- Feature transformation involves `modifying` or `transforming` the features to improve their suitability for machine learning algorithms.
- Common transformation techniques include `normalization`, `scaling`, and `encoding` categorical variables.

4. Feature Creation:
- Feature creation involves deriving new features from existing data.
- This can be done using techniques such as aggregation, pivot table, stacking, etc.
- Applying domain knowledge to generate new features.

5. Feature Interaction Analysis:
- Identifying and understanding how different features interact with each other to influence the target variable.
- This information can be used to create new features or improve existing ones.

Feature engineering is an `iterative process` that requires careful consideration of the data, the machine learning algorithm, and the specific application. 

By applying appropriate feature engineering techniques, data scientists can significantly improve the ML models.
