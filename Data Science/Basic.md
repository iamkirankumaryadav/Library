### Correlation 
- Measures how Strongly Two Variables are related. 
- Change in One variable results in change in another variable. | Measures Strength            
- cannot Capture Trend of Data
- Poor Predictive Performance

### Covariance  
- Measures how much two variables vary with each other.

### Confidence Interval  
- Gives a Range of Values which is likely to conatin Population Parameter.
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
- The Sample Selected does not represents the Population Correctly, it is Biased to One Instinct. 

### Machine Learning Model
- A File that has been Trained to Recogonize certain types of Patterns and Relationships between Features and Labels. 
- File saved after running a Learning Algorithm on Training Data. (File consist of Vectors of Coefficients and Intercepts) Parameters. 

Model Learning Model = Data + Prediction Algorithm Procedure (Using Data to make Prediction)

Data + Algorithm (Sklearn Machine Learning Algorithms)

### Data 
X Train : Independent Features for Training
Y Train : Target Labels for Training

X Test : Independent Features for Testing 
Y Test : Target Labels for Test Data | Unseen Data | Used to Compare with the Predictions made by X Test.

### Algorithm
- A Procedure that Runs on Data to Create Machine Learning Model
- Model Performs Pattern Recognition i.e Learns from Data | Fit on Data Set ( X Train, Y Train )
- Fit() is used to Train the Model with Patterns between Independent Features ( X Train ) and there Corresponding Labels ( Y Train )

e.g 
- Sklearn Provides Different Algorithms for Different Type of Problems
- KNN for Classification
- LinearRegression for Regression 
- LogisticRegression for Classification ( We Find Set of **Coefficients** that Minimize Error on Training Data Set )
- KMeans for Clustering

Algorithms are described using Linear Algebra with Lines, Axes, Points.


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
