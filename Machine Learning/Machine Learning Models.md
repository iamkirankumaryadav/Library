<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

<h1 align="center">Machine Learning Models 🤖🚀💻</h1>

<h4 align="center">ML is a subset of AI that creates an algorithm that can learn from data by itself without being explicitly programmed</h4>

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
Algorithm learns from labelled data | Algorithm learns from unlabelled data | Agents take actions in an environment
The algorithm tries to find relationships | Algorithm tries to find patterns | Agent learns from rewards and penalty

- Columns: Feature Matrix (Variables) and Target Vector (Labels)
- Features: Independent Variable | Dimensions | Attributes | Inputs | Predictors | Estimators | Characteristics.
- Target: Dependent Variable | Label | Class | Output | Predicted Value | Estimated Value | Response.
- Rows | Observations | Records | Samples | Instance.
- Feature: A measurable property, that can be categorical (discrete) or numerical (real or int number)
- Target: What we want to make **prediction** for.
- Model learns a relationship between a feature matrix and a target vector.
- Model is the system that makes **predictions** or **classification** on new unseen data.
- The goal of ML is to build a model that performs well on new data.
- **Parameters** are factors which are considered by the model to make **predictions** or **classifications**.
- **Parameters** are tuned to gain **accuracy** with least [**error**](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Error.md).

### Scikit Learn
1. Scikit Learn is a great library for creating an ML model from data.
2. Before you fit a model using Scikit Learn, your data must be in a recognizable format.
3. Scikit Learn works well with numeric data that is stored in NumPy arrays.
4. It can also convert data from objects like Pandas data frames and NumPy arrays.
5. Feature matrix is a 2D grid of data where rows represents samples and columns represent features.
6. The target vector is usually a 1D vector column.

<h1 name='sup' align=center>Supervised Learning ( Labeled Data )</h1>

- ML algorithms that perform learning by studying the relationship between the feature variables and the known target variable.
- The algorithm learns to recognize patterns in the input data and map them to the correct output based on the labelled data.
- The goal of supervised learning is to create a model that can accurately predict the output for new, unseen input data.
- Supervised learning is useful for regression (continuous target variables) and classification (discrete target variables).

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
- The straight line is called the regression line.
- Formula: y = mX + c, where y is the dependent variable and X is the independent variable.
- **m** is the **slope** and **c** is the **y-intercept**, both are the **regression coefficients**.
- Linear Regression is simple to understand and interpret, with fast training and prediction.
- Linear Regression assumes a linear relationship between variables, sensitive to outliers.
- Can suffer from multicollinearity if the dataset has highly correlated variables.

**Hyperparameters:**

1. **Alpha:**
- Used in Lasso (L1) and Ridge (L2) regression, determines the strength of the regularization.
- A higher value of alpha means more regularization and simpler linear models.
- For αlpha = 0, Ridge regression is just linear regression.
- The best value for alpha is found by cross-validation (Grid Search CV or Random Search CV)

2. **Normalization:**
- If True, the independent variable X will be normalized before regression by subtracting the **mean**.

3. **Fit Intercept:**
- Whether to calculate the intercept **c** for this model.
- If set to False, no intercept will be used in calculations.
 
<h1 name='class' align=center>Classification</h1>

<h3 name='logreg'>2. Logistic Regression (<a href='https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Supervised%20Learning/Classification/Logistic%20Regression.md'>More</a> )</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/04.Logistic%20Regression.ipynb)

- Model used for classification tasks like classifying flower species and image recognition.
- A statistical model used to predict the probability of a binary outcome (T/F, Y/N, 1/0, etc.)
- Logistic Regression starts with a linear equation, and the result is passed through a sigmoid function.
- The sigmoid/logistic function maps the linear combination to a probability between 0 and 1.
- If the predicted probability is greater than a threshold (0.5), the model predicts the outcome as 1.
- One or more independent features are used to **classify** categorical target labels/variables.
- Widely used for binary classification, simple and requires less training, rescaling provides better accuracy.

### Advantages of Logistic Regression

- Model training and predictions are relatively fast, no tuning is usually required.
- Performs well with a small number of observations or samples.

### Logistic Regression for Multiclass Classification

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/05.Logistic%20Regression%20for%20Multiclass%20Classification.ipynb)

- Split the task into multiple binary classification datasets.
- **Fit** a binary classification (Logistic Regression) model on each label.
- One vs Rest (OvR) or One vs All (OvA) is a technique that extends binary classification to **multiclass** classification.
- Digit 0 vs Digit 1, 2 and 3
- Digit 1 vs Digit 0, 2 and 3
- Digit 2 vs Digit 0, 1 and 3
- Digit 3 vs Digit 0, 1 and 2
- The model that predicts the **highest** class probability is the predicted class.
  
