<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

<h1 align="center">Machine Learning Models 🤖🚀💻</h1>

<h3 align="center">Machine Learning Map</align></h3>
  
<table align='center'>
  <tr>
    <th colspan=2>
      <h3><a href=#sup>Supervised Learning</a></h3>
    </th>
    <th colspan=2>
      <h3><a href=#unsup>Unsupervised Learning</a></h3>
    </th>    
  </tr>
  <tr>   
    <th>
      <a href='#reg'>Regression</a>
    </th>
    <th>
      <a href='#class'>Classification</a>
    </th>
    <th>
      <a href='#cluster'>Clustering</a>
    </th>
    <th>
      Association
    </th>
  </tr>
  <tr>
    <th>
      Predict Continuous Numerical Data
    </th>
    <th>
      Classify Discrete Categorical Data
    </th>
    <th>
      Group Similar Data 
    </th>
    <th>
      Identify Similar Data
    </th>
  </tr>
  <tr>
    <td rowspan=3>
      <ol type=1>        
        <li>Simple Linear ( Line of Best Fit )</li>
        <li>Multiple Linear ( Plane of Best Fit )</li>            
        <li>Polynomial ( Curve of Best Fit )</li>
        <li>Lasso ( L1 )</li>
        <li>Ridge ( L2 )</li>
      </ol>
    </td>
    <td rowspan=3>
      <ol type=1>
        <li><a href=#logreg>Logistic Regression</a></li>
        <li><a href=#tree>Decision Tree</a></li>
        <li>
          <a href="https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Ensemble%20Techniques.md">Ensemble Techniques</a>
          <ul>
            <li>Bagging
            <ol type=A>
              <li><a href=#forest>Random Forest</a></li>
            </ol>
            </li>
            <li>Boosting
            <ol type=A>
              <li><a>ADABOOST</a></li>
              <li><a>Gradient Boosting</a></li>
              <li><a>XGBOOST</a></li>
            </ol>
            </li>
          </ul>
        </li>        
        <li><a href=#svm>Support Vector Machine</a></li>
        <li><a href=#naive>Naive Bayes</a></li>
        <li><a href=#knn>K Nearest Neighbors</a></li>
      </ol>
    </td>    
    <td>
      <ol type=1>
        <li><a href=#kmean>K Mean</a></li>
        <li><a href=#hc>Hierarchical</a></li>
        <li><a href="#dbscan">DBSCAN</a></li>      
      </ol>
    </td>
    <td rowspan=3></td>
  </tr>
  <tr>
    <th>Dimension Reduction</th>    
  </tr>
  <tr>
    <td>
      <ol type=1>
        <li><a href=#pca>PCA</a></li>
        <li><a href=#lda>LDA</a></li>
        <li><a href=#tsne>t-SNE</a></li>
      </ul>
    </td>        
  </tr>  
</table>

> Features | Independent Variables | Dimensions | Attributes | Inputs | Predictors | Estimators

> Target | Dependent Variable | Label | Class | Output | Predicted Value | Estimated Value

> Model is the system that makes **Predictions** or **Classification**

> **Parameters** are the Factors which are considered by the model to make **Predictions** or **Classification**

> **Parameters** are Adjusted or Tuned in order to gain **Accuracy** and **Assurance** that the Model is giving Desired Results.

### Steps of Machine Learning
1. Gathering Data
2. Preparing Data ( Data Preprocessing )
3. Explore Data ( Exploratory Data Analysis | **EDA** ) 
4. Clean Data ( Data Cleaning )
5. Feature Engineering ( Important Features to Train Model )
6. Choosing a Correct Model
7. Training Data
8. Testing Data and Evaluation ( [**Metrics**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Regression%20Metrics.md) )
9. Hyperparameter Tuning
10. Prediction

<h1 name='sup' align=center>Supervised Learning ( Labeled Data )</h1>

<table align=center>
  <tr>
    <th><h3>Prediction</h3></th>
    <th><h3>Classification</h3></th>
  </tr>
  <tr>
    <th>Predicts a Numerical Variable</th>
    <th>Predicts a Categorical Variable</th>
  </tr>
