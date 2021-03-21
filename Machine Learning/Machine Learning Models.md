<h1 align="center">Machine Learning Models 🤖🚀💻</h1>



![Machine Learning Algorithms](Image/MLAlgorithm.png)

<h1 align="center">Machine Learning Map</align></h1>
  
<table align='center'>
  <tr>
    <th colspan=2>
      <a href=#sup>Supervised Learning</a>
    </th>
    <th>
      <a href=#unsup>Unsupervised Learning</a>
    </th>
    <th>
      Reinforcement Learning
    </th>
  </tr>
  <tr>   
    <th>
      Regression
    </th>
    <th>
      Classification
    </th>
    <th>
      Clustering
    </th>
  </tr>
  <tr>
    <th>
      Predict Continuous Data
    </th>
    <th>
      Classify Discrete Data
    </th>
    <th>
      Group Similar Data 
    </th>
  </tr>
  <tr>
    <td>
      <ol type="1">
        <li><a href=#linreg>Linear</a> ( Straight Line )
          <ul>
            <li>Simple Linear</li>
            <li>Multiple Linear</li>
          </ul>
        </li>
        <li>Polynomial ( Curved Line )</li>
        <li>Ridge and Lasso</li>
      </ol>
    </td>
    <td>
      <ol type="1">
        <li><a href=#logreg>Logistic</a></li>
        <li><a href=#tree>Decision Tree</a></li>
        <li><a href=#forest>Random Forest</a></li>
        <li><a href=#svm>Support Vector Machine</a></li>
        <li><a href=#naive>Naive Bayes</a></li>
        <li><a href=#knn>K Nearest Neighbors</a></li>
      </ol>
    </td>
    <td>
      <ol type="1">
        <li><a href=#kmean>K Mean</a></li>
        <li><a href=#hc>Hierarchical</a></li>
        <li>DBSCAN</li>      
      </ol>
    </td>
  </tr>
</table>


### Steps of Machine Learning
1. Gathering Data
2. Preparing Data ( Data Preprocessing )
3. Explore Data ( Exploratory Data Analysis | **EDA** ) 
4. Clean Data ( Data Cleaning )
5. Feature Engineering ( Important Features to Train Model )
6. Choosing a Correct Model
7. Training Data
8. Testing Data and Evaluation
9. Hyperparameter Tuning
10. Prediction

> Model is the system that makes **Predictions**

> **Parameters** are the Factors which are considered by the model to make **Predictions**. **Linear Regression** ( parameters... )

> Learner makes **Adjustments** in the Parameters and the Model to Align the Predictions with Actual Results.

<table align="center">
 <tr>
  <th colspan="2">
   <h3 name='sup'>Supervised Learning</h3>
  </th>
 </tr>
 <tr>
  <th colspan="2">
   One or More Independent Features is used to Predict Dependent Continuous Values or Classify Discrete Labels
  </th>
 </tr>
 <tr>
  <th>
   Regression
  </th>
  <th>
   Classififcation
  </th>  
 </tr>
 <tr>
  <td>
   <ul>
    <li>Predict Continuous Numeric Value</li>
    <li>Output is Continuous</li>
    <li>Further Improved by Regularization or by using Non Linear Model</li>
   </ul>
  </td>
  <td>
   <ul>
    <li>Classify Discrete Classes</li>   
    <li>Output is Discrete</li>
   </ul>
  </td>
 </tr>
</table>

<h3 name='linreg'>1. Linear Regression</h3> 

![Linear Regression](Image/RegressionLine.png)

![Equation of Line](Image/EquationLine.png)

> Simple Linear Regression : Find the Line that **Fits** the Data.

> Multiple Linear Regression : Find the Plane | Hyperplane of **Best Fit**.

> Polynomial Regression : Find a Curve for **Best Fit**. 

<h3 name='logreg'>2. Logistic Regression ( Classification )</h3>

