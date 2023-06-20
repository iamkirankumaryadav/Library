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
import pandas as pd
import matplotlib.pyplot as plt

# Load the data into a DataFrame:
df = pd.read_csv('dataset.csv')
```

#### 2. Data Exploration:
- Explore the basic characteristics of the dataset.
- Use functions `dtypes`, `info` and `describe` to get an initial understanding of the data.

#### 3. Dealing with Missing Values:
- Identify and handle missing values in the dataset.
- Use functions `isnull`, `sum`, `fillna` to detect missing values.
- Choose an appropriate strategy to deal with them.

#### 4. Data Visualization:
#### 5. Feature Engineering:
#### 6. Correlation Analysis:
#### 7. Outlier Detection:
#### 8. Data Transformation and Scailing:
#### 9. Finalizing the Dataset:
