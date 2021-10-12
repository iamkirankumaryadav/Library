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
      Classify Categorical Data
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
    <td></td>
  </tr>
  <tr>
    <th>Dimension Reduction</th>    
    <th>Anomaly Detection</th>    
  </tr>
  <tr>
    <td>
      <ol type=1>
        <li><a href=#pca>PCA</a></li>
        <li><a href=#lda>LDA</a></li>
        <li><a href=#tsne>t-SNE</a></li>
      </ul>
    </td>  
    <td></td>
  </tr>    
</table>

- Features | Independent Variables | Dimensions | Attributes | Inputs | Predictors | Estimators.
- Target | Dependent Variable | Label | Class | Output | Predicted Value | Estimated Value.
- Rows | Observations | Records | Samples.
- `Feature` :  A **measurable** property.
- `Target` : What we want to make **prediction** for.
- `Model` learns a relationship between a `feature matrix` and a `target vector`
- `Model` is the system that makes **predictions** or **classification** on new unseen data.
- `Goal` of machine learning is to build a model that performs well on new data.
- **Parameters** are factors which are considered by the model to make **predictions** or **classification**.
- **Parameters** are tuned to gain **accuracy** with least [**error**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md) and **Assurance** that the model is giving desired expected results. 

### Steps of Machine Learning
1. Gathering Data
2. Explore Data ( Exploratory Data Analysis | **EDA** ) 
3. Preparing Data ( Data Preprocessing | [Missing Data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Missing%20Data.md) | [Outliers](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Outliers.md) | [Categorical Data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Categorical.md) | [Imbalance Data](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Imbalanced%20Dataset.md))
4. Clean Data ( Data Cleaning )
5. Feature Engineering ( Important Features to Train Model | [Transformation](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Normalization%20vs%20Standardization.md) )
6. Choosing a Correct Model
7. Training Data
8. Testing Data and Evaluation ( [**Metrics**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Regression%20Metrics.md) | [Overfitting](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Overfitting.md) )
9. Hyperparameter Tuning
10. Prediction

### Scikit Learn

1. Scikit learn is a great library for creating machine learning model from data.
2. Before you `fit` a model using scikit learn, you data has to be in a recognizable format.
3. Scikit learn works well with `numeric` data that is stored in numpy arrays.
4. It can also convert data from objects like pandas `dataframes` and numpy `arrays`
5. `Feature matrix` is a `2D` grid of data where `rows` represents `samples` and `columns` represents `features`     
6. `Target ector` is usually `1D` vector `column`

<h1 name='sup' align=center>Supervised Learning ( Labeled Data )</h1>

<table align=center>
  <tr>
    <th><h3>Prediction</h3></th>
    <th><h3>Classification</h3></th>
  </tr>
  <tr>
    <th>Predicts a numerical variable</th>
    <th>Predicts a categorical variable</th>
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
    <td><a href="https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Regularization.md"><b>Regularization</b></a> and <a href="https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Regression/Regression%20Metrics.md"><b>Metrics</b></a></td>
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

<h3 name='logreg'>2. Logistic Regression ( <a href='https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Classification/Logistic%20Regression.md'>More</a> )</h3>

- Model used for **classification**.
- Used for tasks like classifying flower species and image recognition.
- One or more independent features is used to **classify** categorical target labels. 
- Dependent ( Output ) should be **categorical** ( 0 or 1 )
- Probability of finite number of outcomes or occurence.

### Advantages of Logistic Regression

- Model **training** and **predictions** are relatively fast.
- No tuning is usually required.
- Performs well with small number of of observations or samples.
 
<h3 name='tree'>3. Decision Tree</h3>

- **Root** Node | Nodes ( Decisions | Conditions | Outcomes ) | Edges | Branches ( Splits of Trees ) | Leaf Node ( Terminal | Label | Class )
- We select the feature as **Node** that **Splits** the data very well.
- Attribute with **High Information Gain** or **Low Entropy** is selected as **Best Attribute** to split.
- Used especially for **Binary** classification and **Multiclass** classification and even used for **Regression**.
- Models where the `Target` variable takes a **Categorical** set of values are **Classification** tree.
- Models where the `Target` variable takes a **Continuous** values are **Regression** Tree.
- **CART** : **C**lassification **A**nd **R**egression **T**ree.
- Growing a tree means deciding which **Feature** to choose ? and what condition to use ? for splitting.
- Continuous can be converted into `Binary` or `Boolean` by setting **Threshold** value.
- We should also know when to **Stop** | **Terminate** ( **Max Depth** ) 
- Decision tree can be **Pruned** if necessary to avoid `Overfitting` 