<h3 name='tree'>3. Decision Tree</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/06.Decision%20Tree.ipynb)

- Root Node: Represents the entire sample and this further gets divided into two or more homogeneous sets.
- Edges | Branches | Splits | Decisions | Conditions | Outcomes | Sub Tree
- Leaf Node | Terminal | Label | Class: Nodes that do not split further.
- The **Decision Tree** recursively splits the data into smaller subsets based on the values (Continuous or Discrete) of input variables.
- At each split, the algorithm chooses the best feature to split the data into two subsets based on the values of that feature.
- The process continues until the data is split into a pure subset (A subset that can't be split further)
- Once the data is split into a pure subset, the decision tree can be used to make predictions for new data points.
- Decision Trees are used to make predictions on new data by traversing the tree, the terminal node represents the predicted outcome.
- The tree is built by selecting the best feature at each node, based on measures of impurity, such as the Gini Index or IG
- Feature with **High Information Gain** or **Low Entropy** or **Low Gini Index** is selected as the best feature.
- The path from the root to a leaf node represents a set of rules that will be used to predict or classify new instances.
- Used especially for binary classification and multiclass classification.
- When the target variable has a categorical set of values, a classification tree is used.
- When the target variable has a continuous value, a regression tree is used.
- **CART:** Classification And Regression Tree.
- Decision Tree is prone to overfitting, resulting into a poor performance on the test data.
- Pruning: When we remove unnecessary sub-nodes (features) of a decision node.
- Pruning reduces the complexity, overfitting, and improves its generalization performance.
- Growing a tree means deciding which feature to choose and what condition to apply for splitting.
- Continuous can be converted into a binary or boolean by setting the threshold value.
- We should also know when to stop | terminate (**Max Depth**) to prevent the model from overfitting.
- Decision trees can be pruned if necessary to avoid overfitting.

**Advantages:**
- Easy to visualize and understand, they can also handle missing data and outliers.
- Don't require extensive data preprocessing such as normalization or rescaling.
- Capture non-linear relationships between the feature matrix and target vector.

```python
from sklearn.tree import DecisionTreeClassifier
```

### Information Gain (Which feature is to be selected as a root node?)
- **IG** decides which feature will become a **node** and will split the data further for building the **tree**.
- Feature with the **High IG** will be considered and the process will continue until **IG** becomes 0.

### Gini Index (Checks for impurity in the dataset)
- A low **Gini Index** is better.
- Pure: All data belongs to the same class in a subset (Gini Index = 0)
- Impure: Data is a mixture of different classes in a subset.

### Entrophy (Measure Disorder | Randomness | Uncertainty in Data | Unpredictability)
- **Low Entropy** is better. (Easy to conclude from the data)

### Cross Entropy (Classification loss function)
- The difference between the predicted probability distribution and the true probability distribution.
- **Low cross entropy:** A close match between the predicted and actual probability distribution.
- **High cross entropy:** A huge difference between the predicted and actual probability distribution.

```
H(p, q) = - Σ p(x) * log(q(x))

x iterates over all possible outcomes.
p(x): The true probability of outcome x.
q(x): The predicted probability of outcome x.
```    

The above metrics are calculated for each feature, which helps to identify the best/most important feature.

Advantage of Decision Tree | Disadvantage of Decision Tree
:--- | :---
Handle categorical and numerical data | Prone to overfitting
No effect of outliers | Need careful **parameter tuning**
Handle **non linear data** |

### Individual trees are prone to overfitting but improve when ensembled

### How to Avoid Overfitting?
- Remove | Prune features with less importance (Low IG, high GI, and high Entrophy) (Irrelevant Feature)
- Early stop (Limit the max_depth of the tree)

<h3 name='forest'>4. Random Forests (Ensemble Learning Technique | Bagging)</h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/09.Random%20Forest.ipynb)

