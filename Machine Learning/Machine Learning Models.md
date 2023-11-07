<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

<h1 align="center">Machine Learning Models 🤖🚀💻</h1>

<h4 align="center"><code>ML</code> is a technique to implement <code>AI</code> that can learn from data by themselves without being explicitly programmed</h4>

<h3 align="center">Machine Learning Map</align></h3>
  
<table align="center">
  <tr>
    <th colspan=1>
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
      <a href='#cluster'>Clustering</a>
    </th>
    <th>
      Association
    </th>
  </tr>
  <tr>
    <th>
      Predict continuous numerical data | Classify discrete categorical data
    </th>
    <th>
      Group similar data 
    </th>
    <th>
      Identify similar data
    </th>
  </tr>
  <tr>    
    <td rowspan=3>
      <ol type=1>
        <li><a href=#reg>Linear Regression</a></li>
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
        <li><a href=#knn>K Nearest Neighbors</a></li>
        <li><a href=#naive>Naive Bayes</a></li>
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

Supervised | Unsupervised | Reinforcement
:--- | :--- | :---
Algorithm learns from `labelled` data | Algorithm learns from `unlabelled` data | `Agents` takes `actions` in an environment
Algorithm tries to find `relationships` and `mappings` | Algorithm tries to find `patterns` | Agent learn from `rewards` and `penalty`

- Columns - Feature Matrix ( Variables ) and Target Vector ( Labels )
- Features - Independent Variable | Dimensions | Attributes | Inputs | Predictors | Estimators | Characteristics.
- Target - Dependent Variable | Label | Class | Output | Predicted Value | Estimated Value | Response.
- Rows | Observations | Records | Samples | Instance.
- `Feature` :  A **measurable** property, can be categorical ( discrete ) or numerical ( real or int number )
- `Target` : What we want to make **prediction** for.
- `Model` learns a relationship between a `feature matrix` and a `target vector`
- `Model` is the system that makes **predictions** or **classification** on new unseen data.
- `Goal` of machine learning is to build a model that performs well on new data.
- **Parameters** are factors which are considered by the model to make **predictions** or **classification**.
- **Parameters** are tuned to gain **accuracy** with least [**error**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md).

### Scikit Learn

1. Scikit learn is a great library for creating `machine learning model` from data.
2. Before you `fit` a model using scikit learn, you data has to be in a recognizable format.
3. Scikit learn works well with `numeric` data that is stored in `NumPy arrays`
4. It can also convert data from objects like `Pandas : dataframes` and `NumPy : arrays`
5. `Feature matrix` is a `2D` grid of data where `rows` represents `samples` and `columns` represents `features`     
6. `Target vector` is usually `1D` vector `column`

<h1 name='sup' align=center>Supervised Learning ( Labeled Data )</h1>

- `Machine Learning` that involves training a model using `labeled` data.
- Algorithm learns to recognize `patterns` in the input data and map them to the correct output based on the labeled data.
- Goal of supervised learning is to create a model that can accurately predict the output for new, unseen input data.
- Supervised learning is useful for `classification` and `regression` problems.

<table align=center>
  <tr>
    <th><h3>Regression</h3></th>
    <th><h3>Classification</h3></th>
  </tr>  
  <tr>
    <td>Predicting a quantity or continuous values.</td>
    <td>Predicting a class or discrete values.</td>
  </tr>
  <tr>
    <td>e.g. Salary, Age, Price, Temperature, Rainfall, etc.</td>
    <td>e.g. Male or Female, True or False, Dog or Cat, etc.</td>
  </tr>
  <tr>
    <td>Better algorithms: Decision Tree, Random Forest, KNN</td>
    <td>Better algorithms: Logistic, Polynomial, SVM</td>
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
    <td colspan=3>One or more <b>Independent Features</b> is used to predict <b>continuous dependent numeric variable</b></td>
  </tr>
  <tr>
    <td colspan=3>Dependent Variable | Target | Output should be <b>Continuous</b></td>
  </tr>
