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
              <li><a href=#adaboost>ADABOOST</a></li>
              <li><a href =#gbm>Gradient Boosting</a></li>
              <li><a href=#xgboost>XGBOOST</a></li>
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
The algorithm tries to find `relationships` and `mappings` | Algorithm tries to find `patterns` | Agent learns from `rewards` and `penalty`

- Columns - Feature Matrix ( Variables ) and Target Vector ( Labels )
- Features - Independent Variable | Dimensions | Attributes | Inputs | Predictors | Estimators | Characteristics.
- Target - Dependent Variable | Label | Class | Output | Predicted Value | Estimated Value | Response.
- Rows | Observations | Records | Samples | Instance.
- `Feature`:  A **measurable** property, that can be categorical ( discrete ) or numerical ( real or int number )
- `Target`: What we want to make **prediction** for.
- `Model` learns a relationship between a `feature matrix` and a `target vector`
- `Model` is the system that makes **predictions** or **classification** on new unseen data.
- The goal of machine learning is to build a model that performs well on new data.
- **Parameters** are factors which are considered by the model to make **predictions** or **classification**.
- **Parameters** are tuned to gain **accuracy** with least [**error**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md).

### Scikit Learn

1. Scikit Learn is a great library for creating a `machine learning model` from data.
2. Before you `fit` a model using Scikit Learn, your data must be in a recognizable format.
3. Scikit Learn works well with `numeric` data that is stored in `NumPy arrays`
4. It can also convert data from objects like `Pandas: data frames` and `NumPy: arrays`
5. `Feature matrix` is a `2D` grid of data where `rows` represents `samples` and `columns` represent `features`     
6. `Target vector` is usually a `1D` vector `column`

<h1 name='sup' align=center>Supervised Learning ( Labeled Data )</h1>

- `Machine Learning` that involves training a model using `labelled` data.
- The algorithm learns to recognize `patterns` in the input data and map them to the correct output based on the labelled data.
- The goal of supervised learning is to create a model that can accurately predict the output for new, unseen input data.
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

- Linear Regression finds the relationship between the dependent variable and one or more independent variables.
- Linear Regression finds the best fit straight line that accurately predicts the output values within a range.
- The straight line is called the `regression line`
- Formula: `y = mX + c`, here `y` is the dependent variable and `X` is the independent variable.
- `m` is the **slope** and `c` is the **y-intercept**, both are the **regression coefficients**.
- Linear Regression is simple to understand and interpret, with fast training and prediction.
- Linear Regression assumes a linear relationship between variables, sensitive to outliers.
- Can suffer from multicollinearity if the dataset has highly correlated variables.

**Hyperparameters:**

1. **Alpha:**
- Used in Lasso `L1` and Ridge `L2` regression, determines the strength of the regularization.
- A higher value of `alpha` means more regularization and simpler linear models.
- For `αlpha = 0`, Ridge regression is just linear regression.
- The best value for `alpha` is found by cross-validation (Grid Search CV or Random Search CV)

2. **Normalization:**
- If `True`, the independent variable `X` will be normalized before regression by subtracting the `mean`

3. **Fit Intercept:**
- Whether to calculate the intercept `c` for this model.
- If set to False, no intercept will be used in calculations.
 
<h1 name='class' align=center>Classification</h1>

<h3 name='logreg'>2. Logistic Regression (<a href='https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Classification/Logistic%20Regression.md'>More</a> )</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/04.Logistic%20Regression.ipynb)

- Model used for `classification` tasks like classifying flower species and image recognition.
- One or more independent features are used to **classify** `categorical` target labels.
- The outcome is measured with a `dichotomous` variable (Only two possible outcomes)
- It predicts the probability of occurrence of an event by fitting data to a `logit` function.
- Dependent ( Output ) should be `categorical` (0 or 1, Yes or No, True or False)
- Widely used for binary classification, simple and requires less training, rescaling provides better accuracy.

### Advantages of Logistic Regression

- Model `training` and `predictions` are relatively fast, no tuning is usually required.
- Performs well with a small number of observations or samples.

### Logistic Regression for Multiclass Classification

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/05.Logistic%20Regression%20for%20Multiclass%20Classification.ipynb)

- Split the task into multiple binary classification datasets.
- **Fit** a binary classification ( Logistic Regression ) model on each label.
- One vs Rest (`OvR`) or One vs All (`OvA`) is a technique that extends binary classification to **multiclass**.
- Digit `0` vs Digit `1`, `2` and `3`
- Digit `1` vs Digit `0`, `2` and `3`
- Digit `2` vs Digit `0`, `1` and `3`
- Digit `3` vs Digit `0`, `1` and `2`
- The model that predicts the **highest** class probability is the predicted class.
  
