# Steps of Machine Learning

### 1. Data Collection 

- **Identify** and **acquire** data.
- `Supervised` : **Labelled** historical data to `train` and `evaluate` the model. 
- `Unsupervised` : **Unlabelled** data to discover the **relationships** and **patterns**.
- `Reinforcement` : The data which helps **agent** to learn which actions yield the most **rewards**.
- The data used for training should be **accurate** and **relevant** in order to get the accurate **predictions**.
- `Quantity` of data should be appropriate, less data will be insufficient to train data with all informations.
- Large **observations** of data with **balanced class** distribution will be perfect for training.
- Large number of **features** will create confusion at the time of training ( **Curse of dimensionality** )
- `Variability` in the data also plays an important role for training.
- The data set should contain a good mixture of observations which explains the **variability** very well.
- The data should have good balance for **bias** and **variance**.

### 2. Data Exploration : 

- **Explore** and **understand** data ( Exploratory Data Analysis )
- `Describing` and `Visualizing` data.
- Calculating `central tendency` and `dispersion` ( spread and skewness ) of dataset. 
- `Visualizing` the data to get the idea ( A picture is worth a thousand words )
- Number of **rows** and **columns**, **distribution** of dataset, **statistical** informations, **data types** and **feature importance**.
- Identify **duplicates**, **missing**, **inconsistency** and **outliers** in data.
- High dimensionality means higher computational complexity.
- Reducing dimensions without loosing information also helps to reduce complexity.
- **Sparsity** and **Density** ( Data with 20% missing data is known to be 20% sparse and 80% dense ) 
- Visualization help to do **comparisons** using **boxplots**, multiple **bar charts**, and multiple **line charts**.
- Visualization helps to find **patterns**, **relationships** and **correlations** using **line chart**.
- Visualization helps to get the `distribution` of data and identify **outliers** using **histogram**.
- Visualization for **compositions** and **contribution** of data using **stacked bar charts** and **pie charts**. 

### 3. Data Preparation 

- **Cleaning** and **preparing** data for training. 
- `Resolving` data quality issues such as **missing** data, **noisy** data, **outlier** data and class **imbalance**.
- `Transforming` the structure of data by **standardization** or **normalization**.
- `Normalization` : Scaling data to fall within a small or specified range.
- `Standardization` ( Z Score Normalization ) : Mean = 0 and Std = 1.
- If we need lower bound : `0` and upper bound : `1`, then use **min max normalization**.
- If there is outlier in the data the most suitable approach is **log transformation**.
- Balancing the **bias** and **variance** by solving **underfitting** and **overfitting**.
- Reducing the number of **rows** and **columns** ( `Feature engineering` )
- `Impute` [missing data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Missing%20Data.md) 
- `Resolve` [outliers](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Outliers.md) 
- `Encode` [categorical data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Categorical.md) 
- `Handle` [imbalanced data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Imbalanced%20Dataset.md)
- `Sampling` :  Selecting a subset of data for training.
- Random sampling without replacement ( no repetition )
- Random sampling with replacement ( repetition : selecting same again ) : Bootstraping
- `Stratified` sampling : Subset with equal class distribution.
- `Dimensionality reduction` : Reduction of features, reduce complexity and training time of data.
- `Feature selection` : Identify **minimal** set of features needed to build a good model ( Creates subset )
- `Feature extraction` : Transform data from high dimensionality to low dimensionality ( Create new features )

### 4. Data modeling 

- Choosing and applying correct machine learning algorithm to work well with data.
- Few of the algorithms can be used for classification as well as prediction.
- Few algorithms are made specially for regressions only.
- Few algorithms are based on `distance` calculations like KNN and K Mean.
- Few algorithms are based on `probability` like logistic regression and Naive Bayes.
- Few algorithms are `tree` based like Decision tree, Bagged trees, Random Forest and Boosted trees.

### 5. Evaluation

- Identify how well the created model is performing on the new unknown dataset.
- Goal is to predict a label or value with least number of `error`
- `100%` perfect accuracy is not possible.
- Data set used for training and testing should be different ( Without any data leakage )
- We apply different ways like **regularization**, **resampling**, **cross validation** and **tuning** to improve accuracy. 
- We try to solve the **overfitting** and **underfitting** by adjusting **bias** and **variance**.
- Calculate different [**metrics**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Regression%20Metrics.md) to solve [overfitting](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Overfitting.md) problems.
- Iterative process to improve the **accuracy** and **performance** of model.

### 6. Actionable Insight

- Identify what to do based on results.
- Make decision whether to deploy or not to production.
