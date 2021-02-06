# Certain Assumptions to Remember Underfitting and Overfitting
- Bias is Error Introduced on Training Data 
- Variance is Error Introduced on Testing Data

# Bias 
- Error Introduced in your Model due to Oversimplification of the Machine Learning Algorithm.
- High Bias led to Underfitting 
- Algorithm is Unable to Capture Relevant Relations between Features and Targets. 
- A High Bias Model includes more Assumptions about Target.
- When you Train your Model at that time Model makes Simplified Assumptions to make the Target Function easier to Understand.
- High Bias Data Set does not Accurately Represents a Model.			
- The Amount that a Model's Prediction differs from the Target Value.

Bias = Predicted - Actual

- A Linear Algorithms often has High Bias, which makes them Learn Fast.
- Simple the Algorithm, more Bias it will Introduce.
- Non Linear Algorithms often have Low Bias.

# How to Reduce Bias?
- K Fold Resampling | Split Data Set into K Numbers and Each Set is used as Testing Set.
- K Fold Cross Validation 
- Bootstrapping | Iteratively Resampling a Data Set with Replacement.

# Low Bias Machine Learning Algorithms 
- Decision Tree.
- KNN.
- SVM.

# High Bias Machine Learning Algorithms 
- Linear Regression. 
- Logistic Regression.

# Variance 
- Error Introduced in your Model due to Complex Machine Learning Algorithms 
- Model Learns Noise from the Training Data Set and Performs bad on Test Data Set.
- Lead to High Sensiitivity and Overfitting.
- Indicates How much the Prediction Alters if different Training Data is used.
- How much a Prediction Differs from its Expected Value.
- Measures Inconsistency of Different Predictions using Different Training Sets.
- High Variance reflects Noise in the Training Data Set.
          
# Model with Low Variance means Sample Actual Data is Close to Prediction.

# Low Variance Algorithms  
- Linear Regression.
- Logistic Regression.  
- Linear Discriminant Analysis (LDA)
- Machine Learning Model does not Vary much with the Different Data Set.

# High Variance Algorithms : 
- Decision Tree
- KNN 
- SVM
- Machine Learning Model varies with Different Data Set. 

# Bias Variance Trade Off

Increasing Bias decreases Variance and Increasing Variance decreases Bias,

Trade Off - Find the Correct Balance : Low Bias and Low Variance.   

# Underfitting | Simple Model : High Bias + Low Variance
- The Model Fails to Characterize the Basic Data Correctly. 
- The Model and Algorithm does not Fit the Data Well enough.

# Overfitting | Complex Model : Low Bias + High Variance
- When a Massive Amount of Data Trains a Machine Learning Model, it tends to Learn from Noise and Inaccurate Data.
- Random Error and Noise | Complex Model | Too Many Parameters (Columns) relative to the number of Observations (Rows) 
- Poor Predictive Performance
- Difference between the Prediction and the Unseen Data Point is High (High Variance)
- Model Tries to Fit the Training Data so closely that it does not Generalize well to New Unseen Data.

# Correlation : Measures how Strongly Two Variables are related. Change in One variable results in change in another variable. | Measures Strength            
- cannot Capture Trend of Data
- Poor Predictive Performance

# Covariance : Two Variables Vary with Each Other.

# Confidence Interval : Gives a Range of Values which is likely to conatin Populatiojn Parameter.
                      : Tells How likely Interval is to contain the Population Parameter.
                      : Represented by Alpha 

# P Value 
- Determine Strength of your Results in Hypothesis Test.
- p value is a Number between 0 and 1
- Low p value <0.05 indicates we can Reject Null Hypothesis
- High p value >0.05 Accept Null Hypothesis.

# Regularisation 
- The Process of Adding Tuning Parameter to Model in order to Prevent Overfitting.
- Adding Constant (L1 - Lasso or L2 - Ridge ) Multiples to Weights.
- The Model Predictions should Minimize the Loss Function.


# Cofounding Variables 
- Variable that Affects | Influences both Dependent and Independent Variables.

# Selection Bias 
- The Samle Selected does not Represents the Population Correctly, it is Biased to One Instinct. 

# Machine Learning Model
- A File that has been Trained to Recogonize certain types of Patterns and Relationships between Features and Labels 
- File saved after running a Learning Algorithm on Training Data. (File consist of Vectors of Coefficients and Intercepts) Parameters. 

