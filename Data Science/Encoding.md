<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Encoding Categorical |  Qualitative Data

### Types of categorical data
1. Nominal: No specific order, just categories (e.g., Genre: music, movies, Colors: red, blue)
2. Ordinal: Has an order or ranking (e.g., Dress size: XS, M, L; Grades: A, B, C)
3. Binary: Two possible values (e.g., Male/Female, Yes/No, 1/0)

### How to deal with categorical data?
- ML models can’t use categorical labels directly, they need to be converted into numeric values.
- Encoding: Transforming categorical labels into numbers for use in ML models.
- It converts text into numbers, reducing data size and eliminating redundancy.

## Data Encoding

### Label Encoding (Better for Ordinal)
Assign a unique integer to each category, encoding label values from 0 to n-1.

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

**OHE** converts each categorical label into a binary vector (0s and 1s), and each category becomes a separate feature.

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