</table>

<h3 name='linreg'>1. Linear Regression</h3>  

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/02.Linear%20Regression.ipynb)

![Equation of Line](Image/EquationLine.png)

- Linear regression uses a straight line to predict the value of a dependent variable from an independent variable.
- The straight line is called the regression line. Formula: `y = mx + c`
- Linear regression is used when there is a linear relationship between the two variables.
- The relationship can be described by a straight line, it uses existing data to train the model.

<h1 name='class' align=center>Classification</h1>

<h3 name='logreg'>2. Logistic Regression (<a href='https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Classification/Logistic%20Regression.md'>More</a> )</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/04.Logistic%20Regression.ipynb)

- Model used for `classification` tasks like classifying flower species and image recognition.
- One or more independent features are used to **classify** `categorical` target labels. 
- Dependent ( Output ) should be `categorical` ( 0 or 1 )
- `Probability` of a finite number of outcomes or occurrences.

### Advantages of Logistic Regression

- Model `training` and `predictions` are relatively fast, no tuning is usually required.
- Performs well with a small number of observations or samples.

### Logistic Regression for Multiclass Classification

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/05.Logistic%20Regression%20for%20Multiclass%20Classification.ipynb)

- Split the task into multiple binary classification datasets.
- **Fit** a binary classification ( Logistic Regression ) model on each.
- One vs Rest (`OvR`) or One vs All (`OvA`) is a technique that extends binary classification to **multiclass**.
- Digit `0` vs Digit `1`, `2` and `3`
- Digit `1` vs Digit `0`, `2` and `3`
- Digit `2` vs Digit `0`, `1` and `3`
- Digit `3` vs Digit `0`, `1` and `2`
The model that predicts the **highest** class probability is the predicted class.
  
<h3 name='tree'>3. Decision Tree</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/06.Decision%20Tree.ipynb)

- `Root Node`: `Decisions` | `Conditions` | `Outcomes`
- `Edges`: `Branches` | `Splits`
- `Leaf Node`: `Terminal` | `Label` | `Class`
- The `Decision Tree` recursively splits the data into smaller subsets based on the values (Continuous or Discrete) of input variables.
- At each split, the algorithm chooses the best variable to split the data on and then splits the data into two subsets based on the values of that variable.
- The process continues until the data is split into subsets that are pure.
- Once the data is split into pure subsets, the decision tree can be used to make predictions for new data points. 
- We select the feature as `node` that **splits** the data very well.
- Attribute with `High Information Gain` or `Low Entropy` or `Low Gini Index` is selected as `best attribute` to split.
- Used especially for `binary` classification and `multiclass` classification and even used for `Regression`
- Models, where the `target` variable takes a `categorical` set of values, are a `classification` tree.
- Models, where the `target` variable takes a `continuous` value, are `regression` Tree.
- `CART` : **C**lassification **A**nd **R**egression **T**ree.
- Growing a tree means deciding which `feature` to choose and what condition to use? for splitting.
- `Continuous` can be converted into `binary` or `boolean` by setting the `threshold` value.
- We should also know when to `stop` | `terminate` ( **Max Depth** ) to prevent from `overfitting`
- Decision tree can be `pruned` if necessary to avoid `overfitting`

```python
from sklearn.tree import DecisionTreeClassifier
```

### `Information Gain` ( Which Feature will be selected as Root Node ? )

- `High Information Gain` is better ( Explains the split very well )
- `Information Gain` decides which feature will become `Node` and will `split` the data further for building the **tree**.
- Split with the `High Information Gain` will be considered as the first split and the process will continue until **IG** becomes 0.

### `Gini Index` ( Checks for `Impurity` in the dataset )

- `Low Gini Index` is better.
- `Pure`: All data belongs to the `same` class in a subset ( Gini Index = 0 )
- `Impure`: Data is a mixture of `different` classes in a subset.