</table>

<h1 name='reg' align=center>Regression</h1>

<table align=center>
  <tr>
    <th colspan=3><h3><a href="https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Linear%20Regression.md">Linear Regression</a></h3></th>
  </tr>
  <tr>
    <td>1</td>
    <td><strong>Simple Linear Regression</strong></td>
    <td>Find the <strong>Line</strong> of Best Fit</td>            
  </tr>
  <tr>
    <td>2</td>
    <td><strong>Multiple Linear Regression</strong></td>
    <td>Find the <strong>Plane | Hyperplane</strong> of Best Fit</td>  
  </tr>
  <tr>
    <td>3</td>
    <td><strong>Polynomial Linear Regression</strong></td>
    <td>Find the <strong>Curve</strong> of Best Fit</td>
  </tr>
  <tr>
    <td>4</td>
    <td><a href="https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md"><b>Regularization</b></a></td>
    <td>Helps to Improve Linear and Polynomial Regressions</td>
  </tr>
  <tr>
    <td colspan=3>One or More <b>Independent Features</b> is used to Predict <b>Continuous Dependent Numeric Variable</b></td>
  </tr>
  <tr>
    <td colspan=3>Dependent Variable | Target | Output should be <b>Continuous</b></td>
  </tr>
</table>

<h3 name='linreg'>1. Linear Regression</h3>

![Equation of Line](Image/EquationLine.png)

<h1 name='class' align=center>Classification</h1>

<h3 name='logreg'>2. Logistic Regression</h3>

- One or More Independent Features is used to **Classify** Discrete Categorical Labels 
- Dependent ( Output ) should be **Discrete** ( 0 or 1 )
- Probability of Finite Number of Outcomes | Occurence.
 
<h3 name='tree'>3. Decision Tree</h3>

- **Root** Node ) | Nodes ( Decisions | Conditions | Outcomes ) | Edges | Branches ( Splits of Trees ) | Leaf Node ( Terminal | Label | Class )
- We Select the Feature as **Node** that **Splits** the Data very well.
- Attribute with **High Information Gain** or **Low Entropy** is Selected as **Best Attribute** to Split upon.
- Used especially for **Binary** Classification and **Multiclass** Classification and even used for **Regression**
- Tree Models where the Target Variable takes a **Discrete** Set of Values are **Classification** Tree
- Tree Models where the Target Variable takes a **Continuous** Values are **Regression** Tree
- **CART** : **C**lassification **A**nd **R**egression **T**ree
- Growing a Tree means Deciding Which **Feature** to Choose ? and What **Condition** to Use ? for splitting.
- Continuous can be Converted into Binary or Boolean by Setting **Threshold**.

- We should also know when to **Stop** ( **Max Depth** ) 
- Decision Tree can be **Pruned** if Necessary to **Avoid Overfitting** 

### Information Gain ( Which Feature will be Selected as Root Node ? )

- **High IG** is Better.
- **Information Gain** decides which Feature will become Node and will **Split** the Data further for Building the **Tree**.
- Split with the High **Information Gain** will be Considered as First Split and the process will continue untill **IG** becomes 0

### Gini Index ( Checks for Impurity in the Dataset )

- **Low** Gini Index is Better.
- **Pure** : All Data belongs to **Same** Class in a Subset ( Gini Index : 0 )
- **Impure** : Data is Mixture of **Different** Classes in a Subset.

### Entrophy ( Measure Disorder | Randomness | Uncertainity in Data )

- **Low** Entrophy is Better. ( Easy to Draw Conclusion from Data )
- **High** Entrophy ( Hard to Draw Conclusion from Data )

Advantage of Decision Tree | Disadvantage of Decision Tree
:--- | :---
Handle **Categorical** and **Numerical** Data | Prone to **Overfitting**
No effect of **Outliers** | Need Carefull **Parameter Tuning**
Handle **Non Linear Data** |

> Individual Trees are prone to **Overfitting** but Improves when **Ensembled**.

### How to Avoid Overfitting
- Remove | **Prune** Branches with Less Importance ( Irrelevant Feature )
- Early Stop ( Limit the **Max Depth** of the Tree )

