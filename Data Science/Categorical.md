<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# How to Deal with `Categorical Data` ?

- `Nominal` : No ordering | No ranking among the values e.g. **Genre** of music, movie and videos.
- `Ordinal` : Order | Rank among the values. e.g. Size of tshirts ( XS - S - M - L - XL - XXL ) education level, grades. 
- `Binary` : Male or Female | Yes or No | True or False | 1 or 0 ( Dichotomous )
- We can't `train` the model directly with `categorical labels` they need to be encoded.
- `Encoding` : Transforming `categorical labels` in `numeric values` that can be consumed by model.

### `Logistic Regression`
- Classify the `target` variables into 2 `discrete` classes ( Binary Classification )
- If the `target` variable has more than 2 classes then use multiclass classification.
```python
ovr: one vs rest 
ova: one vs all

# Define model
model = LogisticRegression(multi_class='ovr')
```
- Combine `sparse` categories ( Category labels with very less observations )

### `Label Encoding` ( Better for `Ordinal` )
- Substitute bins by **mean** ( e.g. Age bins by `mean` of age group ) Better if `class labels` are less.
- e.g. Designation feature may contain labels where rank matters ( PHD > Masters > Post Graduate > Bachelor )

### `Dummy Encoding` | `One Hot Encoding` ( Better for `Nominal` )
- Transform **non numerical labels** to `binary` **numerical labels** ( `1` and `0` ) 
- Convert a **categorical** input variable into **numeric** variable.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

### Handle Categorical Data ( Ordinal )

Qualification
:---
Bachelor
Master
PHD

```python
df['Qualification'] = pd.Categorical(df['Qualification'], ['Bachelor', 'Master', 'PHD'], ordered=True)

# Order represents as: [Bachelor < Master < PHD]

# Replacing categories with numeric orders.
df['Qualification'].cat.codes

print(df['Qualification'])
```

Qualification
:---
0
1
2
