<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">Back to ML</a></p>

# Metrics 🧮

<table align=center> 
  <tr><th><h3><a href="#linear"> Regression</a></h3></th><th><h3><a href="#logistic">Classification</a></h3></th></tr>
  <tr>
    <td>
      <ol>
        <li>Mean Absolute Error ( <a href='#mae'>MAE</a> )</li>
        <li>Mean Squared Error ( <a href='#mse'>MSE</a> )</li>
        <li>Root Mean Squared Error ( <a href='#rmse'>RMSE</a> )</li>
        <li>Coefficient of Determination ( <a href='#r2'>R<sup>2</sup></a> )</li>
        <li>Adjusted R<sup>2</sup> ( <a href='#ar2'>Adj R<sup>2</sup></a> )</li>
      </ol>
    </td>
    <td>
       <ol>
        <li><a href='#cm'>Confusion Matrix</a></li>
        <li><a href='#acc'>Accuracy</a></li>
        <li><a href='#pre'>Precision</a></li>
        <li>Recall | True Positive Rate ( <a href='#tpr'>TPR</a> ) | Sensitivity</li>
        <li>False Positive Rate ( <a href='#fpr'>FPR</a> ) | Specificity</li>
        <li><a href='#f1'>F1 Score</a> or F Measure</li>
        <li><a href='#roc'>ROC</a> | Receiver Operating Characteristic Curve</li>
        <li><a href='#auc'>AUC</a> | Area Under Curve</li>
      </ol>
    </td>
  </tr>
</table>

1. **Start** with some **Initial Configuration** of **Model** and `Predict` the **Output** based on some **Input**.
2. **Compare Predicted Value** with `Target` and **Measure** the `Performance` of our Model.
3. **Parameters** of the **Model** are `Adjusted` **Iteratively** in Order to reach the **Optimal Value** of the **Performance Metric**.

<h3 name="linear">Linear Regression</h3>

- `Predict` **Dependent Variable** on the basis of One or more **Independent** Variable ( s )

<h3 name='mae'>1. Mean Absolute Error ( MAE ) </h3>

![MAE](Image/MAE.png)

- `Sum` of `Absolute` difference between **Actual** and **Predicted** values.
- `MAE` is better for **Outliers**, `Fails` in case of **Large Errors**

![MAE Scikit Learn](Image/MAESK.png)

<h3 name='mse'>2. Mean Squared Error ( MSE ) | LOSS</h3>

![MSE](Image/MSE.jpg)

- `Sum` of `Squared` difference between **Actual** and **Predicted** values.
- **Square** Differences, **Penalizes** even `Small` Error.

![MSE Scikit Learn](Image/MSESK.png)

<h3 name='rmse'>3. Root Mean Square Error ( RMSE )</h3>

![RMSE](Image/RMSE.png)

- **Square Root** of `MSE`, `RMSE` is useful when `Large` Errors are **Undesired**.

<h3 name='r2'>4. Coefficient of Determination ( R<sup>2</sup> ) | Squared Correlation Coefficient</h3>

![R2](Image/R2.png)

- Helps to understand how well the model `Fits` the data | How well the model `Predicts` new observations.
- Measure how `Close` each **data point** `Fits` the **Regression Line** | How well the **Regression Line** `Predicts` **Actual Values**.
- Ideal Value for R<sup>2</sup> is between `70%` to `90%` ( Model `Fits` the data very well )
- Help us to `Compare` **Created** model with the **Base** model.

![R2 Score Scikit Learn](Image/R2Score.png)

![R2 Goog or Bad](Image/R2Good.png)

<h3 name='ar2'>5. Adjusted R<sup>2</sup></h3>

- Improvement of R<sup>2</sup> ( Adjusted R<sup>2</sup> is always `lower` than R<sup>2</sup> )
- Compare models with different number of `Independent` features.
- Adjusted R<sup>2</sup> **Increases** only if the new `Independent` feature improves the model **More** than expected.
- Adjusted R<sup>2</sup> **Decreases** if the new `Independent` feature ) improves the model **Less** than expected.
- Provides more accurate `Correlation` between features.

| MAE or MSE or RMSE | R<sup>2</sup> | R<sup>2</sup> ( Adj )
| :--- | :--- | :---
| Good Model : Value closer to 0 | Good Model : Value closer to 1 | Increases only if new term improves model
| Perfect Model : Value == 0 | Perfect Model : Value == 1 | Decreases if new term does not improves model

<h3 name="logistic">Logistic Regression | Classification</h3>