<h3 name='tree'>3. Decision Tree</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/06.Decision%20Tree.ipynb)

- `Root Node`: Represents the entire sample and this further gets divided into two or more homogeneous sets.
- `Edges` | `Branches` | `Splits` | `Decisions` | `Conditions` | `Outcomes` | `Sub Tree`
- `Leaf Node` | `Terminal` | `Label` | `Class`: Nodes that do not split further.
- The `Decision Tree` recursively splits the data into smaller subsets based on the values (Continuous or Discrete) of input variables.
- At each split, the algorithm chooses the best variable to split the data into two subsets based on the values of that variable.
- The process continues until the data is split into pure subsets (Which can't be split further)
- Once the data is split into pure subsets, the decision tree can be used to make predictions for new data points.
- Decision Trees are used to make predictions on new data by traversing the tree, the terminal node represents the predicted outcome.
- The tree is built by selecting the best split at each node, based on measures of impurity, such as the `Gini Index` or `IG`
- Attribute with `High Information Gain` or `Low Entropy` or `Low Gini Index` is selected as `best attribute` to split.
- The path from the root to a leaf node represents a set of rules that will be used to classify new instances.
- Used especially for `binary` Classification and `multiclass` Classification and even used for `Regression`
- Models, when the `target` variable has a `categorical` set of values, a `classification` tree is used.
- Models, when the `target` variable has a `continuous` value, a `regression` tree is used.
- `CART` : **C**lassification **A**nd **R**egression **T**ree.
- Decision Tree is prone to `overfitting`, resulting in poor performance on the test data.
- Pruning: When we remove unnecessary sub-nodes of a decision node.
- Pruning reduces the complexity, overfitting, and improves its generalization performance.
- Growing a tree means deciding which `feature` to choose and what condition to use? for splitting.
- `Continuous` can be converted into `binary` or `boolean` by setting the `threshold` value.
- We should also know when to `stop` | `terminate` ( **Max Depth** ) to prevent from `overfitting`
- Decision tree can be `pruned` if necessary to avoid `overfitting`

**Advantages:**
- Easy to visualize and understand, they can also handle missing data.
- Don't require extensive data preprocessing such as `normalization` or `scaling`
- Capture non-linear relationships between the target vector and the feature matrix.
- Robust to outliers and can handle them well.

```python
from sklearn.tree import DecisionTreeClassifier
```

### `Information Gain` (Which Feature will be selected as Root Node?)

- `High Information Gain` is better (Explains the split very well)
- `Information Gain` decides which feature will become `Node` and will `split` the data further for building the **tree**.
- Split with the `High Information Gain` will be considered as the first split and the process will continue until **IG** becomes 0.

### `Gini Index` (Checks for `impurity` in the dataset)

- `Low Gini Index` is better.
- `Pure`: All data belongs to the `same` class in a subset (Gini Index = 0)
- `Impure`: Data is a mixture of `different` classes in a subset.

### `Entrophy` (Measure Disorder | Randomness | Uncertainity in Data)

- `Low Entropy` is better. (Easy to conclude data)
- `High Entropy`

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

- Random sampling (Bootstrap Aggregation with replacement)
- An ensemble learning method that uses multiple `decision trees` for both `regression` and `classification`
- Ensemble learning algorithms combine the predictions of multiple decision trees to produce a more accurate prediction.
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
- Random forests are accurate, robust to `overfitting`, used for both `regression` and `classification`.
- Random forest can be trained on data of any type (numerical, categorical, and ordinal data)

**Advantages:**
- RF can handle large datasets with high features and can provide accurate results.
- RF can handle non-linear relationships between features and target variables.
- RF can handle missing values in the data.
- RF performs feature selection by building multiple decision trees.
- Each tree is built using a random selection of features and observations from the dataset.
- Feature sampling ensures that different trees in the random forest use different subsets of features during training.
- This allows the RF to capture a wider range of patterns and relationships within the data.
- Each tree in the random forest can calculate the importance of a feature (feature_importances_)
- A feature that decreases the impurity is an important feature of the model.

```python
from sklearn.ensemble import RandomForestClassifier
```

<h3 name='adaboost'>ADABOOST( Adaptive Boosting)</h3>

- AdaBoost iteratively trains a sequence of weak decision trees.
- Gives more weight to the data points that are misclassified in each iteration.
- AdaBoost can significantly enhance the accuracy of models, especially when dealing with complex datasets.
- AdaBoost is effective in handling class imbalance.
- Doesn't require extensive hyperparameter tuning.
- AdaBoost implicitly performs feature selection by assigning more importance/weights to relevant features.
- Primarily used for classification tasks. Not well suited for regression tasks.

<h3 name='gbm'>GBM ( Gradient Boosting Method)</h3>

- Gradient boosting combines the ideas of boosting (combining weak learners to create a strong learner) with gradient descent.
- A method used to minimize errors in predictions. It's primarily used in regression and classification problems.
- Loss function: Measures how far the model's predictions are from the actual values.
- Gradient boosting algorithms aim to minimize this loss function.
- Gradient Descent: An iterative optimization algorithm is used to minimize the loss function.

Algorithm Steps:
- **Initialize with a Base Model:** Starts with a simple model (decision tree) to make initial predictions.
- **Compute the Residuals:** Calculate the difference between predicted and actual values (residuals)
- **Build a New Model:** Construct a new model to predict the residuals from the previous model.
- **Update the Model:** Update the model's predictions by adding the new model's predictions to the previous predictions.
- **Minimize Loss Function:** Use gradient descent to find the model that minimizes the loss function.
- Repeat the process for a specified number of iterations, until the loss function stops decreasing.

<h3 name='xgboost'>XGBOOST( Extreme Gradient Boosting)</h3>

- An advanced implementation of the gradient boosting algorithm.
- It is scalable and highly efficient and is used for its speed and performance.
- XGBoost improves upon the traditional gradient boosting method.
- XGBoost optimizes the computational process and adds enhancements like regularization.
- Efficiently handles a large number of features and large-scale datasets.
- Works well for both regression and classification problems.
- Regularization features help in reducing overfitting, often leading to better accuracy.
- Automatically handles missing values, reducing the need for extensive data preprocessing.
- Can be more complex and challenging to tune.
- If not properly regularized or if trained for too many iterations, it can overfit the training data.


<h3 name='svm'>5. Support Vector Machine | SVM</h3>

- Aims to find an optimal `hyperplane` that classifies the distinct classes with `maximum margin` in `N-dimensional space`
- `Hyperplanes` are decision boundaries that help to `classify` the data points. Data points are called `Support Vectors`
- `SVM` can be used for `linear` and `non-linear` regression and classification.
- `SVM` can manage high dimensional data and nonlinear relationships between the data points.
- `SVM` uses `kernel trick` for `non-linear` data which creates a `hyperplane` in `N-dimensional space` for linear separation.
- Works better even if the data set has a lot of `outliers` ( Because SVM focus only on `support vectors` closest to the line  )
- Take a long time to `train` and `predict` if the number of `observations` is very large.
- Kernel functions : Linear | Radial basis function ( RBF ) | Polynomial | Exponential.

### Benefits 

- SVM works well with `unstructured` and `semi-structured` data ( text, image, face, anomaly detections, etc. )
- `Generalize` well on the new unseen data and the risk of `overfitting` is also less.

### Disadvantage

- Choosing a `good Kernel` function, `fine tuning` and even `visualization` is challenging.
- Feature scaling (normalization/standardization) is important for better accuracy.
- Not suitable for larger datasets, training can be time and resource-consuming.
- Difficult to understand the `final model`, variable `weights` have individual impact.

<h3 name='knn'>6. K Nearest Neighbours</h3>

- `KNN` is used for both `regression` and `classification`
- `KNN` measures the `geometrical distance` ( euclidean distance ) between the data points. 
- Initialize `K` ( `# nearest neighbours` ) 
- Calculate the distance between new data points and the `K nearest neighbours` of training data points.
- e.g. if K = 5, it will calculate the distance from the 5 nearest data points.
- Sort the calculated distance in `ascending` order and get `the shortest distance or `most frequent` classes in neighbour.
- `Regression`: `Mean` of K nearest distances are considered.
- `Classification`: `Mode` of K nearest distances are considered.

<h3 name='naive'>7. Naive Bayes</h3>

- Naive Bayes is a `probabilistic classifier`, based on `Class Prediction Probability` ( `Binary` and `Multiclass` classification )
- Creates the `conditional probability distribution` for all the classes independently.
- `Naive`: Assumes that all of the `features` are `independent` from each other ( No correlation between any feature )
- e.g `Classification` of Dogs Breed ( Naive Bayes tries to create a `probability` that each Dog belongs to a separate `Class` )
- `Weights` can be added to improve `accuracy`
- P(Class | Data) = (P(Data | Class) * P(Class)) / P(Data)
- P(Class | Data): Probability after observing the data (Posterior Probability)
- P(Data | Class): Likelihood
- P(Class): Probability before observing the data (Prior Probability)
- Classification: Spam email, Dogs Breed Image, and Customer likely to churn.
- Regression: House price, Product Sales, and Customer lifeline.
- Anomaly detection: Detecting fraudulent transactions, Network intrusion, and Outlier detection.  

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

- Groups data points into a specified number of clusters.
- Data points with similar characteristics are grouped in one cluster.
- We choose the `K` number of clusters and select `K` random data points as `centroid` (centre of cluster) as centroid for each cluster.
- Data points nearest to its corresponding `centroid` belong to that cluster.
- Again the `centroid` is calculated, and the data points are updated based on the new `centroid`
- This is an iterative process, we stop when there is no further classification.
- Different starting points ( Random centroid selected ) create different clusters. 
- `Elbow Method`: The sum of squared distance gets smaller as the number of clusters increases.  
- The `Elbow` method helps to find the `optimal` number of clusters.

Steps of K Mean Clustering:
1. Choose the number of clusters (K): This depends on the nature of the data and the desired granularity of the clusters.
2. Initialize the centroids: Randomly select K data points as the initial centroids.
3. Assign data points to the nearest clusters: Forming K clusters.
4. Recalculate centroids: Calculate the new centroid for each cluster  (mean of the data points of the cluster)
5. Repeat 3 and 4 until we cannot find any new centroid after recalculation.

Advantages:
1. Simple to understand and implement.
2. Efficient and can be applied over large data sets.
3. Versatile unsupervised ML algorithm that can be used for data exploration and clustering.

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
 
<h3 name="dbscan"> 3. Density Based Clustering</h3>

- `DBSCAN`: Density-based spatial clustering of applications with noise (outliers).
- Group similar data points together based on density (data points that are closely packed together).
- High Density Region: Points are `close` to each other | High neighbours within the radius.
- Unlike other clustering algorithms, DBSCAN does not require a predefined number of clusters.
- Data points in `low density` regions are `outliers`.
- Visualization can explain the clustering methods in a better way i.e. scatter plot. 
- DBSCAN can effectively identify clusters of arbitrary shapes and sizes.

DBSCAN defines 3 types of data points based on their density and proximity.
1. Core points: Data points that are very close to each other.
2. Border points: Data points that are neighbours but not too close to each other.
3. Noise points: Data points that are very far away from the rest of the data points (Outliers)

### B. Dimensionality Reduction

- A technique used to reduce the number of `features` or `variables` in a dataset while retaining the most important information.
- The aim is to find the **important features | variables** that the model can use for better prediction.
- Reducing **irrelevant features** that have no relation with the target feature.
- Some features bring `Multicollinearity`
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

- Transforms a dataset into a new set of variables without losing information called principal components.
- PCA aims to capture the most important patterns or relationships in the data while reducing its dimensionality.
- Reduce the **dimensions** of large dataset.
- Small data sets are **easy** to **explore** and **visualize**.
- **Analyzing** and **training** is also much **easier** and **faster**.
- The first principal component is the linear combination that explains the largest amount of variation in the data.
- Subsequent principal components explain decreasing amounts of variation.
- Most of the information within the initial variables is **compressed** into **first components**.  
- PCA tries to put **maximum possible information** in **first component**. 
- And then the remaining information in the corresponding **components**.
- `PCA` is affected by scale, so scaling of features before applying `PCA` is important.
- Reconstruct the original data from the reduced dimensional representation by using a subset of the principal components.
- This reconstruction is an approximation of the original data but captures the essential characteristics.

<h3 name='lda'>LDA ( Linear Discriminant Analysis ) ( Supervised )</h3>

- Classify data sets into different categories or classes.
- Maximizes the separation between two or more classes of data.
- LDA creates a new axis ( Maximize the distance between **means** of two classes and minimize variation within each class )

<h3 name='tsne'>t-SNE ( t Distributed Stochastic Neighbor Embedding )</h3>

- Non-linear dimension reduction ( Spiral, Mixed ) 
- Data that is complicated to understand ( Multi-Dimensional Data )
- A tool to visualize and explore high-dimension data.
- Identity clusters based on the similarity of data points.
- Maps **multi dimensional data** to a **lower dimensional space**. 

### Anomaly Detection :
- Discover unusual data points in the data set.
- Used to find fraudulent transactions and identify an `outlier` caused by human error during data entry.
- Reduces complexity of data and helps to understand data more clearly and better way.

### Association Mining :
- Set of items that frequently occur together in a data set.
- Basket Analysis: Items bought together | Goods purchased at the same time help to develop marketing strategies.

### Feature Selection
- Select important features | Helps to improve accuracy | Not every feature adds value to solve the problem.
- Understanding each feature before using it for creating an ML model.
- Correlation between `features` and `target` helps to select better features.
- `Ensemble learning techniques` have a parameter of `feature_importance` which helps us to find important features.

### Standardization 
- Standardize the `range` of the continuous variables so that each one of them contributes equally to the analysis.

![Machine Learning Map](Image/MLMap.jpg)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