### `Entrophy` ( Measure Disorder | Randomness | Uncertainity in Data )

- `Low Entropy` is better. ( Easy to draw conclusions from data )
- `High Entropy` ( Hard to draw conclusions from data )

Advantage of Decision Tree | Disadvantage of Decision Tree
:--- | :---
Handle `categorical` and `numerical` data | Prone to `overfitting`
No effect of `outliers` | Need careful **parameter tuning**
Handle **non linear data** |

### Individual trees are prone to `overfitting` but improve when `ensembled`

### How to Avoid Overfitting?
- Remove | `Prune` branches with less importance ( Irrelevant Feature )
- Early stop ( Limit the `Max Depth` of the tree )

<h3 name='forest'>4. Random Forests ( Ensemble Learning Technique | Bagging )</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/09.Random%20Forest.ipynb)

- An ensemble learning method that uses multiple `decision trees` for both `regression` and `classification`
- Ensemble learning algorithms combine the predictions of multiple models to produce a more accurate prediction.
- Once the decision trees are trained, they are used to predict new data points.
- Each decision tree is built using a random subset of the training data ( feature matrix )
- Multiple `decision trees` ( weak learners ) are trained `parallel` and `individually` | `independently`
- `Bootstrapping` ( Row sampling with replacement ): Subsets are randomly selected from the original dataset.
- `Majority Voting`: `Prediction` of the model is based on the **voting** of decision tree outputs.
- `Regression`: The mean/average of the predictions of all the decision trees are considered.
- `Classification`: The class selected by most of the decision trees are considered.
- Random forest creates a model that is more accurate and less prone to `overfitting` than a single decision tree.
- `Bagging`: Multiple decision trees are trained in `parallel` to form one strong accurate predicting model.
- Adding multiple decision trees reduces the risk of `error` and `overfitting` by reducing the variance.
- Random forests are accurate, robust to `overfitting`, used for both `regression` and `classification`. Can be trained on data of any type (numerical, categorical, and ordinal data)

```python
from sklearn.ensemble import RandomForestClassifier
```

<h3 name='svm'>5. Support Vector Machine | SVM</h3>

- Support Vector Machine is used for both `regression` and `classification`
- Finds an optimal `line` or `hyperplane` that separates the 2 distinct classes with `maximum margin` in `N dimensional space`
- `Hyperplanes` are decision boundaries that help to `classify` the data points. Data points are called `Support Vectors`
- `SVM` can be used for `linear` and `non linear` regression and classification.
- `SVM` can manage high dimensional data and nonlinear relationships between the data points.
- `SVM` uses `kernel trick` for `non linear` data which creates a `hyperplane` in `N dimensional space` for linear seperation.
- Works better even if data set has lot of `outliers` ( Because SVM focus only on `support vectors` closest to the line  )
- Take long time to `train` and `predict` if the number of `observations` are very large.
- Kernel functions : Linear | Radial basis function ( RBF ) | Polynomial | Exponential.

### Benefits 

- SVM works well with `unstructured` and `semi-structured` data ( text, image, face, anomaly detections, etc. )
- `Generalize` well on the new unseen data and risk of `overfitting` is also less.

### Disadvantage

- Choosing a `good Kernel` function, `fine tuning` and even `visualization` is challenging.
- Difficult to understand the `final model`, variable `weights` have individual impact.

<h3 name='knn'>6. K Nearest Neighbours</h3>