### Information Gain ( Which Feature will be selected as Root Node ? )

- **High IG** is better.
- **Information Gain** decides which feature will become `Node` and will **Split** the data further for building the **Tree**.
- Split with the high **Information Gain** will be considered as first split and the process will continue untill **IG** becomes 0.

### Gini Index ( Checks for Impurity in the dataset )

- **Low** Gini Index is better.
- **Pure** : All data belongs to **Same** class in a subset ( Gini Index : 0 )
- **Impure** : Data is mixture of **Different** classes in a subset.

### Entrophy ( Measure Disorder | Randomness | Uncertainity in Data )

- **Low** Entrophy is Better. ( Easy to Draw Conclusion from Data )
- **High** Entrophy ( Hard to Draw Conclusion from Data )

Advantage of Decision Tree | Disadvantage of Decision Tree
:--- | :---
Handle **Categorical** and **Numerical** Data | Prone to **Overfitting**
No effect of **Outliers** | Need carefull **Parameter Tuning**
Handle **Non Linear Data** |

> Individual trees are prone to **Overfitting** but improves when **Ensembled**.

### How to Avoid Overfitting
- Remove | **Prune** branches with less importance ( Irrelevant Feature )
- Early stop ( Limit the **Max Depth** of the tree )

<h3 name='forest'>4. Random Forests ( Ensemble Learning Technique | Bagging )</h3>

- **Merge** a collection of `Parallel` arranged **Independent Decision Trees** to get more **Accurate** and **Stable** Prediction.
- Multiple **Decision Trees** ( Weak Learners ) trained `Parallel` and **Individually** | **Independently**. 
- **Bootstrapped Data Sets** of orignal data and **Randomly** selecting subsets at each step. ( **Row Sampling** with **Replacement** )
- Bagging technique ( **Multiple** Decision Trees are trained in `Parallel` to form one **Strong Learner** ) 
- **Prediction** of model is based on the **Voting** of Decision trees output ( **Majority Voting** )
- Reduces risk of **Error** and **Overfitting**.

<h3 name='svm'>5. Support Vector Machine | SVM</h3>

- `SVM` can be used for both **Regression** and **Classification** ( but better used for Classification )
- Finds an optimal **Line** or **Hyperplane** that separates the 2 **Distinct** classes with Maximum **Margin** in **N Dimensional Space**.
- **Hyperplanes** are **Decision Boundaries** that help to `Classify` the data points.
- Data points are **Support Vectors**.
- `SVM` can be used for **Linear** and **Non Linear** Data.
- SVM uses **Kernel Trick** for **Non Linear** Data which creates a **Hyperplane** in **N Dimensional Space** for linear seperation.
- Works better even if data set has lot of **Outliers** ( Because SVM focus only on **Support Vectors** closest to the Line  )
- Should be used if data set has lot of Independent **Features**. 
- Take long time to **Train** and **Predict** if the number of **Observations** are very large.
- Kernel Functions : Linear | Radial Basis Function ( RBF ) | Polynomial | Exponential.

### Benefits 

- SVM also works well with **Unstructured** and **Semi Structured** Data ( Text, Image, Tree )
- **Generalize** well ( Works well on new unseen data )
- Risk of **Overfitting** is less.

### Disadvantage

- Choosing a **Good Kernel** function, **Fine Tuning** and even **Visualization** is not easy.
- Long **Training Time** for **Large** datasets.
- Difficult to understand **Final Model**, variable weights and individual impact.

<h3 name='knn'>6. K Nearest Neighbours</h3>

- **Multiclass** Classification Algorithm.
- Measures the **Geometrical Distance** ( **Euclidean Distance** ) 
- **K** : Initialize **K** ( Number of Nearest **Neigbors** ) 
- Calculate distance between new **Test** data point and **K Nearest Neigbours** of training data points.
- Sort the **Ordered** calculated distance in **Ascending Order**.
- Get nearest | shortest ( **Least** Distance ) to it or most **Frequent Classes** in neighbor.
- **Regression** : **Mean** of K Nearest Distances ( Mean of Labels )
- **Classification** : **Mode** of K Nearest Distances ( Most Frequent Labels )

