<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Encoding Categoricals |  Qualitative Data

### Types of categorical data
1. **Nominal:** No ordering or ranking among the values e.g. Genre (music, movie or videos), color (red, green, or blue), etc.
2. **Ordinal:** Ordering or ranking among the values. e.g. Dress size (XS, X, M, L, or ML), grades (A, B, C, D), designation (Manager, Senior, Junior), ratings (low, medium, or high), etc.
3. **Binary:** Dichotomous values e.g. Male or Female, Yes or No, True or False, 1 or 0, etc.

### How to deal with categorical data?
- We cannot train the ML model directly with categorical labels, they need to be encoded into numeric values.
- Encoding: Transforming categorical labels into numerical values usable by the ML model.
- Encoding assigns numerical values to characters to store and process text, reducing size by removing redundancy.

## Data Encoding

### Label Encoding (Better for Ordinal)
Assign a unique integer to each category label, encoding the label values between **0** and **n-1**.

<table>
  <tr><th colspan=2><b>Before Encoding</b></th><th colspan=2><b>After Encoding</b></th></tr>
  <tr><td>Color</td><td>Sales</td><td>Color</td><td>Sales</td></tr>
  <tr><td>Green</td><td>50</td><td>0</td><td>50</td></tr>
  <tr><td>Blue</td><td>60</td><td>1</td><td>60</td></tr>
  <tr><td>Red</td><td>70</td><td>2</td><td>70</td></tr>
</table>

```python
# Import LabelEncoder:
from sklearn.preprocessing import LabelEncoder

# Create Instance:
le = LabelEncoder()

# Apply Fit Transform:
phone['column'] = le.fit_transform(phone['column'])
```

### Ordinal Encoding: ordered = True
Example: The designation feature may contain labels where rank matters (PHD > Masters > Bachelor)

```python
# Order represents as: [Bachelor < Master < PHD]
df['Qualification'] = pd.Categorical(df['Qualification'], ['Bachelor', 'Master', 'PHD'], ordered=True)

# Replacing categories with numeric orders:
df['Qualification'].cat.codes
```

**Qualifications** | **Encoded Values**
:--- | :---
Bachelor | 0
Master | 1
PHD | 2

### Dummy Encoding | OHE - One Hot Encoding (Better for Nominal)

**OHE** converts each unique categorical label into binary vectors (0 & 1), and each category becomes a separate feature.

```python
from sklearn.preprocessing import OneHotEncoder

ohe = OneHotEncoder()

phone_ohe = phone_ohe.fit_transform(phone['column'].values.reshape(-1,1)).toarray()

phone_df_ohe = pd.DataFrame(phone_ohe, columns = ['Phone_'+str(int(i)) for i in range(phone_ohe.shape[1])])
phone = pd.concat([phone, phone_df_ohe], axis=1)
```

### **Nominal: ordered = False**
```python
# Use only if the category contains binary values, such as Male or Female, Yes or No, Present or Absent.
df['Gender'] = pd.Categorical(df['Gender'], ['Male', 'Female'], ordered=False)

df['Gender'].cat.codes
```

### **Nominal: get_dummies()**
```python
import pandas as pd

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
