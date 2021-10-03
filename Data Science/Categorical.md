<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to Deal with Categorical Data ?

- **Nominal** : No Ordering | No Ranking among the values of that `Attribute`. e.g. **Genre** of Music, Movie and Videos
- **Ordinal** : Order | Rank among the values. e.g. Size of Tshirts ( XS - S - M - L - XL - XXL ), Education Level, Grades 
- You can’t **Train** the model directly with **Categorical Variables** in their raw form. 
- **Transformation** of **Categorical Labels** in **Numeric Values** by applying some **Encoding** is important.
- Convert into **Numerical Values**, Combine `Sparse` classes ( Classes with very less **Labels** )
- Set **Filter** to classes ( Class Labels should have atleast **50** Observations )

### Dichotomous ( Binary )
- Male or Female | Yes or No | True or False | 1 or 0

### Logistic Regression
- Classify the `Target` variables into 2 classes.
- If the `Target` variable has more than 2 Classes then Create **Dummy** variables. ( 1 or 0 )
- Combine **Sparse** categories ( Category labels with very less observations )

### 1. Label Encoding
- Substitute bins by **Mean** ( e.g. Age Bins by `Mean` of Age Group )
- Label Encoding is better for `Ordinal` categories.
- Rank Matters e.g. Designation feature may contain labels where rank matters ( PHD > Masters > Post Graduate > Bachelor )

> Some times use Business logic to remove **Redundancy** e.g. Pincode is enough instead of State and City 

### 2. Dummy Coding | One Hot Encoding
- Transform **Non Numerical Labels** to **Numerical Labels** ( **Binary** : `1` or `0` ) 
- Convert a **Categorical** input variable into **Numeric** variable.
- One Hot Encoding is better for `Nominal` categories ( `Rank` do not Matters )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
