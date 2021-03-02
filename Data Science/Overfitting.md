# Underfitting and Overfitting
  
### Underfitting | Simple Model : High Bias + Low Variance
- **High Bias** : High Error on Training Data ( **Underfitting** )
- The Model Fails to Characterize the Basic Data Correctly. 
- The Model and Algorithm does not Fit the Data Well enough.

### Overfitting | Complex Model : Low Bias + High Variance
- **High Variance** : High Error on Test Data
- When a Massive Amount of Data Trains a Machine Learning Model, it tends to Learn from Noise and Inaccurate Data.
- Random Error and Noise | Complex Model | Too Many Parameters (Columns) relative to the number of Observations (Rows) 
- Poor Predictive Performance
- Difference between the Prediction and the Unseen Data Point is High (High Variance)
- Model Tries to Fit the Training Data so closely that it does not Generalize well to New Unseen Data.

### Bias and Variance helps us Improve the Data Fitting | Training Process resulting in more Accurate Models.

### Correlation : Measures how Strongly Two Variables are related. Change in One variable results in change in another variable. | Measures Strength            
- cannot Capture Trend of Data
- Poor Predictive Performance

### Covariance  
- Two Variables Vary with Each Other.

### Confidence Interval  
- Gives a Range of Values which is likely to conatin Populatiojn Parameter.
- Tells How likely Interval is to contain the Population Parameter.
- Represented by Alpha 

### P Value 
- Determine Strength of your Results in Hypothesis Test.
- p value is a Number between 0 and 1
- Low p value <0.05 indicates we can Reject Null Hypothesis
- High p value >0.05 Accept Null Hypothesis.

### Regularisation 
- The Process of Adding Tuning Parameter to Model in order to Prevent Overfitting.
- Adding Constant (L1 - Lasso or L2 - Ridge ) Multiples to Weights.
- The Model Predictions should Minimize the Loss Function.


### Cofounding Variables 
- Variable that Affects | Influences both Dependent and Independent Variables.

### Selection Bias 
- The Samle Selected does not Represents the Population Correctly, it is Biased to One Instinct. 

### Machine Learning Model
- A File that has been Trained to Recogonize certain types of Patterns and Relationships between Features and Labels 
- File saved after running a Learning Algorithm on Training Data. (File consist of Vectors of Coefficients and Intercepts) Parameters. 

Model Learning Model = Data + Prediction Algorithm Procedure (Using Data to make Prediction)

Data + Algorithm (Sklearn Machine Learning Algorithms)

### Data 
X Train : Training Data of Independent Variables (Features)
X Test : Test Data of Independent Variables (Target Labels)
Y Train : Training Data of Dependent Variable (Features)
Y Test : Test Data of Dependent Variable | Unseen Data | Used to Compare with the Predictions made by Y Train.

- Train a Model over a Set of Data

### Algorithm
- A Procedure that Runs on Data to Create Machine Learning Model
- Model Performs Pattern Recognition i.e Learns from Data | Fit on Data Set (X Train, X Test)
- Fit() is used to Train the Model with Patterns between Independent Features (X Train) and there Corresponding Labels (X Test)

e.g Sklearn Provides Different Algorithms for Different Type of Problems
We have,
KNN for Classification
LinearRegression and LogisticRegression for Regression (We Find Set of Coefficients that Minimize Error on Training Data Set)
KMeans for Clustering

Algorithms are Described using Linear Algebra with Lines, Axes, Points.

### Steps of Machine Learning
1.Gathering Data
2.Preparing Data (Preprocessing)
3.Choosing a Correct Model
4.Training Data
5.Testing Data and Evaluation
6.Hyperparameter Tuning
7.Prediction

> Model is the System that makes Predictions

> Parameters are the Factors which are considered by the Model to make Predictions. LinearRegression(parameters...)

> Learner makes Adjustments in the Parameters and the Model to Align the Predictions with Actual Results.

### Manage Noise
- The Model created will have a lot more Errors because of Noise
- Noise is Unwanted that Weakens the Learning Process of Model
* Reasons for Noise
- Large Training Data Set
- Errors in Input Data 
- Data Labelling Error
- Lack of Data (Missing Data not Handled Properly)
- Unobservable Attributes that might affect Classifications (Sometimes Data Visualization helps to Find Hidden Patterns)

### Generalisation 
- How well the Model predicts outcomes for a New Set of Data.

### Output of Classification Algorithm
Discrete Classifier : Binary Output (Yes | No)
Probabilistic Classifiers : Number between 0 and 1

### Classification
- Supervised Learning
- Process of taking Some Sort of Input and Assigning a Label to it.
- Prediction of Discrete 'Yes' or 'No'



### Generalization
- Model's Ability to Adapt Properly to New Unseen Data(Test Set), Drawn from the Distribution as the one used to Create (Train Set) the Model
- Develop Intuition about Overfitting
- Determine whether Model is Good or Bad
- Divide a Data Set into a Training Set and Test Set.

A ML Model aims to make Good Predictions on New, Previously Unseen Data.
Divide Data Set into Two Subsets :
Train Set : A Subset to Train a Model.
Test Set : A Subset to Test a Model.

Good Performance on the Test Set is a Indicator of Good Performance on the New Unseen Data.

### Scaling :
- Converting Floating Point Feature Values from their Natural Range (e.g. 100 to 900) into a Standard Range (e.g. 0 to 1 or -1 to 1)

A Feature Set Consisting only Single Feature, Scaling provides little to no Practical Benefit.
Scaling is Beneficial if the Feature Set consists of Multiple Scaling.

Benefits :
1. Helps Gradient Descent Converge more Quickly.
2. Helps the Model Learn Appropriate Weights for Each Feature. (Model Pay more Attention to the Features having Wider Range)

### **Chi Squared Test** 
- A Test for **Independence** of two Categorical Variables and returns **Probability**.
- Derive **Statistical Significance** of Relationship between the Variables.
- Test whether the **Evidence** in the **Sample** is Strong enough to **Generalize** that relationship for a **Population**.
- Difference between **Expected** and **Observed**
- Probability = 0 indicates both Categorical Variable are **Dependent**.
- Probability = 1 indicates both Categorical Variable are **Independent**.
