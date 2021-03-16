# Machine Learning Models 🤖🚀💻

<h3><a href=#sup>Supervised Learning</a> : Classify Data </h3> 
 
<h3><a href=#unsup>Unsupervised Learning</a> : Cluster Data </h3> 

### Steps of Machine Learning
1. Gathering Data
2. Preparing Data ( Preprocessing )
3. Explore Data
4. Clean Data
5. Feature Engineering ( Important Features to Train Model )
6. Choosing a Correct Model
7. Training Data
8. Testing Data and Evaluation
9. Hyperparameter Tuning
10. Prediction

> Model is the system that makes **Predictions**

> **Parameters** are the Factors which are considered by the model to make **Predictions**. **LinearRegression** ( parameters... )

> Learner makes adjustments in the Parameters and the Model to Align the Predictions with Actual Results.

<h3 name='sup'> Supervised Learning</h3>

### A. Regression

- Predict Dependent Variable on the basis of **Independent Features**

- Find **Relationship** between **Independent Variable** and **Dependent Variable**.

- Output is **Continuous**.

### 1. Linear Regression 

![Linear Regression](Image/RegressionLine.png)

![Equation of Line](Image/EquationLine.png)

> Simple Linear Regression : Find the Line that **Fits** the Data.

> Multiple Linear Regression : Find the Plane of **Best Fit**.

> Polynomial Regression : Find a Curve for **Best Fit**. 
 
### 2. Decision Tree

- Nodes 

### 3. Random Forests ( Ensemble Learning Technique )

- Multiple Decision Tree

- **Bootstrapped Data Sets** of Orignal Data and **Randomly** selecting **Subsets** at each step.

- Bagging Technique ( **Multiple** Decision Trees are **Trained** in **Parallel** to Form a **Strong Learner** )
 
- **Prediction** of Model is based on the **Mode** of Decision Trees ( **Majority Voting** )

- Reduces Risk of **Error** and **Overfitting**.

### 4. Neural Network

- Multi Layered Model inspired by **Human Brain**

- Nodes, Edges and Layers   

### B. Classififcation

- Predict **Dependent Variable**( Categories of Labels ) on the basis of **Independent Features**

- Find **Relationship** between **Independent Variable** and **Dependent Variable**.

- Output is **Discrete**

### 1. Logistic Regression 

- Probability of Finite Number of Outcomes.

- Output values can be between 0 and 1

### 2. Support Vector Machine

- Find **Hyperplane** in **N Dimensional Space** that can distinctly classify the data points.

### 3. Naive Bayes

- Probabilistic Machine Learning Model ( Likelihood, Prior Probability and Posterior Probability )

- Probability of **Event A** if **Event B** has already occured.

> P( **A** | **B** ) = P( **B** | **A** ) / P( **B** )

### 4. Decision Tree

### 5. Random Forest

### 6. Neural Network 

All follow Same Process in Regression and Classification the only difference is Output 

> **Regression** Output : **Continuous**

> **Classification** Output : **Discrete**

 
<h3 name='unsup'> Unsupervised Learning</h3>

- Find **Patterns** and **Relationships** from Input Data without References (Labels)

### A. Clustering

- Grouping of Data Points 

- Customer Segmentation | Fraud Detection | Document Classification

> Clustering Techniques

1. K Mean
- We Choose **K** number of Clusters.
- Select K Random Data Points as Centroid.
- Data Points nearest to its Corresponding Centroid belongs to that Cluster
- Again the Centroid is Calculated
- The Data Points are Updated based on New Centroid.

2. K Nearest Neighbours
- Calculate Distance between Test Data and Each Row of Training Data
- Sort the Calculated Distance in Ascending Order
- Get Top Rows Nearest to it or most Frequent Classes
- Return the Prediction.

2. Hierarchical
 
3. Density Based

### B. Dimensionality Reduction

- Aim is to find  the **Inportant Features** that can be used for by our Model for Better Predition.
- Reducing the Number of **Irrelevant Features** that has no relation with the Target Feature.
- There are some Features that brings **Multicollinearity** 
- Feature **Elimination** | **Feature Selection** or Feature **Extraction**
- Save Storage and Time by Improving Performance of Model.
- Due to less number of Features it can be Visualized in 2D and 3D.

### Feature Selection
- Select Relevant Features
- Remove Unwanted Features

> Techniques of Dimensionality Reduction

### Feature Extraction

- Principal Component Analysis. ( Reduce Dimensions of Data )
- Linear Discriminant Analysis.
