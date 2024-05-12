<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Steps of Machine Learning

### **1. Data Collection** 
- Identify and acquire data
- **Supervised:** Labelled historical data to train and evaluate the model. 
- **Unsupervised:** Unlabelled data to discover the relationships and patterns.
- **Reinforcement:** The data that helps the agent to learn which actions yield the most rewards.
- The data used for training should be accurate and relevant to get accurate predictions.
- Quantity of data should be appropriate, less data will be insufficient to train data with all information.
- Large observations of data with balanced class distribution will be perfect for training.
- Large number of features will create confusion at the time of training (Curse of dimensionality)
- Variability in the data also plays an important role in training.
- The data set should contain a good mixture of observations which explains the variability very well.
- The data should have a good balance for bias and variance. It prevents overfitting.

### **2. Data Exploration** 
- Explore and understand data (Exploratory Data Analysis). Describing and visualizing data.
- Calculating central tendency and dispersion (spread and skewness) of the dataset. 
- Visualizing the data to get the idea (A picture is worth a thousand words)
- Number of **rows** and **columns**, **distribution** of dataset, **statistical** informations, **data types** and **feature importance**.
- Identify **duplicates**, **missing values**, **inconsistency** and **outliers** in data.
- High dimensionality means higher computational complexity, high training time, complex understanding and complex visualisation.
- Reducing dimensions without losing information also helps to reduce complexity.
- Sparsity and density (Data with 20% missing data is known to be 20% sparse and 80% dense) 
- Visualization helps to do comparisons using boxplots, multiple bar charts, and multiple line charts.
- Visualization helps to find patterns, relationships and correlations using line charts.
- Visualization helps to get the distribution of data and identify outliers using histograms.
- Visualization for compositions and contribution of data using stacked bar charts and pie charts. 

### **3. Data Preparation** 
- **Cleaning** and **preparing** data for training. 
- Resolving data quality issues such as **missing** data, **noisy** data, **outlier** data and class **imbalance**.
- Transforming the structure of data by **standardization** or **normalization**.
- Normalization: Scaling data to fall within a normal range.
- Standardization (Z Score Normalization): Mean = 0 and Std = 1.
- If we need lower bound: 0 and upper bound: 1, then use **min-max normalization**.
- Balancing the bias and variance by solving underfitting and overfitting.
- Reducing the number of **rows** and **columns** (Feature engineering).
- Impute [missing data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Missing%20Data.md).
- Resolve [outliers](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Outliers.md).
- Encode [categorical data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Categorical.md).
- Handle [imbalanced data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Imbalanced%20Dataset.md).
- Sampling: Selecting a subset of data for training.
- Random sampling without replacement (No repetition of data)
- Random sampling with replacement (Repetition of same data): Bootstrapping.
- Stratified Sampling: Subset with equal class distribution.
- Dimensionality Reduction: Reduction of features, reduce complexity and training time of data.
- Feature selection: Identify **minimal** set of features needed to build a good model (Creates subset, preserves original)
- Feature extraction: Transform data from high dimensionality to low dimensionality (Create new features)

### **4. Data Modeling** 
- Choosing and applying correct machine learning algorithms to work well with data.
- Few of the algorithms can be used for both prediction and classification.
- Few algorithms are made especially for regressions only.
- Few algorithms are based on distance calculations like Linear Regression, SVM, KNN and K Mean.
- Few algorithms are based on probability like Logistic Regression and Naive Bayes.
- Few algorithms are tree-based like Decision Trees and Ensemble Techniques (Bagging and Boosting)

### **5. Evaluation**

- Identify how well the created model is performing on the new unseen dataset.
- The goal is to predict a label or value with the least number of errors.
- 100% perfect accuracy is impossible.
- The dataset used for training and testing should be different (Without any data leakage)
- We apply different ways like Regularization, Cross Validation (Resampling) and Hyperparameter Tuning to improve accuracy. 
- We try to solve the **overfitting** and **underfitting** by adjusting **bias** and **variance**.
- Calculate different [**metrics**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Regression%20Metrics.md) to solve [overfitting](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Overfitting.md) problems.
- Iterative process to improve the **accuracy** and **performance** of model.

### **6. Actionable Insight**
- Identify what to do based on results. Acceptable or need to be improved.
- Decide whether to deploy or not to production.
