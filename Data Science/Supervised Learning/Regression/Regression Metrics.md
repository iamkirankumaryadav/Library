# Regression Metrics

1. We Start by some Initial Configuration of Model and `Predict` the **Output** based on some **Input**.
2. Predicted Value is compared with the `Target` and Measure the `Performance` of our Model.
3. Various Parameters of the Model are `Adjusted Iteratively` in order to reach the **Optimal Value** of the **Performance Metric**.

### Linear Regression
### 1. Mean Squared Error ( `MSE` ) 

![MSE](Image/MSE.jpg)

- Squared Difference between the `Actual` Value and the `Predicted` Value
- Square the Differences, Penalizes even Samll Error

### 2. Root Mean Square Error ( `RMSE` )

![RMSE](Image/RMSE.png)

- Square Root of MSE
- RMSE is useful when `Large` Errors are Undesired

### 3. Mean Absolute Error ( `MAE` )

![MAE](Image/MAE.png)

- Absolute Difference between `Actual` Value and `Predicted` Value.
- MAE is better for **Outliers** 
- All **Individual Differences** are weighted equally.

### 4. Coefficient of Determination ( R<sup>2</sup> )

![R2](Image/R2.png)

- Help us to `Compare` **Current** Model with the **Base** Model.
- R<sup>2</sup> is always <= 1 ( Ranges between `-inf` to `1` )

### 5. Adjusted R<sup>2</sup>
- Improvement of R<sup>2</sup>
- Adjusted R<sup>2</sup> is always `lower` than R<sup>2</sup>

### Logistic Regression
1. Classification Report
2. Confusion Matrix
3. F1 Score, Precision, Recall ( Sensitivity ), Specificity, AUC 
