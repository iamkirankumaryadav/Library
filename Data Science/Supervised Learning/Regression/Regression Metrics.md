<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Regression Metrics 🧮

<table align=center>
  <tr><th colspan=2><h3>Metrics</h3></th></tr>
  <tr>
    <td><h3>Regression :</h3>
      <ol>
        <li>Mean Absolute Error ( <a href='#mae'>MAE</a> )</li>
        <li>Mean Squared Error ( <a href='#mse'>MSE</a> )</li>
        <li>Room Mean Squared Error ( <a href='#rmse'>RMSE</a> )</li>
        <li>Coefficient of Determination ( <a href='#r2'>R<sup>2</sup></a> )</li>
        <li>Adjusted R<sup>2</sup> ( <a href='#ar2'>Adj R<sup>2</sup></a> )</li>
      </ol>
    </td>
    <td><h3>Classification :</h3>
       <ol>
        <li><a href='#cm'>Confusion Matrix</a></li>
        <li><a href='#acc'>Accuracy</a></li>
        <li><a href='#pre'>Precision</a></li>
        <li>Recall | <a href='#tpr'>FPR</a> | Sensitivity</li>
        <li><a href='#fpr'>FPR</a> | Specificity</li>
        <li><a href='#f1'>F1 Score</a></li>
        <li><a href='#roc'>ROC</a></li>
        <li><a href='#auc'>AUC</a></li>
      </ol>
    </td>
  </tr>
</table>

<a href="#linear"> <h3> Linear Regression </h3> </a> 

<a href="#logistic"> <h3> Logistic Regression | Classification </h3> </a>

1. We **Start** with some Initial Configuration of Model and `Predict` the **Output** based on some **Input**.
2. Predicted Value is compared with the `Target` and Measure the `Performance` of our Model.
3. Various Parameters of the Model are `Adjusted Iteratively` in order to reach the **Optimal Value** of the **Performance Metric**.

<h3 name="linear">Linear Regression</h3>

- `Predict` **Dependent Variable** on the basis of One or more **Independent** Variable ( s )

<h3 name='mae'>1. Mean Absolute Error ( MAE ) </h3>

![MAE](Image/MAE.png)

- Absolute Difference between `Actual` Value and `Predicted` Value.
- MAE is better for **Outliers** 
- All **Individual Differences** are weighted equally
- `Fails` in case of **Large Errors**

![MAE Scikit Learn](Image/MAESK.png)

<h3 name='mse'>2. Mean Squared Error ( MSE ) | LOSS</h3>

![MSE](Image/MSE.jpg)

- Squared Difference between the `Actual` Value and the `Predicted` Value
- Square the Differences, Penalizes even Samll Error

![MSE Scikit Learn](Image/MSESK.png)

<h3 name='rmse'>3. Root Mean Square Error ( RMSE )</h3>

![RMSE](Image/RMSE.png)

- Square Root of MSE
- RMSE is useful when `Large` Errors are Undesired

<h3 name='r2'>4. Coefficient of Determination ( R<sup>2</sup> )</h3>

![R2](Image/R2.png)

- Square of `Correlation`
- Help us to `Compare` **Current** Model with the **Base** Model

![R2 Score Scikit Learn](Image/R2Score.png)

- R<sup>2</sup> is always <= 1 

![R2 Goog or Bad](Image/R2Good.png)

<h3 name='ar2'>5. Adjusted R<sup>2</sup></h3>

- Improvement of R<sup>2</sup>
- Adjusted R<sup>2</sup> is always `lower` than R<sup>2</sup>

| MAE or MSE or RMSE | R<sup>2</sup> |
| :--- | :--- |
| Good Model : Value closer to Zero | Good Model : Value closer to One |
| Perfect Model : Value == 0 | Perfect Model : Value == 1 |

<h3 name="logistic">Logistic Regression | Classification</h3>

