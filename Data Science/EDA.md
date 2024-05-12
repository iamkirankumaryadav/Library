# **Exploratory Data Analysis**

EDA is a process of analyzing and summarizing data using statistics and data visualization methods.

1. **EDA** is the most essential step in a data science and data analysis process.
2. **Data scientists** spend almost 70% of their work doing EDA of their dataset.
3. Discover patterns, spot anomalies, identify outliers, understand main characteristics, gain insights, test hypotheses, and check assumptions with summary **statistics** and **graphical representations**.
4. An iterative cycle that involves generating questions about the data, searching for answers by visualizing, transforming, and modelling the data, and using what is learned to refine or generate new questions.
5. **Graphical Analysis**: Visualizations and charts are used to visualize trends and patterns in the data.
6. **Statistical Analysis**: Measuring central tendency, spread, variability and distribution are used to analyze the data.
7. EDA helps to prepare the dataset for analysis, allows the ML model to predict, gives more accurate results, and helps to choose a better ML model.
8. Allows you to get a better understanding of your data before you start building models or making predictions.
9. The best approach will vary depending on the specific data set and the goals of your analysis.
10. EDA is a powerful tool that can help you to better understand your data and make better decisions about how to use it.

### Steps:
1. Loading Data
2. Data Exploration
3. Handling Missing Data
4. Data Visualization
5. Feature Engineering
6. Outlier Detection
7. Data Encoding
8. Transformation / Rescaling / Standardization

### By exploring your data, you can identify the following:

1. **Missing values:** Are there any missing values in your data?
2. **Outliers:** Are there any outliers in your data? Unusual data points.
3. **Distributions:** What are the distributions of your data? Are they normally distributed or skewed?
4. **Relationships:** Is there any correlation between independent and dependent variables? 
5. Patterns: Are there any patterns in your data? For example, are there any trends over time?

### Steps:

### **1. Importing Libraries and Loading Dataset:**
- Import required **libraries**, **modules** and **submodules**.
- Load your dataset into a **DataFrame**.

```python
# Import Libraries:
import pandas as pd # For Data Manipulation
import matplotlib.pyplot as plt # For Data Visualization

# Load the data into a DataFrame:
df = pd.read_csv('dataset.csv')
```

### **2. Data Exploration:**
- Explore the basic characteristics of the dataset.
- Use functions like **dtypes**, **info** and **describe** to get an initial understanding of the data.

```python
# Summary Information of Dataset:
df.info()

# Descriptive Statistics:
df.describe()
```  

### **3. Dealing with Missing Values:**
- Identify and handle missing values in the dataset.
- Use functions **isnull**, **sum**, **fillna** to detect missing values.
- Choose an appropriate strategy to deal with them.

```python
# Find missing values:
df.isna().sum()

# Handle missing values by imputation:
df.fillna(value, inplace=True)

# Handle missing values by removal:
df.dropna(inplace=True)
```

### **4. Data Visualization:**
- Create a visual representation of the data to gain insights.
- Generate various plots, such as histograms, scatter plots, box plots and correlation matrix.
- Libraries like Matplotlib, Seaborn or Plotly to create visuals.

```python
# Create Histogram:  
plt.hist(df['Height'], bins=10)
plt.xlabels('X axis label')
plt.ylabels('Y axis label')
plt.title('Histogram')
plt.show()
```
          
### **5. Feature Engineering:**
- Explore and create new features from the existing features to enhance the predictive power of the data.
- FE involves transformation, scaling, binning and creating derived features based on domain knowledge.

```python
# Create new feature by binning an existing feature:
df['new_column'] = pd.cut(df['existing_column'], bins = [0, 10, 20, 30, 40])
```  

### **6. Correlation Analysis:**
- Examine the relationships between variables in the dataset.
- Calculate correlation coefficients and visualize them using heatmaps or correlation matrices.

```python
# Calculate correlation coefficients:
correlation_matrix = df.corr()

# Visualize correlation matrix as a heatmap:
plt.figure(figsize = (10,8))
sns.heatmap(correlation_matrix, annot = True, cmap = 'coolwarm')
plt.title('Correlation Matrix')
plt.show()
```

### **7. Outlier Detection:**
- Identify, detect and handle outliers in the dataset.
- Outliers can significantly impact analysis and modelling results.
- Data visualizations help in finding outliers (Box Plot, Scatter Plots, etc.)
- Statistical techniques such as Z scores or Interquartile Range (IQR)

```python
# Create Box Plot:
plt.boxplot(df['data'])
plt.xlabels('X axis label')
plt.ylabels('Y axis label')
plt.title('Box Plot')
plt.show()

# Import libraries:
from scipy import stats

# Find Z score and threshold values:
z_scores = stats.zscore(df['data'])
threshold = 3

# Detect outliers:
outliers = np.where(np.abs(z_scores) > threshold)

# Handle outliers:
median_value = df['data'].median()
df['data'][outliers] = median_value
```

### **8. Data Transformation and Scaling:**
- Make the data more normally distributed.
- Scale the features to ensure they are on the same scale.
- Discourage the dominating features with high-scale values.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
df_scaled = scaler.fit_transform(df['data'])
```

### **9. Finalizing the Dataset:**
- Make final adjustments to the dataset.
- Remove unnecessary columns or create dummy variables for categorical features.

```python
# Remove unnecessary columns:
df.drop(['Address Line 2', 'Address Line 3'], axis = 1, inplace = True)

# Create dummy variables for categorical features:
df = pd.get_dummies(df, columns = categorical_columns, drop_first = True)
```  

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