- `KNN` is used for both `regression` and `classification`
- `KNN` measures the `geometrical distance` ( euclidean distance ) 
- Initialize `K` ( `# nearest neighbours` ) 
- Calculate the distance between new data points and `K nearest neigbours` of training data points.
- Sort the calculated distance in `ascending` order and get `the shortest distance or `most frequent` classes in neighbour.
- `Regression`: `Mean` of K nearest distances are considered.
- `Classification`: `Mode` of K nearest distances are considered.

<h3 name='naive'>7. Naive Bayes</h3>

- Naive Bayes is a `probabilistic classifier`, based on `Class Prediction Probability` ( `Binary` and `Multiclass` classification )
- Creates the `conditional probability distribution` for all the classes independently.
- `Naive`: Assumes that all of the `features` are `independent` from each other ( No correlation between any feature )
- e.g `Classification` of Dogs Breed ( Naive Bayes tries to create a `probability` that each Dog belongs to separate `Class` )
- `Weights` can be added to improve `accuracy`

> P( **A** | **B** ) = P( **B** | **A** ) / P( **B** )

All follow the same process in **Regression** and **Classification** the only difference is in **Output**. 

> **Regression** : **Continuous Numerical**

> **Classification**  : **Categorical**

<h1 name='unsup' align=center>Unsupervised Learning ( Unlabeled Data )</h1>

<table align=center>
  <tr>
    <th><h3>Clustering</h3></th>
    <th><h3>Association</h3></th>
  </tr>
  <tr>
    <td>Group | Cluster | Segment similar data points.</td>
    <td>Identify a set of items that occur together in the dataset.</td>
  </tr>
  <tr>
    <td>Grouping the similar data points.</td>
    <td>Find important relationships between data points.</td>
  </tr>
  <tr>
    <td>Group of customers with similar purchasing behaviour.</td>
    <td> Customers who buy phones also tend to buy cases.</td>
  </tr>
  <tr>
    <td>Better algorithms: K Means, Hierarchical, PCA</td>
    <td>Better algorithms : Apriori</td>
  </tr>
</table>

- Find `patterns` and `relationships` between **feature matrix**.
- Extract important features and explore the dataset in detail.
- Unsupervised algorithms don't make **predictions** from the data.
 
 <h1 name='cluster' align=center>Clustering</h1>

- Find some underlying `pattern` and `structure` in data.
- Groups the data points into **segments** or **clusters** based on **similarity**.
- Customer Segmentation | Fraud Detection | Document Classification

### Clustering Techniques

<h3 name='kmean'>1. K Mean Clustering</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/10.K%20Mean%20Clustering.ipynb)

- Cluster data points with similar characteristics in one cluster.
- We choose **K** number of clusters.
- Select **K** random data points as `centroid`
- Data points nearest to its corresponding `centroid` belong to that **cluster**.
- Again the `centroid` is calculated, and the data points are updated based on the new `centroid`
- **Iterative** Process | Stops when there is no further classification.
- Different starting points ( Random centroid selected ) Create different clusters. 
- **Elbow** Method: The sum of squared distance gets smaller as the number of clusters increases.  
- The `Elbow` method helps to find the **optimal** number of clusters.

<h3 name='hc'>2. Hierarchical Clustering</h3>

 Groups data points into a `hierarchy` of clusters. 

A. Agglomerative
- Bottom-Up Approach
- `AGNES`: **Ag**glomerative **Nes**ting
- Starts with treating each data point as a part of its own individual cluster.
- After each iteration, similar and closest clusters are merged with each other, until there is only one cluster remaining.

B. Divisive
- Top Down Approach
- **DIANA** ( **Di**vise **Ana**lysis )
- Starts with all the data points in a single cluster.
- After each iteration, it splits the large clusters into two smaller clusters, until each cluster contains only one data point.

### How do we Calculate the similarity between the clusters?
- `MIN`: Distance between the closest data points of two clusters.
- `MAX`: Distance between the farthest data points of two clusters.
- `AVG`: Average distance between each data point of two clusters.
- `Centroids`: Distance between the centroid of two clusters.
 
<h3 name="dbscan"> 3. Density Based Clustering </h3>

- `DBSCAN` ( Density-Based Spatial Clustering of Applications with **Noise** )
- Group similar data points together based on density.
- High Density Region: Points are `close` to each other | High neighbours within the radius.
- Data points in `low density` regions are `outliers`.
- Clustering methods explain better with visualization. e.g. Scatter Plot.
- Relationships between features can be represented via clustering.

### B. Dimensionality Reduction

- A technique used to reduce the number of `features` or `variables` in a dataset while retaining the most important information.
- The aim is to find the **important features | variables** that the model can use for better prediction.
- Reducing **irrelevant features** that have no relation with the target feature.
- There are some features that bring `Multicollinearity`
- **Feature Elimination** | **Feature Selection** or **Feature Extraction**
- Save storage and time by improving the performance of the model.
- Due to less number of features it can be visualized in `2D` and `3D`.
- Project data into lower dimensions while preserving as much useful variability ( 19/20 ) as possible.
- e.g. If we observe a `Scatter Plot` in multi-dimension it will be complicated for understanding. 
- Consider only 1D then it is just a line and a few points in which some are close to the line and some are a bit far away from the line.
- Combine features or remove features to reduce dimensions.

### Techniques of Dimensionality Reduction

<h3 name='pca'>PCA ( Principal Component Analysis ) ( Unsupervised )</h3> 

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/11.PCA.ipynb)

- Transforms a dataset into a new set of variables without loosing information called principal components.
- PCA aims to capture the most important patterns or relationships in the data while reducing its dimensionality.
- Reduce the **dimensions** of large dataset.
- Small data sets are **easy** to **explore** and **visualize**.
- **Analyzing** and **training** is also much **easier** and **faster**.
- First principal component is the linear combination that explains the largest amount of variation in the data.
- Subsequent principal components explain decreasing amounts of variation.
- Most of the informations within the initial variables are **compressed** into **first components**.  
- PCA tries to put **maximum possible information** in **first component**. 
- And then remaining information in the corresponding **components**.
- `PCA` is effected by scale, so scaling of features before applying `PCA` is important.
- Reconstruct the original data from the reduced dimensional representation by using a subset of the principal components.
- This reconstruction is an approximation of the original data but captures the essential characteristics.

<h3 name='lda'>LDA ( Linear Discriminant Analysis ) ( Supervised )</h3>

- Classification | Sperate Data into Different Categories or Classes
- LDA Creates **New Axis** ( **Maximize** the **Distance** between **Means** of **Two Classes** and **Minimize Variation** within each Class )

<h3 name='tsne'>t-SNE ( t Distributed Stochastic Neighbor Embedding )</h3>

- Non-Linear Dimension Reduction ( Spiral, Mixed ) 
- Data which is Complicated for Understanding ( Multi-Dimensional Data )
- A Tool to **Visualize** and **Explore** High Dimension Data.
- Identity **Clusters** based on Similarity of Data Points.
- Maps **Multi Dimensional Data** to a **Lower Dimensional Space**. 

### Anomaly Detection :
- Automatically Discover **Unusual** Data Points in Data Set.
- Used to Find Fraudulent Transactions and identify an `Outlier` caused by Human Error during Data Entry.
- Reduces Complexity of Data and Helps to Understand Data more Clearly and Better Way.

### Association Mining :
- Set of Items that Frequently Occur together in a Data Set.
- Basket Analysis: Items Bought Together | Goods Purchased at the Same Time Help to Develop Marketing Strategies.

### Feature Selection
- **Select** Important Features | Helps to Improve **Accuracy** | Not Every Feature Adds Value to Solve Problem.
- **Understanding** Each Feature before using it for Creating a Machine Learning Model.
- **Correaltion** between **Features** and **Target** helps to Select Better Features.
- **Ensemble Learning Techniques** have a Parameter of **feature_importance** which helps us to find Important Features.

### Standardization 
- Standardize the **range** of the **continuous** variables so that each one of them contributes equally to the **analysis**.

![Machine Learning Map](Image/MLMap.jpg)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