<h3 name='naive'>7. Naive Bayes</h3>

- Based on **Conditional Probability** | Class **Prediction** Probability ( Used for **Binary** and **Multiclass** Classification )
- Probabilistic Machine Learning Model ( Likelihood, Prior Probability and Posterior Probability )
- Probability of **Event A** if **Event B** has already occured.
- **Naive** : Assumes that all of the **Features** are **Independent** from each other.
- e.g **Classification** of Dogs Breed ( Naive Bayes tries to create a **Probability** that each Dog belongs to seperate Class | Label )
- Weights can be added to improve **Accuracy**. 

> P( **A** | **B** ) = P( **B** | **A** ) / P( **B** )

All follow same process in **Regression** and **Classification** the only difference is in **Output**. 

> **Regression** : **Continuous Numerical**

> **Classification**  : **Categorical**

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
    <td>Customer Buy Phone also tend to Buy Phone Case</td>
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
- Due to less number of Features it can be Visualized in `2D` and `3D`.
- Project Data into Lower Dimension while Preserving as much as Useful Variability ( 19/20 ) as Possible.
- e.g If we Observe a Scatter Plot in Multidimension it will be Complicated for Understanding. 
- Consider only 1 Dimension then It is just a Line and few Points in which some are close to Line and some are bit far away from line.
- Combine Features or Remove Features to Reduce Dimensions.

### Techniques of Dimensionality Reduction

<h3 name='pca'>PCA ( Principal Component Analysis ) ( Unsupervised )</h3> 

- A **Dimensionality Reduction** Method ( Reduce the **Dimensions** of Large Data Sets )
- **Transforming** a Large Data Set ( More Features ) into Smaller Data Set ( Without Lossing **Accuracy** )
- Small Data Sets are **Easy** to **Explore** and **Visualize** and make Analyzing much **Easier** and **Faster** for **ML Algorithms** 
- **Principal Components** are New Variables that are constructed as **Linear Combinations**
- Combinations are done such a way that New Variables are **Uncorrelated** 
- Most of Information within the Initial Variables is **Compressed** into **First Components**  
- PCA tries to Put **Maximum Possible Information** in **First Component** and then Maximum remaining Information in the Corresponding **Components** 

<h3 name='lda'>LDA ( Linear Discriminant Analysis ) ( Supervised )</h3>

- Classification | Sperate Data into Different Categories or Classes
- LDA Creates **New Axis** ( **Maximize** the **Distance** between **Means** of **Two Classes** and **Minimize Variation** within each Class )

<h3 name='tsne'>t-SNE ( t Distributed Stochastic Neighbor Embedding )</h3>

- Non Linear Dimension Reduction ( Spiral, Mixed ) 
- Data which is Complicated for Understanding ( Multi Dimensional Data )
- A Tool to **Visualize** and **Explore** High Dimension Data.
- Identify **Clusters** based on Similarity of Data Points.
- Maps **Multi Dimensional Data** to a **Lower Dimensional Space**. 

### Anomaly Detection :
- Automatically Discover **Unusual** Data Points in Data Set.
- Used to Find Fraudulent Transactions, Identify an `Outlier` caused by Human Error during Data Entry.
- Reduces Complexity of Data and Helps to Understand Data more Clearly and Better Way.

### Association Mining :
- Set of Items that Frequently Occur together in Data Set.
- Basket Analysis : Items Bought Together | Goods Purchased at the Same Time Help to Develop Marketing Strategies.

### Feature Selection
- **Select** Important Features | Helps to Improve **Accuracy** | Not Every Feature Adds Value to Solve Problem.
- **Understanding** Each Feature before using it for Creating Machine Learning Model.
- **Correaltion** between **Features** and **Target** helps to Select Better Features.
- **Ensemble Learning Techniques** have a Parameter of **feature_importance** which helps us to find Important Features.

### Standardization 
- Standardize the **Range** of the **Continuous** Initial Variables so that each one of them contributes Equally to the **Analysis**.

![Machine Learning Map](Image/MLMap.jpg)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
