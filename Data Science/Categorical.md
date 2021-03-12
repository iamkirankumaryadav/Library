# How to Deal with Categorical Data ?

- More than **One Class Label** and **Discrete Value**.
- **Nominal** : No Ordering | Ranking among the Values of that `Attribute`. e.g. **Genre** of Music, Movie and Videos
- **Ordinal** : Order | Rank among the Values. e.g. Size of Tshirts ( XS - S - M - L - XL - XXL ), Education Level, Grades 

- You can’t **Train** the Model directly with **Categorical Variables** in their **Raw form**. They must be treated.
- **Transformation** of **Categorical Labels** in **Numeric Values** by applying some **Encoding** is Important.

- Convert into **Numerical Values**
- Combine `Sparse` Classes ( Classes with very less **Labels** )
- Set **Filter** to Classes ( Class Labels should have atleast **50** Observations )

### 1. Label Encoding
- Substitute Bins by **Mean**
- e.g. Age Bins by Mean of Age Group
- Label Encoding is Better for **Ordinal** Categories
- Rank Matters e.g. Designation Feature may contain Labels where Rank Matters ( PHD > Masters > Post Graduate > Bachelor )

> Some times use Business Logic to remove **Redundancy** e.g. Pincode is enough instead of State and City 

### 2. Dummy Coding | One Hot Encoding
- Transform **Non Numerical Labels** to **Numerical Labels** ( **Binary** : 1 or 0 ) 
- Convert a **Categorical Input Variable** into **Numeric Variable**
- One Hot Encoding is better for **Nominal** Categories ( Rank do not Matters )
