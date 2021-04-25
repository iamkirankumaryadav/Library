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
        <li>Recall | <a href='#tpr'>TPR</a> | Sensitivity</li>
        <li><a href='#fpr'>FPR</a> | Specificity</li>
        <li><a href='#f1'>F1 Score</a></li>
        <li><a href='#roc'>ROC</a></li>
        <li><a href='#auc'>AUC</a></li>
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

- `Absolute` Difference between **Actual Value** and **Predicted Value**.
- `MAE` is better for **Outliers**, `Fails` in case of **Large Errors**

![MAE Scikit Learn](Image/MAESK.png)

<h3 name='mse'>2. Mean Squared Error ( MSE ) | LOSS</h3>

![MSE](Image/MSE.jpg)

- `Squared` Difference between the **Actual Value** and the **Predicted Value**.
- **Square** Differences, **Penalizes** even **Samll Error**.

![MSE Scikit Learn](Image/MSESK.png)

<h3 name='rmse'>3. Root Mean Square Error ( RMSE )</h3>

![RMSE](Image/RMSE.png)

- **Square Root** of `MSE`, `RMSE` is useful when `Large` Errors are **Undesired**.

<h3 name='r2'>4. Coefficient of Determination ( R<sup>2</sup> ) | Squared Correlation Coefficient</h3>

![R2](Image/R2.png)

- Helps to Understand How well the Model **Fits** the Data and How well the Model **Predicts** New Observations.
- Ideal Value for R<sup>2</sup> is between 70% to 90% ( Model Fits the Data very Well )
- Help us to `Compare` **Current** Model with the **Base** Model.

![R2 Score Scikit Learn](Image/R2Score.png)

![R2 Goog or Bad](Image/R2Good.png)

<h3 name='ar2'>5. Adjusted R<sup>2</sup></h3>

- Improvement of R<sup>2</sup> ( Adjusted R<sup>2</sup> is always `lower` than R<sup>2</sup> )
- Compare Models with different number of **Predictors** | **Independent Features**.
- Adjusted R<sup>2</sup> **Increases** only if the New Term ( Independent Feature ) Improves the Model **More** than Expected.
- Adjusted R<sup>2</sup> **Decreases** if the New Term ( Independent Feature ) Improves the Model **Less** than Expected.
- Provides **More Accurate Correlation** between Variables.

| MAE or MSE or RMSE | R<sup>2</sup> | R<sup>2</sup> ( Adj )
| :--- | :--- | :---
| Good Model : Value closer to Zero | Good Model : Value closer to One | Increases only if New Term Improves Model More
| Perfect Model : Value == 0 | Perfect Model : Value == 1 | Decreases if New Term does not Improves Model Well

<h3 name="logistic">Logistic Regression | Classification</h3>

- **Predict** the `Class` | `Label` of a **Data Point** on the basis of One or more **Independent Features**.
- Depending on the number of `Class` | `Label` that **Target Variable** includes, it can be `Binary` or `Multi Class` **Classification**.
- Data Set should contain Well `Balanced` **Class Distribution**
- **Good Classifier** : `1 or 100%` | **Bad Classifier** < `0.5 or 50%`

<h3 name='cm'>1. Confusion Matrix</h3>

- Show `Correct` and `Incorrect` Predictions | Classifications on each **Class** | **Label**

![Classification](Image/Classification.png)

- **True Positive** ( `TP` ) : Predicts `1` | `Positive` when Actual is `1` | `Positive` 
- **True Negative** ( `TN` ) : Predicts `0` | `Negative` when Actual is `0` | `Negative` 
- **False Positive** ( `FP` ) : Predicts `1` | `Positive` when Actual is `0` | `Negative` ( `Type I` Error | Incorrect **True Prediction** )
- **False Negative** ( `FN` ) : Predicts `0` | `Negative` when Actual is `1` | `Positive` ( `Type II` Error | Incorrect **False Prediction** )

> **FP** is `Acceptable` but **FN** is Dangerous | Fatal for Problems related to **Medical Field**

