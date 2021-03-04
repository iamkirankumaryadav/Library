# Feature Engineering

- **Preprocessing** of Data comes under **Feature Engineering**.
- Extract Information and Capture Meaningful **Insights** from the Dataset.
- Make Data Ready for **Machine Learning Algorithms**.
- Use `Domain Knowledge` of Data to Create **Features** and **Variables** to use in **Machine Learning**.
- Improve Machine Learning **Model Performance**.
- Remove `Unused` Features.

> Handling **Missing Data** | Encoding **Categorical Variables** | **Variable Transformation** | **Create New Features**

### 1. Handling Missing Data
- Mean | Median | Mode Imputation
- Eliminate Missing Data
- Imputation with the Help of Existing Data

### 2. Categorical Encoding
- Label Encoding
- One Hot Encoding 
- Dummy Encoding

### 3. Variable Transformation
- Make Distribution Normal
- Logarithmic ( log ( x ) ) | Exponential ( x <sup> n </sup> ) | Square root ( sqrt ( x ) ) | Reciprocal ( 1 / x )

### 4. Discretization
- Sorting Value of Variables in **Bins** or **Intervals** ( **Buckets** )
- Equal Width Discretization
- Equal Frequency Discretization
- Decision Tree Descretization ( Tree **Splits** Equally )

### 5. Handle Outliers
- **Visualize** by using **Boxplots**, **Histogram** and **Bar Graphs**
- **Filter** or **Trim** Data set 
- **Remove** Outliers ( Row or Column > 75% of Missing Data ) 

### 6. Feature Scaling
- Standardization  ( x - **mean** ( x ) ) / **std** ( x ) 
- Min Max Rescaling ( 0 - 1 )
- Maximum Absolute Scaling : Dividing Each value with Maximum Value ( 0 - 1 )
- Robust Scaling : Dividing by **IQR** ( **Q3** - **Q1** )
- Mean Normalization : ( x - mean ) / ( max - min )

### 7. Data and Time Engineering 
- Parse Data and Time so that we can extract Year, Month, Day, Week and Perform any Operation. 

### 8. Feature Creation
- Create New Meaningful Feature from the Existing Features. ( Aggregating | Arithmetic Calculation )

### 9. Aggregation of Transaction Data
- Total of Sales 
- Profit of the Day 
- Total Amount Credited or Debited for the Day 
