### [DS + AI](https://github.com/KIRANKUMAR7296/Library/blob/main/AI/AI.md) | [ML](https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md) | [Real World Applications](https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/IBM%20Machine%20Learning.md) | [Elite](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Primer%20Steps.md) | [NLP](https://github.com/KIRANKUMAR7296/Library/blob/main/AI/Natural%20Language%20Processing.md) | [CV](https://github.com/KIRANKUMAR7296/Library/blob/main/AI/Computer%20Vision.md) | [P1](https://github.com/KIRANKUMAR7296/Distracted-Driver-Classification) | [P2](https://github.com/KIRANKUMAR7296/SMS-Classification)

---

### [Python](https://github.com/KIRANKUMAR7296/Library/blob/main/Python/1.Python.md) | [Data Types](https://github.com/KIRANKUMAR7296/Library/blob/main/Python/2.Data%20Types.md) | [Pandas](https://github.com/KIRANKUMAR7296/Library/blob/main/Python/Pandas.md) | [NumPy](https://github.com/KIRANKUMAR7296/Library/blob/main/Python/NumPy.md) | [OOP](https://github.com/KIRANKUMAR7296/Library/blob/main/Python/3.Object%20Oriented%20Programming.md) | [Git](https://github.com/KIRANKUMAR7296/Library/blob/main/Git.md) | [SQL](https://github.com/KIRANKUMAR7296/Library/blob/main/SQL/SQL%20Queries.md)

---

### [Linear Regression](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Linear%20Regression.md) | [Metrics](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Regression%20Metrics.md) | [Regularization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md) | [Logistic Regression](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Classification/Logistic%20Regression.md) | [Ensemble Techniques](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md)
 
---

### [Statistics](https://github.com/KIRANKUMAR7296/Library/blob/main/Statistics/Statistics.md) | [Terms](https://github.com/KIRANKUMAR7296/Library/blob/main/Statistics/Important%20Statistical%20Terms.md) | [Distribution](https://github.com/KIRANKUMAR7296/Library/blob/main/Statistics/Distribution.md) | [Standardization](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Normalization%20vs%20Standardization.md) | [Error](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md) | [Bias and Variance](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Bias%20and%20Variance.md)

--- 

### [Cross Validation](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Cross%20Validation.md) | [Multiclass vs Multilabel](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Multi%20Class%20and%20Multi%20Label%20Classification.md) | [Dimensionality Reduction](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Unsupervised%20Learning/Dimensionality%20Reduction.md) | [Algorithm Selection](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Steps/Algorithm%20Selection.md)

---

### [Missing Data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Missing%20Data.md) | [Outliers](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Outliers.md) | [Categorical Feature](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Categorical.md) | [Imbalanced Data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Imbalanced%20Dataset.md) | [Overfitting](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Overfitting.md)

---

### [Pandas vs SQL](https://pandas.pydata.org/pandas-docs/stable/getting_started/comparison/comparison_with_sql.html#join)

**Time** Complexity of Occurence of Characters in a String : `O(n)`

### Log Function
- `Log` is Inverse of `Exponent`
- e.g. Base Investment : `5₹` and 5 Times Return : `125₹` ( Log<sub>5</sub> 125 : `3` Years )
- Log<sub>5</sub> 5<sup>3</sup> = 3 ( i.e. 3 * Log<sub>5</sub>5 = 3 * `1` | Log<sub>5</sub>5 = 1 )

### Model = Algorithm ( Parameters ) + Data

### Data Pipeline ( Where and How the Data are Collected, Transformed and Loaded ) 
- A Set of **Actions** that **Extract Data** from various **Sources**, Transform it into Proper Format and Load for Processing.
- An Automated Process 
- 1. Select Columns from Database
- 2. Merge Columns 
- 3. Subset Rows ( Sample ) 
- 4 Substitute NA with Mean or Medians ( Impute )
- 5. Load them in Other Database.
- First Time the Process is Complicated but if you do it Right you will have to do it just once.
- To have Automation you need to Think, Plan and Write Down in Simple Language, keep it Reproducible. ( Not only for you also for others. )