- Random sampling (Bootstrap aggregation with replacement)
- An ensemble learning method that uses multiple decision trees for both regression and classification.
- Ensemble learning algorithms combine the predictions of multiple decision trees to produce a more accurate prediction.
- Once the decision trees (weak learners) are trained, they are used to predict new data points.
- Each decision tree is built using a random subset of the training data (feature matrix)
- Multiple decision trees (weak learners) are trained in parallel and individually/independently.
- Bootstrapping (Row sampling with replacement): Subsets are randomly selected from the original dataset.
- Majority Voting: Prediction of the model is based on the **voting** of decision tree outputs.
- Regression: The mean/average of the predictions of all the decision trees are considered.
- Classification: The class selected by most of the decision trees is considered.
- Random forest creates a model that is more accurate and less prone to overfitting than a single decision tree.
- **Bagging:** Multiple decision trees are trained in parallel to form one strong accurate predicting model.
- Adding multiple decision trees reduces the risk of error and overfitting by reducing the variance.
- Random forests are accurate, robust to overfitting, and used for both regression and classification.
- Random forests can be trained on data of any type (numerical, categorical, and ordinal data)
- Random forest provides an attribute **model.feature_importances_** that retrieves the relative importance scores for each input feature.
- Anyhow each Decision Tree uses Gini Index, Entropy, and Information Gain which find the best features from the dataset.

**Advantages:**
- RF can handle large datasets with high features and can provide accurate results.
- RF can handle non-linear relationships between features and target variables.
- RF can handle missing values in the data.
- RF performs feature selection by building multiple decision trees.
- Each tree is built using a random selection of features and observations from the dataset.
- Feature sampling ensures that different trees in the random forest use different subsets of features during training.
- This allows the RF to capture a wider range of patterns and relationships within the data.
- Each tree in the random forest can calculate the importance of a feature (feature_importances_)
- A feature with high IG, low GI and low entropy is an important feature for the model.

```python
from sklearn.ensemble import RandomForestClassifier
```

<h3 name='adaboost'>ADABOOST (Adaptive Boosting)</h3>

- AdaBoost iteratively trains a sequence of weak decision trees.
- Gives more weight to the data points that are misclassified in each iteration.
- AdaBoost can significantly enhance the accuracy of models, especially when dealing with complex datasets.
- AdaBoost is effective in handling class imbalance and doesn't require extensive hyperparameter tuning.
- AdaBoost implicitly performs feature selection by assigning more importance/weights to relevant features.
- Primarily used for classification tasks. Not well suited for regression tasks.

<h3 name='gbm'>GBM (Gradient Boosting Method)</h3>

- Gradient boosting combines the ideas of boosting (combining weak learners to create a strong learner) with gradient descent.
- A method used to minimize errors in predictions. It's primarily used in regression and classification problems.
- Loss function: Measures how far the model's predictions are from the actual values.
- Gradient boosting algorithms aim to minimize this loss function.
- Gradient Descent: An iterative optimization algorithm used to minimize the loss function.

Algorithm Steps:
- **Initialize with a base model:** Starts with a simple model (decision tree) to make initial predictions.
- **Compute the Residuals:** Calculate the difference between predicted and actual values (residuals)
- **Build a New Model:** Construct a new model to predict the residuals from the previous model.
- **Update the Model:** Update the model's predictions by adding the new model's predictions to the previous predictions.
- **Minimize Loss Function:** Use gradient descent to find the model that minimizes the loss function.
- Repeat the process for a specified number of iterations, until the loss function stops decreasing.

<h3 name='xgboost'>XGBOOST (Extreme Gradient Boosting)</h3>

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

- Aims to find an optimal hyperplane that classifies the distinct classes with maximum margin in N-dimensional space.
- Hyperplanes are decision boundaries that help to classify the data points. Data points are called Support Vectors.
- SVM can be used for linear and non-linear regression and classification.
- SVM can manage high dimensional data and nonlinear relationships between the data points.
- SVM uses kernel trick for non-linear data which creates a kernel matrix in N-dimensional space for linear separation.
- Works better even if the data set has a lot of outliers (Because SVM focus only on support vectors closest to the hyperplane)
- Take a long time to train and predict if the number of observations is very large.
- Kernel functions: Linear | Radial basis function ( RBF ) | Polynomial | Exponential.

### Benefits 

- SVM works well with unstructured and semi-structured data (text, image, face, anomaly detections, etc.)
- Generalize well on the new unseen data and the risk of overfitting is also less.

### Disadvantage

- Choosing a good Kernel function, fine-tuning and even visualization is challenging due to high dimensionality.
- Feature rescaling (normalization/standardization) is very important for better accuracy.
- Not suitable for larger datasets, training can be time and resource-consuming.
- Difficult to understand and interpret the final model, variable weights have individual impact.

<h3 name='knn'>6. K Nearest Neighbours</h3>