- Dependent ( Output ) should be **Discrete** ( 0 or 1 )
- Used for **Classification**
- Probability of Finite Number of Outcomes | Occurence.
- Output values can be between 0 and 1
 
<h3 name='tree'>3. Decision Tree</h3>

- **Root** Node and **Internal** Nodes are **Conditions**
- **Leaf** Node represents a Class **Label** | **Terminal** Node
- **Splits** a Dataset based on **Different** Conditions ( Branch | Edge | Split )
- Used **Binary** Classification and **Multiclass** Classification and even for **Regression**
- Tree Models where the Target Variable takes a **Discrete** Set of Values are **Classification** Tree
- Tree Models where the Target Variable takes a **Continuous** Values are **Regression** Tree
- **CART** : **C**lassification **A**nd **R**egression **T**ree

### Information Gain 

- **Information Gain** is used to decide which Feature ( **Root** Node ) to **Split** on at each step in Building the Tree
- The Split with the Highest **Information Gain** will be taken as the First Split and the process will continue untill **IG** becomes 0

### Gini Index ( Checks for Impurity in the Dataset )

- Lowest Gini Index is selected 
- Pure : All Data belongs to Same Class in a Subset ( Gini Index : 0 )
- Impure : Data is Mixture of Different Classes in a Subset

Advantage of Decision Tree | Disadvantage of Decision Tree
:--- | :---
Handle **Categorical** and **Numerical** Data | Prone to **Overfitting**
No effect of **Outliers** | Need Carefull **Parameter Tuning**

### How to Avoid Overfitting
- Remove | **Prune** Branches with Less Importance ( Irrelevant Feature )
- Early Stop ( Limit the Max Depth of the Tree )

<h3 name='forest'>4. Random Forests ( Ensemble Learning Technique | Bagging )</h3>

- Multiple **Decision Trees** ( Weak Learners ) trained **Parallel** Individually
- **Bootstrapped Data Sets** of Orignal Data and **Randomly** selecting **Subsets** at each step. ( **Sampling** with **Replacement** )
- Bagging Technique ( **Multiple** Decision Trees are **Trained** in **Parallel** to Form a **Strong Learner** ) 
- **Prediction** of Model is based on the **Voting** of Decision Trees Output ( **Majority Voting** )
- Reduces Risk of **Error** and **Overfitting**.

<h3 name='svm'>5. Support Vector Machine | SVM</h3>

- SVM can be used for both **Regression** and **Classification**
- Finds a **Line** or **Hyperplane** that Separates the 2 **Distinct** Classes with Maximum **Margin** in **N Dimensional Space**.
- **Hyperplanes** are **Decision Boundaries** that help to Classify the Data Points.
- Data Points are **Support Vectors**.
- SVM can be used for **Linear** and **Non Linear** Data.
- SVM uses **Kernel Trick** for **Non Linear** Data which Creates a **Hyperplane** in **N Dimensional Space**.

### Benefits 

- SVM also works well with **Unstructured** and **Semi Structured** Data ( Text, Image, Tree )
- **Generalize** Well ( Works well on New Unseen Data )
- Risk of **Overfitting** is Less.

### Disadvantage

- Choosing a Good Kernel Function is not easy
- Long **Training Time** for Large Datasets.
- Difficult to Interpret and Understand Final Model, Variable Weights and Individual Impact.
- Not easy to **Fine Tune** and **Visualize**.

<h3 name='knn'>6. K Nearest Neighbours</h3>

- **K** : Number of Nearest **Neigbors**
- Calculate Distance between New **Test** Data Point and **K Nearest Neigbours** of **Training** Data Points
- Sort the Calculated Distance in **Ascending Order**
- Get Nearest ( **Least** Distance ) to it or most **Frequent Classes** in Neighbor

<h3 name='naive'>7. Naive Bayes</h3>

