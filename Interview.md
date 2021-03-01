# Data Science
> **Science** of Extracting **Knowledge** and **Meaningful Insights** from **Structured** and **Unstructured Data**.

# Machine Learning
> Field of **Science** that gives Computer the Ability to **Learn** from **Data** without being **Explicitly** Programmed.

# Artificial Intelligence
> **Simulation** of **Human Intelligence** in **Machines** to **Think** like **Humans** and **Mimic** their **Actions**.


# Bias and Variance
- We try to make out **Model** more **Accurate** by **Tuning** and **Tweaking** the **Parameters**.
- But we cannot make a **100%** Accurate Model.
- **Prediction** ( Continuous ) and **Classification** Models, can never be **Error Free**.

> **Y** = f ( **x** ) + **e**

**Y** : Response Variable | Dependent Variable

**x** : Independent Variable

**e** : Irreducible Error

- Even we make a **100%** Accurate Estimate of **f( x )**, Our Model won't be **Error Free**, known as **Irreducible Error**

# Activation Function
- A Function that takes in the **Weighted Sum** of all the Inputs from **Previous Layer** and Generates Output for **Next Layer**.

# Decision Tree
- **Decision Tree** is used for both **Regression** and **Classification**
- **Upside Down** Approach
- Top Node ( **Root** ) | Decisions ( **Nodes** ) | Splits of Trees ( **Edges** | **Branches** ) | Terminal Node ( **Leaf** )
- **Decision** Tree Algorithms are referred to as **CART** ( **Classification** and **Regression Tree** )
- Growing a **Tree** involves deciding on **Which Features to Choose ?** and **What Conditions to Use ?** for splitting.
- We should also know when to **Stop**
- **Pruning** : Removing **Features** that are not important.

# Cross Validation
- **Validation** : **Assurance** that your model is trained well ( **Low Bias** and **Low Variance** ) 
- Whether Model is **Generalized** well for the **New Unseen Data**.
- Aim is to reduce **Overfitting**.

### 1. Holdout Method ( **Traditional Approach** )
- Remove a Part of **Training Data** befor Training and keep it for **Validation**.
- By Reducing the **Trainiing Data**, we risk losing important **Patterns | Trends** in Dataset.
- Suffers from **High Variance**.
- Create a Model with **Low Bias** and **Low Variance**.

### 2. K Fold Cross Validation
- Data is divided into **k** subsets.
- One of **k** subset is used as **Validation Set**.
- **k - 1** subsets are used as **Training Set**.
- **Mean** Error of **k** trials is calculated.
- Reduces **Bias** and **Variance**.

### Stratified K Fold Cross Validation
- Data is divided into **k** subsets.
- Each Subset has **Equal Proportion** of samples of each **Target Class**.
- One of **k** subset is used as **Validation Set**.
- **k - 1** subsets are used as **Training Set**.
- **Mean** Error of **k** trials is calculated.
- Reduces **Bias** and **Variance**.

### Leave One Out Cross Validation | LOOCV
- Leave **One Data** from the Training Dataset for **Validation**.
- Use remaining Data Samples for **Training**.
- Repeated for all combinations.
- Approach is **Exhaustive**, Need to **Train** and **Validate** the Model for all **Possible Combinations**. 

# Multiclass vs Multilabel Classification

| Multiclass | Multilabel |
| :--- | :--- |
| Classify more than **Two Classes** | Classify more than **Two Labels** |
| Image with Single Picture | A **Post** can be posted with Multiple **#Tags** on Social Media  |
| Iris Flower : Setosa \| Versicolor \| Virginica | Image containing Men, Tree, Car, Sky in One Picture |
| Penguin : Chinstrap \| Adelie \| Gentoo | StackoverFlow Question may fall into **#DataScience #ML #AI** |

# DBMS vs RDBMS

| DBMS | RDBMS |
| :--- | :---  |
| Store Data in the form of **File** | Store Data in the form of **Tables** |
| **Hierarchical** arrangement of Data | **Rows** and **Columns** ( **Tables** ) |
| Manage **Data** in Computer | Maintain **Relationships** of **Table** in a **Database** |

### Cross Join | Cartesian Product
- Generate **Paired** Combination of Each **Row** of **First** Table with each **Row** of the **Second** Table

