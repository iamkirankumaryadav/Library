# Why Feature Scaling ?

- The Units of Independent Features and Dependent Features are `Different`
- If we use those Feature for **Training** the Model will not Understand the `Units` it only considers `Magnitude`.
- e.g. Height ( cm ) and Weight ( kg ) for Calculating BMI,
- Here Height ( int ) and Weight ( float ) have different Scale for Measurement
- **Feature Scaling** will bring the value of both the Independent Features between 0 to 1.

# Algorithms that requires Feature Scaling
1. Regression ( `Gradient Descent` : while performing Gradient Descent the Scaled value will be near to Global Minima. )
2. Classification ( We find **Coefficients** )
3. K Mean ( Distance is Calculated, If we try to Find Distance between two Data Points of Different Features, there will be Large Variance. )
4. KNN 

# Algorithms that `do not` requires Feature Scaling
1. **Decision Tree** ( Scaling will not Affect the Splitting of Tree )
2. **Ensemble Techniques** ( Base Learner is **Decision Tree** )