<h3 name='forest'>4. Random Forests ( Ensemble Learning Technique | Bagging )</h3>

- **Merge** a Collection of Parallel Arranged **Independent Decision Trees** to get more **Accurate** and **Stable** Prediction.
- Multiple **Decision Trees** ( Weak Learners ) trained **Parallel** and **Individually**. 
- **Bootstrapped Data Sets** of Orignal Data and **Randomly** selecting **Subsets** at each step. ( **Sampling** with **Replacement** )
- Bagging Technique ( **Multiple** Decision Trees are **Trained** in **Parallel** to Form a **Strong Learner** ) 
- **Prediction** of Model is based on the **Voting** of Decision Trees Output ( **Majority Voting** )
- Reduces Risk of **Error** and **Overfitting**.

<h3 name='svm'>5. Support Vector Machine | SVM</h3>

- SVM can be used for both **Regression** and **Classification** ( but Better use for Classification )
- Finds a Optimal **Line** or **Hyperplane** that Separates the 2 **Distinct** Classes with Maximum **Margin** in **N Dimensional Space**.
- **Hyperplanes** are **Decision Boundaries** that help to Classify the Data Points.
- Data Points are **Support Vectors**.
- SVM can be used for **Linear** and **Non Linear** Data.
- SVM uses **Kernel Trick** for **Non Linear** Data which Creates a **Hyperplane** in **N Dimensional Space** for Linear Seperation.
- Works Better even if Data set has lot of **Outliers** ( Because SVM Focus only on **Support Vectors** closest to the Line  )
- Should be Used if Data Set has lot of **Features** 
- Take Long Time to **Train** and **Predict** if the Number of **Observations** are very Large
- Kernel Functions : Linear | Radial Basis Function ( RBF ) | Polynomial | Exponential

### Benefits 

- SVM also works well with **Unstructured** and **Semi Structured** Data ( Text, Image, Tree )
- **Generalize** Well ( Works well on New Unseen Data )
- Risk of **Overfitting** is Less.

### Disadvantage

- Choosing a **Good Kernel** Function, **Fine Tuning** and even **Visualization** is not easy
- Long **Training Time** for **Large** Datasets.
- Difficult to Understand **Final Model**, Variable Weights and Individual Impact.

<h3 name='knn'>6. K Nearest Neighbours</h3>

- **Multiclass** Classification Algorithm
- Measures the **Geometrical Distance** ( **Euclidean Distance** ) 
- **K** : Initialize **K** ( Number of Nearest **Neigbors** ) 
- Calculate Distance between New **Test** Data Point and **K Nearest Neigbours** of **Training** Data Points
- Sort the **Ordered** Calculated Distance in **Ascending Order**
- Get Nearest ( **Least** Distance ) to it or most **Frequent Classes** in Neighbor
- **Regression** : **Mean** of K Nearest Distances ( Labels )
- **Classification** : **Mode** of K Nearest Distances ( Labels )

<h3 name='naive'>7. Naive Bayes</h3>

- Based on **Conditional Probability** | Class **Prediction** Probability ( Used for **Binary** and **Multiclass** Classification )
- Probabilistic Machine Learning Model ( Likelihood, Prior Probability and Posterior Probability )
- Probability of **Event A** if **Event B** has already occured
- **Naive** : Because it assumes that all of the **Independent Features** are **Independent** from each other
- e.g **Classification** of Dogs Breed ( Naive Bayes tries to Create a **Probability** that the Dog belongs in each Class | Label )
- Weights can be Added to Improve **Accuracy** 

> P( **A** | **B** ) = P( **B** | **A** ) / P( **B** )

All follow Same Process in **Regression** and **Classification** the only difference is in **Output** 

> **Regression** : **Continuous Numerical**

> **Classification**  : **Discrete Categorical**

<h1 name='unsup' align=center>Unsupervised Learning ( Unlabeled Data )</h1>

