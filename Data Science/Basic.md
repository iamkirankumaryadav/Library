### Cofounding Variables 
- Variable that Affects | Influences both Dependent and Independent Variables.

### Selection Bias 
- The Sample Selected does not represents the Population Correctly, it is Biased to One Instinct. 

### Machine Learning Model
- A File that has been Trained to Recogonize certain types of Patterns and Relationships between Features and Labels. 
- File saved after running a Learning Algorithm on Training Data. (File consist of Vectors of Coefficients and Intercepts) Parameters. 

Model Learning Model = Data + Prediction Algorithm Procedure (Using Data to make Prediction)

Data + Algorithm ( Sklearn Machine Learning Algorithms )

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


### Output of Classification Algorithm
Discrete Classifier : Binary Output (Yes | No)
Probabilistic Classifiers : Number between 0 and 1

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