- KNN is used for both regression and classification. Measures the Euclidean distance between the data points. 
- Initialize K (# nearest neighbours) we need for comparison or calculation.
- Calculate the distance between new data points and the K nearest neighbours of training data points.
- e.g. if K = 5, it will calculate the distance from the 5 nearest data points.
- Sort the calculated distance in ascending order and get the shortest distance or most frequent classes in neighbour.
- Regression: Mean of K nearest distances are considered.
- Classification: Mode of K nearest distances are considered.

<h3 name='naive'>7. Naive Bayes</h3>

- Naive Bayes is a probabilistic classifier, based on class prediction probability (Binary and Multiclass classification)
- Creates the conditional probability distribution for all the classes independently.
- Naive: Assumes that all of the features are independent of each other (No correlation between any feature)
- e.g Classification of dog breed (Naive Bayes tries to create a probability that each dog belongs to a separate class)
- Weights can be added to improve accuracy.
- Fast, highly scalable, requires less training, and can be used for real-time predictions.
- Can handle missing data and is not sensitive to irrelevant features.
- P(Class | Data) = (P(Data | Class) * P(Class)) / P(Data)
- P(Class | Data): Probability after observing the data (Posterior Probability)
- P(Data | Class): Likelihood
- P(Class): Probability before observing the data (Prior Probability)
- Classification: Spam email, Dogs Breed Image, and Customer likely to churn.
- Regression: House price, Product Sales, and Customer lifeline.
- Anomaly detection: Detecting fraudulent transactions, Network intrusion, and Outlier detection.

<h1 name='unsup' align=center>Unsupervised Learning (Unlabeled Data)</h1>

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
    <td>Better algorithms: Apriori</td>
  </tr>
</table>
 
 <h1 name='cluster' align=center>Clustering</h1>

- Find relationships and patterns between independent features.
- Extract important features and explore the dataset in detail.
- Groups the data points into segments or clusters based on similarity.
- Unsupervised algorithms don't make predictions from the data.

### **Clustering Techniques**

<h3 name='kmean'><strong>1. K Mean Clustering</strong></h3>

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/10.K%20Mean%20Clustering.ipynb)

- An unsupervised ML algorithm to group similar data points into K distinct clusters.
- Data points with similar characteristics are grouped in one cluster.
- Mean in K-Mean refers to the averaging of data (Finding the centroid by calculating mean)
- Decide how many clusters you want to form in your data. 
- K random data points are initially selected as a centroid (centre of cluster) for each cluster.
- Each data point nearest to its corresponding centroid belongs/assigned to that cluster.
- The centroid is recalculated for the newly formed clusters, and the data points are updated based on the new centroid.
- This is an iterative process, we stop when there is no further classification.
- Different starting points (centroid) create different clusters. 

### **Elbow Method**
- The sum of the squared distance between the data point and centroid gets smaller as the number of clusters increases.
- The **Elbow Method** helps us to find the optimal number of clusters.

**Usage:**
1. **Market Segmentation:** Grouping customers based on purchasing behaviour, age, income, etc.
2. **Document Classification:** Grouping documents by topics, subject, or contents.
3. **Image Compression:** Reducing the number of colours in an image.
4. **Spatial Data Analysis:** Identifying areas of similar land use in an urban setting.
5. **Anomaly Detection:** Detecting unusual patterns or outliers in datasets.

<h3 name='hc'><strong>2. Hierarchical Clustering</strong></h3>

- Groups data points into a hierarchy of clusters. We don't need to determine the number of clusters.
- A dendrogram can visualize and determine the number of clusters in the data.

### Agglomerative Nesting (Bottom-Up Approach)
- Treating each data point as a single cluster and then merging the closest data points.
- After each iteration, similar and closest clusters are merged, until there is only one cluster left.

### Divise Analysis (Top-Down Approach)
- Starts with considering all the data points in a single cluster
- Iteratively splits the clusters based on dissimilarity.

### How do we calculate the similarity between the clusters?
- **MIN:** Distance between the closest data points of two clusters.
- **MAX:** Distance between the farthest data points of two clusters.
- **AVG:** Average distance between each data point of two clusters.
- **Centroids:** Distance between the centroid of two clusters.
 
<h3 name="dbscan"><strong>3. Density Based Clustering</strong></h3>

- **DBSCAN:** Density-based spatial clustering of applications with noise (outliers).
- Group similar data points together based on density (data points that are closely packed together).
- **High-Density Region:** Data points are close to each other | High neighbours within the radius.
- Unlike other clustering algorithms, DBSCAN does not require a predefined number of clusters.
- Data points in low-density regions are outliers.
- Visualization (Scatter Plot or Density Plot) can explain the clustering method in a better way.
- DBSCAN can effectively identify clusters of arbitrary shapes and sizes.

