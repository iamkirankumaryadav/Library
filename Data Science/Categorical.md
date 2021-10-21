<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to Deal with Categorical Data ?

- `Nominal` : No ordering | No ranking among the values e.g. **Genre** of music, movie and videos.
- `Ordinal` : Order | Rank among the values. e.g. Size of tshirts ( XS - S - M - L - XL - XXL ) education level, grades. 
- You can’t **train** the model directly with **categorical variables** in their raw form. 
- `Transformation` of **categorical labels** in **numeric values** by applying some **encoding** is important.
- Convert into **numerical values**, combine `sparse` classes ( Classes with very less **labels** )
- Set **filter** to classes ( Class labels should have atleast **50** observations )

### Dichotomous ( Binary )
- Male or Female | Yes or No | True or False | 1 or 0

### Logistic Regression
- Classify the `target` variables into 2 classes.
- If the `target` variable has more than 2 classes then use multiclass one vs rest `OvR` or one vs all `OvA`
- Combine **sparse** categories ( Category labels with very less observations )

### 1. Label Encoding
- Substitute bins by **mean** ( e.g. Age bins by `mean` of age group )
- Label encoding is better for `ordinal` categories.
- e.g. Designation feature may contain labels where rank matters ( PHD > Masters > Post Graduate > Bachelor )

Some times use business logic to remove `redundancy` e.g. Pincode is enough instead of state and city.

### 2. Dummy Coding | One Hot Encoding
- Transform **non numerical labels** to `binary` **numerical labels** ( `1` and `0` ) 
- Convert a **categorical** input variable into **numeric** variable.
- One hot encoding is better for `nominal` categories ( `Rank` do not matters )

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