<table align=center>
  <tr>
    <th><h3>Clustering</h3></th>
    <th><h3>Association</h3></th>
  </tr>
  <tr>
    <td>Group | Cluster | Segment Similar Data</td>
    <td>Identify Set of Items that Occur together in the Dataset</td>
  </tr>
  <tr>
    <td>Group of Customers with Similar Purchasing Behavior</td>
    <td>Customer Buy Product A also tend to Buy Product B</td>
  </tr>
</table>

> Find **Patterns** and **Relationships** between **Independent** Features and **Dependent** Feature ( **Labels** )

> Extract Important Features and Explore the Data Set in Detail.

 <h1 name='cluster' align=center>Clustering</h1>

> Group the Data Set into **Groups** | **Segments** | **Clusters** According to **Similarity**.

> Customer Segmentation | Fraud Detection | Document Classification

### Clustering Techniques

<h3 name='kmean'>1. K Mean Clustering</h3>

- Cluster Data Points with Similar Characteristics in one Cluster
- We Choose **K** number of Clusters
- Select **K** Random Data Points as Centroid
- Data Points nearest to its Corresponding Centroid belongs to that Cluster
- Again the Centroid is Calculated
- The Data Points are Updated based on New Centroid
- **Iterative** Process | Stops when there is no further Classification.
- Different Starting Points ( Random Centroid Selected ) Create Different Clusters 
- **Elbow** Method : Sum of Squared Distance get smaller as the Number of Clusters Increases | Used to Find **Optimal** Number of Clusters

<h3 name='hc'>2. Hierarchical Clustering</h3>

A. Agglomerative
- Bottom Up Approach
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
 
<h3 name="dbscan"> 3. Density Based Clustering </h3>

- **DBSCAN** ( Density Based Spatial Clustering of Applications with **Noise** )
- Groups together Points based on Density ( High Density Region : Points are Close to each other | Finds Neighbors by Density )
- Data Points which are in **Low Density** regions are **Outliers** | Seperate from every other **Data point**
- Clustering methods explains better with Visualization
- Relationships between Features can be represented via Clustering

### B. Dimensionality Reduction

- Aim is to find  the **Important Features** that can be used by our Model for Better Predition.
- Reducing the Number of **Irrelevant Features** that has no relation with the Target Feature.
- There are some Features that brings **Multicollinearity** 
- Feature **Elimination** | **Feature Selection** or Feature **Extraction**
- Save Storage and Time by Improving Performance of Model.
- Due to less number of Features it can be Visualized in 2D and 3D.
- Project Data into Lower Dimension while Preserving as much as Useful Variability ( 19/20 ) as Possible.
- e.g If we Observe a Scatter Plot in Multidimension it will be Complicated for Understanding. 
- Consider only 1 Dimension then It is just a Line and few Points in which some are close to Line and some are bit far away from line.
- Combine Features or Remove Features to Reduce Dimensions.

### Techniques of Dimensionality Reduction

<h3 name='pca'>PCA ( Principal Component Analysis )</h3>

- A **Dimensionality Reduction** Method ( Reduce the **Dimensions** of Large Data Sets )
- **Transforming** a Large Data Set ( More Features ) into Smaller Data Set ( Without Lossing **Accuracy** )
- Smaller Data Sets are Easier to **Explore** and **Visualize** and make Analyzing Data much **Easier** and **Faster** for **Machine Learning Algorithms** 
- **Principal Components** are New Variables that are constructed as **Linear Combinations**
- Combinations are done such a way that New Variables are **Uncorrelated** 
- Most of Information within the Initial Variables is **Compressed** into **First Components**  
- PCA tries to Put **Maximum Possible Information** in **First Component** and then Maximum remaining Information in the Corresponding **Components** 

<h3 name='lda'>LDA ( Linear Discriminant Analysis )</h3>

- Classification | Sperate Data into Different Categories or Classes

<h3 name='tsne'>t-SNE ( t Distributed Stochastic Neighbor Embedding )</h3>

- Non Linear Dimension Reduction ( Spiral, Mixed ) 
- Data which is Complicated for Understanding ( 3 Dimensional )

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

### Standardization 
- Standardize the **Range** of the **Continuous** Initial Variables so that each one of them contributes Equally to the **Analysis**.

![Machine Learning Map](Image/MLMap.jpg)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
