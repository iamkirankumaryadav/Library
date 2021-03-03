# How to Deal with Categorical Data ?

- More than **One Class Label** and **Discrete Value**.
- **Nominal** : No Ordering among the Values of that attribute. e.g. **Genre** of Music, Movie and Videos
- **Ordinal** : Order among the Values. e.g. Size of Tshirts ( XS - S - M - L - XL - XXL ), Education Level, Grades 

- You can’t **Train** the Model with  Categorical Variables** in their **Raw form**. They must be treated.
- **Transformation** of **Categorical Labels** in **Numeric Values** by applying some **Encoding Scheme** is Important.

- Convert into **Numerical Values**

### 1. Label Encoding
- Transform **Non Numerical Labels** to **Numerical Labels** ( **Nominal** ) 
- Substitute Bins by **Mean**
- e.g. Age Bins by Mean of Age Group

> Some times use Business Logic to remove **Redundancy** e.g. Pincode is enough instead of State and City 

### 2. Dummy Coding | One Hot Encoding
- Convert a **Categorical Input Variable** into **Numeric Variable**

