<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

### Elite Data Science Primer

<h3><a href='#eda'>Exploratory Data Analysis</a> ( EDA )&nbsp; |&nbsp; <a href='#clean'>Data Cleaning</a>&nbsp; |&nbsp; <a href='#fe'>Feature Engineering</a></h3>

<h2 name='eda'>1. Exploratory Data Analysis</h2>

> Extract Information and **Capture Meaningful Insights** from the Dataset is **Exploratory Data Analysis**

### Know about the Data Set | Statistical Information | Summary of Data

1. Hint for **Data Cleaning**
2. Idea for **Feature Engineering**
3. **Data Visualization** to Discover **Hidden Patterns** and **Relations** | Spot **Anomalies** | Detect **Outlier** ( **Five Number Summary** | **IQR** )
4. **Scatter Plot**, **Histogram** and **Boxplot** for **Continuous** Variables ( **Outliers**, **Correlation**, **Measure of Spread** and **Central Tendency** )
5. **Bar** Plot to know about **Categorical** Variables | **Histogram** to understand **Distribution** of Data | **Heatmap** ( **Correlation** )

### Ask Questions to Data 
- How many **Observations** ? ( **Rows** )
- How many **Features** ? ( **Columns** )
- **Data Types** of the Features ? ( **Categorical** or **Numeric** )
- **Target Variable** in the Data Set ?
- Whether Data set is **Balanced** or **Imbalanced** ?
- Do the Values on the Right **Scale** ? or needs ( **Transformation** | **Normalization** | **Standardization** )
- Identify **Missing** Data | Reason for Missing Data
- Plot **Numerical Distributions** ( Detect **Outliers**, `Boxplot`, `Scatter`, `Histogram` )
- Plot **Categorical Data** ( `Bar Chart` | **Frequency** of Data | Combine **Sparse** Classes ) 
- Find **Correlations** ( `Heatmaps` )
- **Analysis** : **Univariate** ( One Variable ) | **Bivariate** ( Two Variables ) | **Multivariate** ( More than Two Variables )

<h2 name='clean'>2. Data Cleaning</h2>

> Better Data > Fancy Algorithm

### What ? | Why ? | How ?

- Remove Irrelevant | Incorrect | Incomplete | Improper | Duplicate | Inconsistent | Outdated | Insecure | Unformatted Data ( Filter )
- Fix Typo Error ( Inconsistent Capitalization ) Mislabelled Classes ( 'home' and 'Home' is Same )
- Filter Outliers by Setting Filter or Replace with some Relevant Value ( Mean, Median or Mode )
- Convert Data from One Format to Standard Format
- If Data is Stored in Multiple CSV Files, Combine CSV Data into Single Data Frame
- Fill | Impute | Drop | Handle Missing Data ( Add 'Missing' label in Categorical, Set Flag as 0 in Continuous )
- Split | Merge | Extract Column ( s ) or Row ( s )
- Create `New` Relevant Feature from Existing One

### Benefits of Data Cleaning
- Improve **Data Quality**
- **Save** Time and Increase Overall Productivity
- Improve **Decision Making**
- Boost **Business**
- Minimize **Compliance** ( Laws | Requirements | Rules | Regulations | Standard | Policies | Governance | Transparency ) Risk

<h2 name='fe'>3. Feature Engineering</h2>

> In EDA we only **Identify** and in Feature Engineering and Data Cleaning we Actually **Fix** the Problems Identified

- Feature Engineering is Performed after complete `EDA`
- Make Data Ready for **Machine Learning Algorithms**
- Use `Domain Knowledge` of Data to Create **Features** and **Variables** to use in **Machine Learning**
- Improve Machine Learning **Model Performance**
- Remove `Unused` Features
- Handle `Date` and `Time` Features
- Handle `Missing` Data   
- Handle `Categorical` Data ( Categorical to Numeric | Grouping Sparse Data | Create Dummy )

> Handling **Missing Data** | Encoding **Categorical Variables** | **Variable Transformation** | **Create New Features**

### 1. Handling Missing Data
- **Drop** ( Particular **Row** | Entire **Columns** )
- **Impute** ( Mean | Median | Mode ) ( `Univariate` )
- **Flag** ( Continuous : 1 or 0 | Categorical : 'Missing' ) 
- **Predict** from Existing Data ( `Multivariate` )

### 2. Categorical Encoding
- **Label** Encoding ( `Ordinal` )
- **One Hot** Encoding | Dummy Encoding ( `Nominal` ) 

### 3. Variable Transformation
- Create **Normal Distribution**
- Logarithmic ( log ( x ) ) | Exponential ( x <sup> n </sup> ) | Square root ( sqrt ( x ) ) | Reciprocal ( 1 / x )

### 4. Discretization
- **Sorting** Value of Variables in **Bins** or **Intervals** ( **Buckets** )
- Equal Width Discretization
- Equal Frequency Discretization
- Decision Tree Descretization ( Tree **Splits** Equally )

### 5. Handle Outliers
- **Visualize** by using **Boxplots**, **Histogram** and **Bar Graphs**
- **Filter** or **Trim** Data set 
- **Remove** Outliers 
- Setup a **Filter** and **Trim** Data Set
- **Change** | **Replace** the Outlier 

### 6. Feature Scaling
- Standardization  ( x - **mean** ( x ) ) / **std** ( x ) 
- Min Max Rescaling ( 0 - 1 )
- Maximum Absolute Scaling : Dividing Each value with Maximum Value ( 0 - 1 )
- Robust Scaling : Dividing by **IQR** ( **Q3** - **Q1** )
- Mean Normalization : ( x - mean ) / ( max - min )

### 7. Date and Time Engineering 
- Parse **Date** and **Time** so that we can extract Year, Month, Day, Week and Perform any Operation. 

### 8. Feature Creation
- Create New Meaningful **Feature** from the Existing Features. ( Aggregating | Arithmetic Calculation )

### 9. Aggregation of Transaction Data
- **Total** of Sales 
- **Profit** or **Loss** of the Day 
- Total Amount **Credited** or **Debited** for the Day 

# Machine Learning Pipeline
- Help to **Automate** Machine Learning **Workflows**.
- Pipeline **Chain** together Multiple Steps to **Train** the Model, Output of each Step is used as Input to the Next Step.
- Pipelines are **Cyclic**, contains **Iterative** Steps to Continuously Improve the **Accuracy** of **Algorithm** and makes Model **Scalable**.
- The Learning Algorithm Finds **Patterns** in the **Training Data** that Maps the **Features** to the **Target** and Create a ML Model.

### 1. Data 
- Data Collection
- Data Preprocessing
- Exploratory Data Analysis
- Data Preprocessing

### 2. Data Preparation
- Data Cleaning
- Feature Engineering ( Deal with Numerical Data + Handle Categorical Data )
- Data Visualization ( Find Hidden Patterns )
- Feature Extraction | Feature Selection
- Transforation, Normalization or Standardization 

### 3. Data Modeling 
- Split the Data into Train Set and Test Set 
- Train the Model on Train Set
- Tune the Model on Validate Set
- Evaluate the Model on Test Set

### 4. Deployment
- Integrate with Application or Website
- Fine Tuning
- Real Life Prediction or Classifications

### Small Pipelines 
- `make_pipeline`( Imputer, Column Transformer, Estimator ) | Estimator : Classifier or Regressor.
- `make_column_transformer()` : We can apply different **Encoder** on different Column **Individually** based on Requirement )
- pipeline can be directly used for Training using `fit()` and it can even Predict using `predict()`

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
