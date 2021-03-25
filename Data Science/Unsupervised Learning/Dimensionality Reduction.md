<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Dimensionality Reduction

- Unsupervised Machine Learning 
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

### Linear Discriminant Analysis 
- Supervised Algorithm
- Seperate Classes
- Works better with Large Data Set

### Principle Component Analysis ( PCA )
- Dimensionality Reduction Method ( Reduce Dimensions of Large Data Sets, Explains Variance and Minimize **Correlation** )
- **Transforming** Large Set of Variables into Small without **Loss** of any Information in Large Dataset.
- Reducing the Number of **Variables** of a Data Set.
- Linear Combination of Orignal Features 
- PCA is used for Numerical Data only
- Divide the Variables into **Groups** ( High Correlated and Less Correlated ) 

### Auto Encoder
- `Unsupervised` Learning Method
- Type of Artificial Neural Network
- Learn | Discover the **Representation** | **Structure** of Data Set
- Ignore Noise in Data 

### Applications of autoencoders include:

1. Anomaly detection
2. Removine Noise from Data ( Images, Audio )
3. Image Inpainting | Conservation | Restoration ( **Reconstructing** Missing Part of an Image )
4. Information Retrieval

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
