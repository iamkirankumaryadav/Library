# Data Exploration

Exploration requires **Patience** to Slice and Dice Data in multiple ways.

**Clean** and **Understand** the Data in a Comprehensive way.

> Understand, Clean and Prepare your data for building your **Predictive Model**

1. Variable Identification
2. Univariate Analysis
3. Bivariate Analysis
4. Handling Missing Value
5. Outlier Treatment
6. Variable Transformation
7. Variable Creation

### 1. Variable Identification
- Identify **Independent** Features ( **Predictor** ) and **Dependent** Feature ( **Target** )
- e.g. Suppose we want to **Predict**, whether Student will play Cricket or not.
- Identify **Predictor Variables**, **Target Variable**, **Data type** of Variables and **Category** of Variables ( Categorical or Continuous ).

### 2. Univariate Analysis
- Depends on whether the Variable is Continuous or Categorical
- Highlist Missing, Duplicate and Outliers.

a. Continuous Variables 
- Understand the **Central Tendency** and **Spread* of Variables.
> Central Tendency ( Mean | Median | Mode | Min | Max )
> Measure of Spread | Dispersion ( Range, Quartile, IQR, Variance, Standard Deviation, Skewness and **Kurtosis** )
> Visualization ( Histogram | Box Plot )

b. Categorical Variables 
- Frequency Table to Understand **Distribution** of each Category.
- Value Count | Unique | Nunique | Percentage
- Bar Chart.

### 3. Bivariate Analysis
- Find **Relationship** between two Variables
- Combinations ( Continuous and Continuous | Categorical and Continuous | Categorical and Categorical )

a. **Continuous** and **Continuous**
- Find **Patterns** and **Relationship** using **Scatter Plot**
- The Relationship can be **Linear** or **Non Linear**.
- **Correlation** indicates the **Strength** of Relationship
- **Correlation** lies between **-1** to **1**
- **Correlation = 1** Perfect **Positive** Correlation.
- **Correlation = -1** Perfect **Negative** Correlation.
- **Correlation = 0** No Correlation.

b. **Categorical** and **Categorical**
- Two Way Table and **Stacked Column Chart**

### **Chi Squared Test** 
- A Test for **Independence** of two Categorical Variables and returns **Probability**.
- Derive **Statistical Significance** of Relationship between the Variables.
- Test whether the **Evidence** in the **Sample** is Strong enough to **Generalize** that relationship for a **Population**.
- Difference between **Expected** and **Observed**
- Probability = 0 indicates both Categorical Variable are **Dependent**.
- Probability = 1 indicates both Categorical Variable are **Independent**.

b. **Categorical** and **Continuous**
- Z Test and T Test : Whether **Mean** of two groups are statistically different from each other or not.
