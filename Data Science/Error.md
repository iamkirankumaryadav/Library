<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Error in Linear Regression

### Manage Noise
- Created **Model** will have a lot of `Error` because of `Noise`, `Noise` is Unwanted that **Weakens** the Learning Process of **Model**.

### Reasons for **Noise**
- `Large` Training Data Set | Errors in Input Data | Data Labelling Error | Unobserved Attributes | Hidden Patterns.

### Data Visualization helps to Find Hidden Patterns.

### Important Confusing Terms

1. Sum of Squared Residual ( `RSS` ) | Sum of Squared Error ( `SSE` )
2. Explained Sum of Square ( `ESS` ) | Sum of Squared Regression ( `SSR` )
3. Total Sum of Square ( `TSS` ) | Sum of Squared Total ( `SST` )
4. R Squared ( R<sup>2</sup> | Coefficient of Determination | Squared Correlation Coefficient )

### RSS | SSE

> Residual Sum of Squares | Sum of Squares Error

![RSS|SSE](Image/SSE_RSS.jpg)

- e : Error
- SSE = Sum ( Actual - Prediction ) <sup>2</sup>
- Residuals : Sum of Squares of Errors.
- Unexplained Variability.
- Variability : Distance of Actual Value from its Mean or Predicted Value.

### ESS | SSR

> Explained Sum of Squares | Sum of Squares Regression.

![ESS|SSR](Image/SSR_ESS.jpg)

- Measures How well our Line Fits the Data.
- Sum ( Prediction - Mean ) <sup>2</sup>
- Explained Variability.

### TSS | SST

> Total Sum of Squares | Sum of Squares Total

![TSS|SST](Image/SST_TSS.jpg)

- Measures Total Variability
- Explained Variability + Unexplained Variability
- Sum ( Actual - Mean ) <sup>2</sup>
- SST = SSR + SSE
- TSS = ESS + RSS

![TSS](Image/All.jpg)

### R Squared

- Measures Goodness of Fit
- Explains Variability of Model.
- R<sup>2</sup> = SSR / SST
- R<sup>2</sup> = ESS / TSS
- Explained Variability / Total Variability.
- R<sup>2</sup> ranges between 0 and 1
- R<sup>2</sup> = 0 means our Regression Line Explains None of the Variability of the Data
- R<sup>2</sup> = 1 means our Model Explains the Entire Variability of the Data.

### Note

- R<sup>2</sup> = 0 or R<sup>2</sup> = 1 is very Rare.
- R<sup>2</sup> Actually Ranges between 0.2 to 0.9

### What is Variability ?

- How **Spread** Out the Data is. 
- Data Points are Distributed.  
- Far Distance with Each Other.

### How to Describe ?

1. Range
2. Interquartile range
3. Variance
4. Standard Deviation

### Range 

- Range = Max - Min

- Distance between the Largest and Smallest Data Point in a Data Set.

### Interquartile Range

- Data Set is Divided in 4 Equal Quartiles
- IQR = Q3 - Q1
- Tells where most of the Values Lies.
- Q0 = Min
- Q1 = First Quartile | 25th Percentile
- Q2 = Second Quartile | Median | 50th Percentile.
- Q3 = Third Quartile | 75th Percentile
- Q4 = Fourth Quartile | Max

### Variance

- How Spread Out Data is ?
- Small Variance = Data Set is Tight Clustered.
- Large Variance = Data Set is Spread Apart.

### Standard Deviation

- Data is **Closer** to the Mean or **Away** from the Mean.
- Tall Bell Curve : Data is Tightly around Mean.
- Small Bell Curve : Data is Uniformely Spread.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