![Confusion Matrix](Image/ConfusionMatrix.png)

<h3 name='acc'>2. Accuracy</h3>

- Number of `Correct` Prediction to the Number of **Total Predictions**
- Accuracy Score is Good if Datasets contains well `Balanced` **Class Distribution**.
- Used when All the Classes ( `TP`, `TN`, `FP` and `FN` ) are **Equally** Important.

![Accuracy](Image/Accuracy.png)

<h3 name='pre'>3. Precision</h3>

- Focus on **Positive** `Predictions` ( How Good our Model is when **Prediction** is `Positive` ? )
- Measures the **Correctly** Identified **Positive Cases** from all the **Predicted Positive Cases**.
- Used when the **Cost** of False Positives ( `FP` ) is **High**. ( e.g. There is Virus but still Antivirus is Predicting that the System is Safe it's Costly )
- **Evaluates** Model only based on **Positive Predictions**.

![Precision](Image/Precision.png)

<h3 name='tpr'>4. Recall | True Positive Rate ( TPR ) | Sensitivity</h3>

- Focus on **Positive** `Class` ( How Good our Model is at `Correctly` predicting `Positive` **Classes** ? )
- Measures the **Correctly** Identified **Positive Cases** from all the **Actual Positive Cases**. 
- Used when the **Cost** of False Negatives ( `FN` ) is **High**. ( e.g. Person is Really prone to COVID 19 but Test Result is Negative it can be Fatal. )
- **True Positive Rate** : Proportion of **Positive Class** that is `Correctly` Predicted as **Positive**.

![Recall](Image/Recall.png)

<h3 name='fpr'>5. False Positive Rate ( FPR ) | Specificity</h3>

- Measures the **Incorrectly** Identified **Positive Cases** from all the **Actual Negative Cases**. 
- **False Positive Rate** : Proportion of **Negative Class** that is `Incorrectly` Predicted as **Positive**.

![FPR](Image/FPR.png)

### **Precision**, **TPR** and **FPR** is a Better Metric for Imbalanced Data Set because it **Focus** on only **One Class**.

<h3 name='f1'>6. F1 Score</h3>

- Weighted Average ( Harmonic Mean ) of **Precision** and **Recall**
- Useful for Datasets with `Uneven` | `Imbalanced` **Class Distribution** and it also considers FP and FN.
- **Better Measure** for the **Incorrectly Classified Cases** than the **Accuracy Metric**.
- **Accuracy** is used when `TP` and `TN` are more **Important* and **F1 Score** is used when `FN` and `FP` are more **Crucial**.
- **F1-score** is a **Better Metric** to **Evaluate** in **Real Life Application**.
- **F1 Score** Keeps a `Balance` between **Recall** and **Precision** for the **Classifier** | **Model**.
- `Best` Value for **F1 Score** is `1` | `Worst` Value for **F1 Score** is `0`

![F1](Image/F1.png)

> **Precision**, **Recall** and **F1 Score** are better `Metrics` for **Imbalanced Dataset**

<h3 name='roc'>7. ROC | Receiver Operating Characteristic Curve</h3>

- Helps to Understand **Characteristics** of Curve by plotting `TPR` on **Y Axis** and `FPR` on **X Axis** at different Classification **Thresholds**.
- **Y Axis** : True Positive Rate ( `TPR` ) vs **X Axis** : False Positive Rate ( `FPR` )
- **Plots** `TPR` vs `FPR` at Different Classification `Thresholds`
- If Threshold is near to `1.0` or `100%`: **Classifications** gets more **Accurate**.

![ROC](Image/ROC.svg)

<h3 name='auc'>8. AUC | Area Under ROC Curve</h3> 

- Helps to Understand **Performance** of a **Classification Model** across all Classification `Thresholds`.
- AUC = 1.0 ( **Perfect** Classifier ) | AUC > 0.75 ( **Good** Classifier ) | AUC : **50%** ( **Bad** Classifier ) | AUC < 0.5 ( **Worst** Classifier )

![AUC](Image/AUC.png)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