- Based on **Conditional Probability** | Class **Prediction** Probability ( Used for **Binary** and **Multiclass** Classification )
- Probabilistic Machine Learning Model ( Likelihood, Prior Probability and Posterior Probability )
- Probability of **Event A** if **Event B** has already occured
- **Naive** : Because it assumes that all of the **Independent Features** are **Independent** from each other
- e.g **Classification** of Dogs Breed ( Naive Bayes tries to Create a **Probability** that the Dog belongs in each Class | Label )
- Weights can be Added to Improve **Accuracy** 

> P( **A** | **B** ) = P( **B** | **A** ) / P( **B** )

All follow Same Process in **Regression** and **Classification** the only difference is Output 

> **Regression** Output : **Continuous**

> **Classification** Output : **Discrete**

<h1 name='unsup'> Unsupervised Learning</h1>

- Find **Patterns** and **Relationships** between **Independent** Features and **Dependent** Feature ( **Labels** )
- Extract Important Features and Explore the Data Set in Detail.

### A. Clustering

- Group the Data Set into Groups | Segments | Clusters According to **Similarity**.
- Customer Segmentation | Fraud Detection | Document Classification

> Clustering Techniques

<h3 name='kmean'>1. K Mean Clustering</h3>

- Cluster Data Points with Similar Characteristics in one Cluster
- We Choose **K** number of Clusters
- Select **K** Random Data Points as Centroid
- Data Points nearest to its Corresponding Centroid belongs to that Cluster
- Again the Centroid is Calculated
- The Data Points are Updated based on New Centroid
- **Iterative** Process | Stops when there is no further Classification.
- Different Starting Points ( Random Centroid Selected ) Create Different Clusters 
- **Elbow** Method : Sum of Squared Distance get smaller as the Number of Clusters Increases

<h3 name='hc'>2. Hierarchical Clustering</h3>

A. Agglomerative
- Bootom Up Approach
- **AGNES** ( **Ag**glomerative **Nes**ting )
- Each Data Point is considered as an Individual Cluster
- At each Iteration, Similar Clusters merge with other Clusters until One Single Cluster remains.

B. Divisive
- Top Down Approach
- **DIANA** ( **Di**vise **Ana**lysis )
- Dividing the Single Cluster into n Clusters

### How we Calculate Similarity between the Clusters
- **MIN** ( Distance between the Closest Points of Two Clusters )
- **MAX** ( Distance between the Farthest Points of Two Clusters )
- Group **AVG** ( Average of Distance between Each Data Points of Two Clusters )
- Distance between **Centroids** ( Distance between the Centroid of Two Clusters )
 
### 3. Density Based Clustering

### B. Dimensionality Reduction

- Aim is to find  the **Inportant Features** that can be used for by our Model for Better Predition.
- Reducing the Number of **Irrelevant Features** that has no relation with the Target Feature.
- There are some Features that brings **Multicollinearity** 
- Feature **Elimination** | **Feature Selection** or Feature **Extraction**
- Save Storage and Time by Improving Performance of Model.
- Due to less number of Features it can be Visualized in 2D and 3D.

### Anomaly Detection :
- Automatically Discover **Unusual** Data Points in Data Set.
- Used to Find Fraudulent Transactions, Identify an Outlier caused by Human Error during Data Entry.
- Reduces Complexity of Data and Helps to Understand Data more Clearly and Better Way.

### Association Mining :
- Set of Items that Frequently Occur together in Data Set.
- Basket Analysis : Items Bought Together | Goods Purchased at the Same Time Help to Develop Marketing Strategies.

### Feature Selection
- **Select** Important Features | Helps to Improve **Accuracy** | Not Every Feature Adds Value to Solve Problem
- **Remove** Unwanted Features | Irrelevant Features Affects Accuracy |
- **Understanding** Each Feature before using it for Creating Machine Learning Model

> Techniques of Dimensionality Reduction

### Feature Extraction

- **PCA** : Principal Component Analysis. ( Reduce Dimensions of Data )
- **LDA** : Linear Discriminant Analysis.
