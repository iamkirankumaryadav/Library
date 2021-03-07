# Regression Metrics

1. We **Start** with some Initial Configuration of Model and `Predict` the **Output** based on some **Input**.
2. Predicted Value is compared with the `Target` and Measure the `Performance` of our Model.
3. Various Parameters of the Model are `Adjusted Iteratively` in order to reach the **Optimal Value** of the **Performance Metric**.

### Linear Regression
- `Predict` **Dependent Variable** on the basis of One or more **Independent** Variable ( s )

### 1. Mean Absolute Error ( `MAE` )

![MAE](Image/MAE.png)

- Absolute Difference between `Actual` Value and `Predicted` Value.
- MAE is better for **Outliers** 
- All **Individual Differences** are weighted equally
- `Fails` in case of **Large Errors**

![MAE Scikit Learn](Image/MAESK.png)

### 2. Mean Squared Error ( `MSE` ) 

![MSE](Image/MSE.jpg)

- Squared Difference between the `Actual` Value and the `Predicted` Value
- Square the Differences, Penalizes even Samll Error

![MSE Scikit Learn](Image/MSESK.png)

### 3. Root Mean Square Error ( `RMSE` )

![RMSE](Image/RMSE.png)

- Square Root of MSE
- RMSE is useful when `Large` Errors are Undesired

### 4. Coefficient of Determination ( R<sup>2</sup> )

![R2](Image/R2.png)

- Square of `Correlation`
- Help us to `Compare` **Current** Model with the **Base** Model

![R2 Score Scikit Learn](Image/R2Score.png)

- R<sup>2</sup> is always <= 1 ( Ranges between `-inf` to `1` )

![R2 Goog or Bad](Image/R2Good.png)

### 5. Adjusted R<sup>2</sup>
- Improvement of R<sup>2</sup>
- Adjusted R<sup>2</sup> is always `lower` than R<sup>2</sup>

| MAE or MSE or RMSE | R<sup>2</sup> |
| :--- | :--- |
| Good Model : Value closer to Zero | Good Model : Value closer to One |
| Perfect Model : Value == 0 | Perfect Model : Value == 1 |

### Logistic Regression
- `Predict` the `Class` | `Label` of a **Data Point** on the basis of One or more **Independent Features**.
- Depending on the number of `Class` | `Label` that **Target Variable** includes, it can be `Binary` or `Multi Class` **Classification**.

> Data Set should contain Well `Balanced` **Class Distribution**

### 1. Classification Accuracy 
- Number of `Correct` Prediction to the Number of **Total Predictions**
- Accuracy Score is Good if Datasets contains well `Balanced` Class Distribution

![Accuracy](Image/Accuracy.png)

### 2. Confusion Matrix
- Show `Correct` and `Incorrect` Predictions | Classifications on each **Class** | **Label**

![Confusion Matrix](Image/ConfusionMatrix.png)

### 3. Precision
- Focus on `Positive Predictions` ( How Good our Model is when **Prediction** is `Positive` ? )
- **Evaluates** Model only based on `Positive Predictions`

![Precision](Image/Precision.png)

### 4. Recall | True Positive Rate ( `TPR` ) | Sensitivity
- Focus on `Positive Class` ( How Good our Model is at `Correctly` predicting `Positive` Classes ? )
- **Evaluates** Model only based on its **ability** to  **Predict** the `Positive Class`
- **True Positive Rate** : Proportion of **Positive Class** that is `Correctly` Predicted as **Positive**

![Recall](Image/Recall.png)

### 4. False Positive Rate ( `FPR` ) | Specificity
- Focus on `Negative Class` ( How Good our Model is at `Correctly` predicting `Negative` Classes ? )
- **Evaluates** Model only based on its **ability** to  **Predict** the `Negative Class`
- **False Positive Rate** : Proportion of **Negative Class** that is `Correctly` Predicted as **Negative**

![FPR](Image/FPR.png)

### 6. F1 Score
- Weighted Average of **Precision** and **Recall**
- Useful for Datasets with `Uneven` **Class Distribution**
- It considers `FP` and `FN`
- `Best` Value for **F1 Score** is `1`
- `Worst` Value for **F1 Score** is `0`

![F1](Image/F1.png)