- **Predict** the `Class` | `Label` of a data point on the basis of one or more `Independent` features.
- Depending on the number of `Class` | `Label` that `Target` variable includes, it can be `Binary` or `Multi Class` classification.
- Data set should contain well `Balanced` class distribution.
- **Good Classifier** : `1 or 100%` | **Bad Classifier** < `0.5 or 50%`

<h3 name='cm'>1. Confusion Matrix</h3>

- Show `Correct` and `Incorrect` Predictions | Classifications on each **Class** | **Label**

![Classification](Image/Classification.png)

```
True Positive ( `TP` )  : Predicts `1` | `Positive` when Actual is `1` | `Positive` 
True Negative ( `TN` )  : Predicts `0` | `Negative` when Actual is `0` | `Negative` 
False Positive ( `FP` ) : Predicts `1` | `Positive` when Actual is `0` | `Negative` ( `Type I` Error | Incorrect True Prediction )
False Negative ( `FN` ) : Predicts `0` | `Negative` when Actual is `1` | `Positive` ( `Type II` Error | Incorrect False Prediction )
```

> **FP** is `Acceptable` but **FN** is Dangerous | Fatal for Problems related to **Medical Field**

![Confusion Matrix](Image/ConfusionMatrix.png)

<h3 name='acc'>2. Accuracy</h3>

- Number of `Correct` Prediction to the Number of `Total Predictions`
- Accuracy Score is Good if Datasets contains well `Balanced` **Class Distribution**.
- Used when All the Classes ( `TP`, `TN`, `FP` and `FN` ) are **Equally** Important.

![Accuracy](Image/Accuracy.png)

<h3 name='pre'>3. Precision</h3>

- Measures the `Correctly` Identified `Positive` cases from all the `Predicted Positive` cases.
- Used when the **Cost** of False Positives ( `FP` ) is **High**. ( e.g. There is Virus but still Antivirus is Predicting that the System is Safe it's Costly )

![Precision](Image/Precision.png)

<h3 name='tpr'>4. Recall | True Positive Rate ( TPR ) | Sensitivity</h3>

- Measures the `Correctly` Identified `Positive` cases from all the `Actual Positive` cases. 
- Used when the **Cost** of False Negatives ( `FN` ) is **High**. ( e.g. Person is Really prone to COVID 19 but Test Result is Negative it can be Fatal. )
- **True Positive Rate** : Proportion of **Positive Class** that is `Correctly` Predicted as **Positive**.

![Recall](Image/Recall.png)

<h3 name='fpr'>5. False Positive Rate ( FPR ) | Specificity</h3>

- Measures the `Incorrectly` Identified `Positive` cases from all the `Actual Negative` cases. 
- **False Positive Rate** : Proportion of **Negative Class** that is `Incorrectly` Predicted as **Positive**.

![FPR](Image/FPR.png)

<h3 name='f1'>6. F1 Score</h3>

- Weighted Average ( Harmonic Mean ) of **Precision** and **Recall**.
- Represents balance between the `Precision` and `Recall`
- Useful for `Imbalanced` Datasets ( `Uneven` Class Distribution ) and it also considers `FP` and `FN`.
- **Better Measure** for the **Incorrectly Classified Cases** than the **Accuracy Metric**.
- **Accuracy** is used when `TP` and `TN` are more **Important**.
- **F1 Score** is used when `FN` and `FP` are more **Crucial**.
- **F1-score** is a better metric to evaluate in **Real Life Application**.
- **F1 Score** keeps a `Balance` between **Recall** and **Precision** for the **Classifier** | **Model**.
- `Best` value for **F1 Score** is `1` | `Worst` value for **F1 Score** is `0`

![F1](Image/F1.png)

> **Precision**, **Recall** and **F1 Score** are better `Metrics` for **Imbalanced Dataset**

<h3 name='roc'>7. ROC | Receiver Operating Characteristic Curve</h3>

- Helps to Understand **Characteristics** of Curve by plotting `TPR` on **Y Axis** and `FPR` on **X Axis** at different Classification **Thresholds**.
- **Y Axis** : True Positive Rate ( `TPR` )  
- **X Axis** : False Positive Rate ( `FPR` )
- **Plots** `TPR` vs `FPR` at Different Classification `Thresholds`
- If Threshold is near to `1.0` or `100%`: **Classifications** gets more **Accurate**.

![ROC](Image/ROC.svg)

<h3 name='auc'>8. AUC | Area Under ROC Curve</h3> 

- Helps to Understand **Performance** of a **Classification Model** across all Classification `Thresholds`.
- AUC = 1.0 ( **Perfect** Classifier ) | AUC > 0.75 ( **Good** Classifier ) | AUC : **50%** ( **Bad** Classifier ) | AUC < 0.5 ( **Worst** Classifier )

![AUC](Image/AUC.png)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
