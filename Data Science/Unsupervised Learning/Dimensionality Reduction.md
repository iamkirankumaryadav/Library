# Dimensionality Reduction

- When the Number of **Features** is very large relative to the number of **Observations** in your Dataset 

- Certain Algorithms Struggles to **Train** Effective Models ( Especially Algorithms which consist Distance Calculations )

### Feature Selection

- Select only **Relevant** Features that make Impact on Target Variable.
- Filter Irrelevant or Redundant Features from your Dataset

### Faeture Extraction
- Create a New Data Set with Relevant Features that Captures most of the **Information** and **Insights** 

### Key Difference between Feature Selection and Feature Extraction
- Feature **Selection** keeps a Subset of the `Original` Features 
- Feature **Extraction** Creates a `New` Subset | Dataset

### Variance Thresholds
- Variance is Dependent on Scale, Always **Normalize** your **Features** first
- Remove Features whose values don't Change much from Observation to Observation 
e.g ( If a Public Health Data set contains 96% of Observations where for `35 Years Old Men`, then `Age` and `Gender` Features can be Eliminated )

### Correlation Threshold
- Remmove Highly Correlated Features ( Multicollinearity )
- **Highly Correlated** Data provides **Redundant** Information

### Principle Component Analysis ( PCA )
- Dimensionality Reduction Method ( Reduce Dimensions of Large Data Sets )
- **Transforming** Large Set of Variables into Small without **Loss** of any Information in Large Dataset.
- Reducing the Number of **Variables** of a Data Set.
- Unsupervised Algorithm
- Explains Variance
- Linear Combination of Orignal Features 
- PCA is used for Numerical Data only
- Minimize **Correlation**
- Divide the Variables into **Groups** ( High Correlated and Less Correlated ) 

### Linear Discriminant Analysis
- Supervised Algorithm
- Seperate Classes


### Auto Encoder
- Unsupervised Learning Method
- Type of Artificial Neural Network