DBSCAN defines 3 types of data points based on their density.
1. **Core points:** Data points that are very close to each other.
2. **Border points:** Data points that are neighbours but not too close to each other.
3. **Noise points:** Data points that are very far away from the rest of the data points (Outliers)

### **B. Dimensionality Reduction**

- A technique used to reduce the number of features/variables in a dataset while retaining the most important information.
- Simplifying the complexity of the dataset by reducing the number of dimensions (variables) without losing information.
- The aim is to find the **important features/variables** that the model can use for better prediction.
- Reducing **irrelevant features** that have no relation with the target feature.
- Reduces **multicollinearity**, and saves storage and time by improving the performance of the model.
- Project data into lower dimensions while preserving as much useful variability (19/20) as possible.
- e.g. If we observe a Scatter Plot in multi-dimension it will be complicated for understanding. 
- Consider only 1D then it is just a line and a few points in which some are close to the line and some are a bit far away from the line.
- Combine features or remove features to reduce dimensions.
- Dimensionality Reduction helps to prevent the models from overfitting (Due to too many features)
- Simplifies the model, improves accuracy, fast training, easy visualization, and helps to identify patterns easily.
- Scale and normalize data before applying dimensionality reduction techniques.
- Use visualizations to assess how well the reduced dimensions represent the data.

### **Techniques of Dimensionality Reduction**

<h3 name='pca'>Principal Component Analysis (PCA | Unsupervised | Numerical)</h3> 

[Algorithm](https://github.com/KIRANKUMAR7296/Algorithms/blob/main/Code/11.PCA.ipynb)

- Transforms a dataset into a new set of features without losing information called principal components.
- A dataset with high dimensions and high correlation can be complicated for analysis and visualization.
- PCA aims to capture the most important features in the dataset while reducing its dimensionality.
- Datasets with essential features are easy to explore, visualize, analyze and train (simplifies the EDA).
- The first principal component (PC1) explains the largest amount of variation in the dataset.
- Subsequent principal components (PCs) explain the decreasing amount of variations in the dataset.
- PCA tries to put the maximum possible information in the first principle component. 
- And then tries to put the remaining information in the corresponding principle components.
- PCA is affected by the scale, so rescaling features before applying PCA is important.

<h3 name='lda'><strong>Linear Discriminant Analysis (LDA | Supervised | Categorical | Classification)</strong></h3>

- LDA identifies the best way to separate the existing categories/classes in the dataset.  
- Finds the best linear separation to classify datasets into different categories/classes.
- Reduce the number of features and maximize the separation between two or more categories/classes.
- LDA creates a new axis (Maximize the distance between means of two classes and minimize variation within each class)

<h3 name='tsne'>t-SNE (t Distributed Stochastic Neighbor Embedding | Non-linear)</h3>

- Used to visualize high dimensional data in a low dimensional space.
- Non-linear dimensionality reduction technique (spiral, mixed) 
- t-SNE calculates the probability that a data point is a neighbour of another data point in the higher dimensional space.
- t-SNE then constructs a similar joint probability distribution in the lower dimensional space.
- Identity clusters based on the similarity of data points.
- Reduces dimensions while keeping similar instances closer and dissimilar instances apart.

### Anomaly Detection
- Discover unusual data points and abnormal relationships and patterns in the dataset.
- Used to find fraudulent transactions and identify an outlier caused by human error during data entry.
- Reduces complexity of data and helps to understand data in a better way.

### Association Mining
- Set of items that frequently occur together in a dataset.
- **Basket Analysis:** Items bought together | Goods purchased simultaneously help develop marketing strategies.

### Apriori
- A widely used algorithm in **data mining**, specifically for **association rule learning**.
- It helps identify relationships between items that frequently appear together in transactions.

![Machine Learning Map](Image/MLMap.jpg)

### Reinforcement Learning
- ML technique that enables an agent to learn and interact with an environment by trial and error.
- RL uses rewards and punishments to address and signals for positive and negative behaviour.
- RL agents learn from the consequences of their actions.

**Key Components of RL**
1. **Agent:** The entity that learns and interacts with the environment.
2. **Environment:** The surrounding world that the agent interacts with.
3. **State:** The current situation of the agent within the environment.
4. **Action:** The choices the agent can make.
5. **Reward:** A signal indicating how well the agent performed in a given state.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
