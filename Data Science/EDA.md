### **Exploratory Data Analysis**

`EDA` is a process of analyzing data sets to **summarize** their **characteristics**, using `statistics` and `data visualization` methods.

1. **EDA** is a most essential step in a data science projects and data analysis process.
2. **Data scientists** spend almost 70% of their work doing EDA of their dataset.
3. Discover patterns, spot anomalies, identify outliers, understand main characteristics, gain insights, test hypotheses, and check assumptions with summary **statistics** and **graphical representations**.
4. An iterative cycle that involves generating questions about the data, searching for answers by visualizing, transforming, and modeling the data, and using what is learned to refine or generate new questions.
5. **Graphical Analysis**: Visualizations and charts are used to visualize trends and patterns in the data.
6. **Statistical Analysis**: Measuring central tendency, spread, variability and distribution are used to analyze the data.
7. EDA helps to prepare the dataset for analysis, allows a ML model to predict, gives more accurate results, and helps to choose a better ML model.

### Steps:

#### 1. Importing Libraries and Loading Dataset:
- Import required **libraries**, **modules** and **submodules**.
- Load your dataset into a **DataFrame**.

```python
# Import Libraries:
import pandas as pd # For Data Manipulation
import matplotlib.pyplot as plt # For Data Visualization

# Load the data into a DataFrame:
df = pd.read_csv('dataset.csv')
```

#### 2. Data Exploration:
- Explore the basic characteristics of the dataset.
- Use functions `dtypes`, `info` and `describe` to get an initial understanding of the data.

```python
# Summary Information of Dataset:
df.info()

# Descriptive Statistics:
df.describe()
```  

#### 3. Dealing with Missing Values:
- Identify and handle missing values in the dataset.
- Use functions `isnull`, `sum`, `fillna` to detect missing values.
- Choose an appropriate strategy to deal with them.

```python
# Find missing values:
df.isna().sum()

# Handle missing values by imputation:
df.fillna(value, inplace=True)

# Handle missing values by removal:
df.dropna(inplace=True)
```

#### 4. Data Visualization:
- Create visual representation of the data to gain insights.
- Generate various plots, such as histograms, scatter plots, box plots and correlation matrix
- Libraries like Matplotlib, Seaborn or Plotly to create visuals.

```python
# Create Histogram:  
plt.hist(df['Height'], bins=10)
plt.xlabels('X axis label')
plt.ylabels('Y axis label')
plt.title('Histogram')
plt.show()
```
          
#### 5. Feature Engineering:
- Explore and create new features from the existing feature to enhance the predictive power of the data.
- FE involves transformation, scailing, binning and creating derived features based on domain knowledge.

```python
# Create new feature by binning an existing feature:
df['new_column'] = pd.cut(df['existing_column'], bins = [0, 10, 20, 30, 40])
```  

#### 6. Correlation Analysis:
- Examine the relationships between variables in the dataset.
- Calculate correlation coefficients and visualize them using heatmaps or correlation matrices.

```python
# Calculate Correlation Coefficients:
correlation_matrix = df.corr()

# Visualize correlation matrix as a heatmap:
plt.figure(figsize = (10,8))
sns.heatmap(correlation_matrix, annot = True, cmap = 'coolwarm')
plt.title('Correlation Matrix')
plt.show()
```

#### 7. Outlier Detection:
- Identify, detect and handle outliers in the dataset.
- Outliers can significantly impact analysis and modeling results.
- Data visualizations helps in finding outliers (Box Plot, Scatter Plots, etc)
- Statistical techniques such as Z scores or Interquartile Range (IQR)

```python
# Create Box Plot:
plt.boxplot(df['data'])
plt.xlabels('X axis label')
plt.ylabels('Y axis label')
plt.title('Box Plot')
plt.show()

# Import Libraries:
from scipy import stats

# Find Z Score and Threshold Values:
z_scores = stats.zscore(df['data'])
threshold = 3

# Detect Outliers:
outliers = np.where(np.abs(z_scores) > threshold)

# Handle Outliers:
median_value = df['data'].median()
df['data'][outliers] = median_value
```

#### 8. Data Transformation and Scailing:
- Make the data more normally distributed.
- Scale the features to ensure they are on same scale.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
df_scaled = scaler.fit_transform(df['data'])
```

#### 9. Finalizing the Dataset:
- Make final adjustments to the dataset.
- Remove unnecessary columns or create dummy variables for categorical features.

```python
# Remove Unnecessary Columns:
df.drop(['Address Line 2', 'Address Line 3'], axis = 1, inplace = True)

# Create Dummy Variables for Categorical Features:
df = pd.get_dummies(df, columns = categorical_columns, drop_first = True)
```  