- `Predict` the `Class` | `Label` of a **Data Point** on the basis of One or more **Independent Features**.
- Depending on the number of `Class` | `Label` that **Target Variable** includes, it can be `Binary` or `Multi Class` **Classification**.

> Data Set should contain Well `Balanced` **Class Distribution**

> **Good Classifier** : `1 or 100%` | **Bad Classifier** < `0.5 or 50%`

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
- Accuracy Score is Good if Datasets contains well `Balanced` Class Distribution
- Used when All the Classes ( TP, TN, FP and FN ) are Equally Important.

![Accuracy](Image/Accuracy.png)

<h3 name='pre'>3. Precision</h3>

- Focus on `Positive Predictions` ( How Good our Model is when **Prediction** is `Positive` ? )
- Measures the **Correctly** Identified Positive Cases from all the **Predicted** Positive Cases.
- Used when the Costs of False Positives is **High**. ( e.g. There is Virus but still Antivirus is Predicting that the System is Safe it's Costly )
- **Evaluates** Model only based on `Positive Predictions`

![Precision](Image/Precision.png)

<h3 name='tpr'>4. Recall | True Positive Rate ( `TPR` ) | Sensitivity</h3>

- Focus on `Positive Class` ( How Good our Model is at `Correctly` predicting `Positive` Classes ? )
- **Evaluates** Model only based on its **ability** to  **Predict** the `Positive Class`
- Measures the Correctly identified Positive Cases from all the **Actual Positive Cases**. 
- Used when the Cost of False Negatives is **High**. ( e.g. Person is Really prone to COVID 19 but Test Result is Negative it can be Fatal. )
- **True Positive Rate** : Proportion of **Positive Class** that is `Correctly` Predicted as **Positive**

![Recall](Image/Recall.png)

<h3 name='fpr'>4. False Positive Rate ( `FPR` ) | Specificity</h3>

- Focus on `Negative Class` ( How Good our Model is at `Correctly` predicting `Negative` Classes ? )
- **Evaluates** Model only based on its **ability** to  **Predict** the `Negative Class`
- **False Positive Rate** : Proportion of **Negative Class** that is `Correctly` Predicted as **Negative**

![FPR](Image/FPR.png)

### **Precision**, **TPR** and **FPR** is a Better Metric for Imbalanced Data Set because it **Focus** on only **One Class**.

<h3 name='f1'>5. F1 Score</h3>

- Weighted Average of **Precision** and **Recall**
- Useful for Datasets with `Uneven` | `Imbalanced` **Class Distribution** and it also considers FP and FN.
- A Better Measure of the Incorrectly Classified Cases than the Accuracy Metric.
- Accuracy is used when TP and TN are more Important and F1 Score is used when FN and FP are more Crucial.
- **F1-score** is a Better Metric to Evaluate in **Real Life Application**.
- `Best` Value for **F1 Score** is `1` | `Worst` Value for **F1 Score** is `0`

![F1](Image/F1.png)

> **Precision**, **Recall** and **F1 Score** are better `Metrics` for **Imbalanced Dataset**

<h3 name='roc'>6. ROC Curve</h3>

- Receiver Operating Characteristic Curve
- Y Axis : True Positive Rate ( `TPR` )
- X Axis : False Positive Rate ( `FPR` )
- Plots TPR vs FPR at Different Classification `Thresholds`
- If Threshold is near to `1.0` or `100%`: **Classifications** gets more **Accurate**.

![ROC](Image/ROC.svg)

<h3 name='auc'>7. AUC</h3> 

- `Area` Under **ROC Curve**
- Shows the `Performance` of a Classification Model across all Classification `Thresholds`.
- AUC = 1.0 ( **Perfect** Classifier ) | AUC > 0.75 ( **Good** Classifier ) | AUC : **50%** ( **Bad** Classifier ) | AUC < 0.5 ( **Worst** Classifier )

![AUC](Image/AUC.png)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
