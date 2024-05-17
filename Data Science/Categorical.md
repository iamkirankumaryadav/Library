<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# **How to Deal with categorical data?**

- **Nominal:** No ordering | No ranking among the values e.g. **Genre** of music, movie and videos.
- **Ordinal:** Order | Rank among the values. e.g. Size of t-shirts ( XS - S - M - L - XL - XXL ) education level, grades. 
- **Binary:** Male or Female | Yes or No | True or False | 1 or 0 ( Dichotomous )
- We can't train the model directly with categorical labels they need to be encoded.
- **Encoding:** Transforming categorical labels into numeric values that can be consumed by the model.

### **Logistic Regression**
- Classify the target variables into 2 discrete classes (Binary Classification)
- If the target variable has more than 2 classes then use multiclass classification.
```python
# ovr: one vs rest | ova: one vs all
model = LogisticRegression(multi_class='ovr')
```
- Combine sparse categories (Category labels with very less observations)

### **Label Encoding (Better for Ordinal)**
- Substitute bins by **mean** (e.g. Age bins by mean of age group) Better if class labels are fewer.
- e.g. Designation feature may contain labels where rank matters ( PHD > Masters > Bachelor )

```python
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

phone['column'] = le.fit_transform(phone['column'])
```

### **Ordinal: ordered = True**
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

### **Dummy Encoding | OHE - One Hot Encoding (Better for Nominal)**
- OHE creates a binary variable (0 & 1) for each unique categorical value.

```python
from sklearn.preprocessing import OneHotEncoder

ohe = OneHotEncoder()

phone_ohe = phone_ohe.fit_transform(phone['column'].values.reshape(-1,1)).toarray()

phone_df_ohe = pd.DataFrame(phone_ohe, columns = ['Phone_'+str(int(i)) for i in range(phone_ohe.shape[1])])
phone = pd.concat([phone, phone_df_ohe], axis=1)
```

### **Nominal: ordered = False**
```python
# Use only if there are binary values in the category: i.e Male or Female, Yes or No, Present or Absent
df['Gender'] = pd.Categorical(df['Gender'], ['Male', 'Female'], ordered=False)

df['Gender'].cat.codes
```

### **Nominal: get_dummies()**
```python
# Splits the column containing nominal categorical values into individual columns:
pd.get_dummies(df)
```

Gender | Gender_Male | Gender_Female
:--- | :---: | :---:
Female | 0 | 1
Male | 1 | 0
Male | 1 | 0
Female | 0 | 1

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