Model Learning Model = Data + Prediction Algorithm Procedure (Using Data to make Prediction)

Data + Algorithm (Sklearn Machine Learning Algorithms)

# Data 
X Train : Training Data of Independent Variables (Features)
X Test : Test Data of Independent Variables (Target Labels)
Y Train : Training Data of Dependent Variable (Features)
Y Test : Test Data of Dependent Variable | Unseen Data | Used to Compare with the Predictions made by Y Train.

- Train a Model over a Set of Data

# Algorithm
- A Procedure that Runs on Data to Create Machine Learning Model
- Model Performs Pattern Recognition i.e Learns from Data | Fit on Data Set (X Train, X Test)
- Fit() is used to Train the Model with Patterns between Independent Features (X Train) and there Corresponding Labels (X Test)

e.g Sklearn Provides Different Algorithms for Different Type of Problems
We have,
KNN for Classification
LinearRegression and LogisticRegression for Regression (We Find Set of Coefficients that Minimize Error on Training Data Set)
KMeans for Clustering

Algorithms are Described using Linear Algebra with Lines, Axes, Points.

# Steps of Machine Learning
1.Gathering Data
2.Preparing Data (Preprocessing)
3.Choosing a Correct Model
4.Training Data
5.Testing Data and Evaluation
6.Hyperparameter Tuning
7.Prediction

# Model is the System that makes Predictions
# Parameters are the Factors which are considered by the Model to make Predictions. LinearRegression(parameters...)
# Learner makes Adjustments in the Parameters and the Model to Align the Predictions with Actual Results.

# Manage Noise
- The Model created will have a lot more Errors because of Noise
- Noise is Unwanted that Weakens the Learning Process of Model
* Reasons for Noise
- Large Training Data Set
- Errors in Input Data 
- Data Labelling Error
- Lack of Data (Missing Data not Handled Properly)
- Unobservable Attributes that might affect Classifications (Sometimes Data Visualization helps to Find Hidden Patterns)

# Generalisation 
- How well the Model predicts outcomes for a New Set of Data.

# Output of Classification Algorithm
Discrete Classifier : Binary Output (Yes | No)
Probabilistic Classifiers : Number between 0 and 1

# Classification
- Supervised Learning
- Process of taking Some Sort of Input and Assigning a Label to it.
- Prediction of Discrete 'Yes' or 'No'

Bias and Variance helps us Improve the Data Fitting | Training Process resulting in more Accurate Models.

# Error due to Bias 
- Difference between the Expected Prediction of our Model and the Correct Value which we are trying to Predict.
- Each Time you run a New Analysis Creating a New Model, Due to Randomness in the Underlying Data Sets, Bias Measures How Far off these Model's Predictions are from the Correct Value.

# Error dur to Variance
- The Variability of a Model Prediction from a given Data Point
- How much the Predictions for a given point vary between different Models.

# Good Fit Model
- Low Bias and Low Variance
- Prediction is Actually Close to the Actual True 
- Generalized enough to Work with any Unseen Data (Low Variance) and at the Same Time should produce Low Prediction Error (Low Bias)

# Generalization
- Model's Ability to Adapt Properly to New Unseen Data(Test Set), Drawn from the Distribution as the one used to Create (Train Set) the Model
- Develop Intuition about Overfitting
- Determine whether Model is Good or Bad
- Divide a Data Set into a Training Set and Test Set.

A ML Model aims to make Good Predictions on New, Previously Unseen Data.
Divide Data Set into Two Subsets :
Train Set : A Subset to Train a Model.
Test Set : A Subset to Test a Model.

Good Performance on the Test Set is a Indicator of Good Performance on the New Unseen Data.

# Scaling :
- Converting Floating Point Feature Values from their Natural Range (e.g. 100 to 900) into a Standard Range (e.g. 0 to 1 or -1 to 1)

A Feature Set Consisting only Single Feature, Scaling provides little to no Practical Benefit.
Scaling is Beneficial if the Feature Set consists of Multiple Scaling.

Benefits :
1. Helps Gradient Descent Converge more Quickly.
2. Helps the Model Learn Appropriate Weights for Each Feature. (Model Pay more Attention to the Features having Wider Range)


Pandas Series : Column

Pandas DataFrames : Key (Column Label)
                    Value (Column Value)