### Data Lake
- A Storage Repository where Data is Stored in its Natural | Raw format.
- Data Warehouse uses Files or Folders Structure, Data Lakes uses Flat Architecture.

### Important Disclaimer
- We try to make out **Model** more **Accurate** by **Tuning** and **Tweaking** the **Parameters**.
- But we cannot make a **100%** Accurate Model.
- **Prediction** ( Continuous ) and **Classification** Models, can never be **Error Free**.

> **Y** = f ( **x** ) + **e**

**Y** : Response Variable | Dependent Variable

**x** : Independent Variable

**e** : Irreducible Error ( Even we make a **100%** Accurate Estimate of **f ( x )**, Our Model can't be **Error Free**, known as **Irreducible Error** )

### Activation Function
- A Function that takes in the **Weighted Sum** of all the Inputs from **Previous Layer** and Generates Output for **Next Layer**.

### Hyperparameter Optimization
- Finding **Ideal** Set of **Parameters** for a Prediction Algorithm with Optimum Performance

Parameter | Hyperparameter
:--- | :---
`Internal` Configuration Variables of the Model | `External` Configuration Variables of the Model
Estimated or Learned from Data | Cannot be Estimated from Data ( Guides How to Train Algorithm )

Data Ware House | Data Lake
:--- | :---
Structured + Pre-processed | Unstructured + Semi Structured + Structured + Raw
Organized before Storing | Organized before using
Business Professionals, Analyst, BI and Visualizations | **Data Scientists**, **Analytics** and **AI**

| DBMS | RDBMS |
| :--- | :---  |
| Store Data in the form of **File** | Store Data in the form of **Tables** |
| **Hierarchical** arrangement of Data | **Rows** and **Columns** ( **Tables** ) |
| Manage **Data** in Computer | Maintain **Relationships** of **Table** in a **Database** |

| Classification | Clustering |
| :--- | :---  |
| Need **Prior** Knowledge of Data | **No Prior** Knowledge of Data |
| Classify New Sample into known **Classes** | Suggest Groups based on **Patterns** in Data |
| **Decision Tree** | **K Means** |
| **Labelled** Samples | **Unlabelled** Samples |

LDA | PCA
:--- | :---
Linear Discriminant Analysis | Principle Component Analysis
Supervised | Unsupervised

K Means | K Nearest Neighbor
:--- | :---
Unsupervised | Supervised
K : Number of **Clusters** | K : Number of **Nearest** Neighbors
Determine the Distances of Each Data Points to the **Centroid** and Assign each Point to Closest Cluster **Centroid** | **Calculate** Distance between **New** Data Point with **Nearest** K Neighbours.

Variance | Covariance
:--- | :---
**Magnitude** | **Magnitude** and **Direction**
**Data Points** from its `Mean` | Data Points **Varies** with respect to each other

### Which Algorithm Generates the Best Model ?

Accuracy | Latency
:--- | :---
How they Handle Data of Different Size ? | How Long will it take to **Train** ?
How will they Handle Complexity of Feature Relationships ? | How Long will it take to **Predict** ?
How will they Handle Messy Data ( Missing Data + Outliers )

### Autocorrelation
- The **Correlation** of the `Data Point` with a delayed copy of itself. 
- Temperature of the Day **Today** vs Temperature of the Day **Yesterday** or **Tommorrow**.

### Multicollinearity 
- A Phenomenon in which at least two **Independent Variables** are **Linearly Correlated** ( One can be `Predicted` from the other )

### Cross Join | Cartesian Product
- Generate **Paired** Combination of Each **Row** of **First** Table with each **Row** of the **Second** Table

### Data Scientist Steps 
1. Explore ( Exploratory Data Analysis ) and Clean ( Data Cleaning ) the Data
2. Split Data into Train + Validate + Test Sets
3. Train with an Initial Model and Evaluate 
4. Tune Hyperparameters + Cross Validations 
5. Evaluate on Validation Set  
6. Evaluate on Test Set
