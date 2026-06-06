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

### 🎯 How do you evaluate the performance of an ML model?
```
📝 First, we give some input data to the model with initial configuration and let it make predictions.
🔍 We compare the model's predictions with the actual correct answers.
📊 We calculate performance metrics (Accuracy, Precision, Recall) to see how well the model is performing.
🔄 Based on these metrics, we adjust the model's parameters and train it again to improve its performance.
📈 This process is repeated until the model reaches the best possible performance.
🧪 We then test the model on new, unseen data to check how well it generalizes.
🏆 Finally, we select the model that performs best on unseen data.
🚨 Compare it with other models to choose the most suitable one for the task.
```

<h2 name="linear">Linear Regression</h2>

🔮 Predicts continuous numeric dependent variables based on one or more independent variables.

<h3 name='mae'>1. Mean Absolute Error (MAE) </h3>

![MAE](Image/MAE.png)
```
📏 MAE measures the average difference between the actual values and the predicted values.
➖ It calculates the absolute difference, ignores whether the error is positive (+) or negative (-).
📐 The MAE value is expressed in the same unit as the target variable (Y), making it easy to understand.
😊 Since it uses absolute values instead of squaring the errors, MAE is less sensitive to outliers.
📉 A lower MAE means the model's predictions are closer to the actual values, indicating better performance.
```

![MAE Scikit Learn](Image/MAESK.png)

<h3 name='mse'>2. Mean Squared Error (MSE) | LOSS</h3>

![MSE](Image/MSE.jpg)
```
📏 MSE measures the average of the squared differences between the actual values and the predicted values.
🔢 Instead of taking the absolute value like MAE, MSE squares each error before averaging.
⚠️ Because errors are squared, large errors get much bigger, making MSE highly sensitive to outliers.
📐 The unit of MSE is squared units (e.g., ₹², m², kg²), which makes it less intuitive to interpret than MAE.
➕➖ Squaring the errors removes negative signs, so MSE is always zero or positive.
📉 A lower MSE means the model's predictions are closer to the actual values and the model is performing better.
```

![MSE Scikit Learn](Image/MSESK.png)

<h3 name='rmse'>3. Root Mean Square Error (RMSE)</h3>

![RMSE](Image/RMSE.png)
```
📏 RMSE is the square root of MSE (Mean Squared Error).
📐 Unlike MSE, RMSE is expressed in the same unit as the target variable, making it easier to understand.
⚠️ Since RMSE is based on squared errors, large errors receive a higher penalty than small errors.
🎯 RMSE is especially useful when large prediction errors are undesirable and need to be minimized.
🤝 RMSE combines:
  ✅ MAE's Advantage: Same unit as the target variable.
  ✅ MSE's Advantage: Penalizes large errors more strongly.
📉 A lower RMSE means the model's predictions are closer to the actual values and the model is performing better.
```

MAE | MSE | RMSE
:--- | :--- | :---
Absolute (Actual - Predicted) | Squared (Actual - Predicted) | Square Root (MSE)
Good for small errors | Magnify small errors | Shrinks down larger errors
Units of predicted value remain same | Unit gets squared | Units remain same
Less sensitive towards outliers | More sensitive towards outliers | Less sensitive towards outliers

<h3 name='r2'>4. Coefficient of Determination (R<sup>2</sup>) | Squared Correlation Coefficient</h3>

![R2](Image/R2.png)
```
📊 R² measures how well the model explains the variation in the target variable (Y).
📈 It tells us how closely the data points fit the regression line.
🔍 In simple terms, R² shows how much of the changes in Y can be explained by the input variables (X).
🎯 A higher R² value generally means the model fits the data better.

🔴 R² = 0
  The model explains none of the variation in the target variable.
  It performs no better than simply predicting the average value.

🟡 R² = 0.50
  The model explains 50% of the variation in the target variable.

🟢 R² = 1
  The model explains 100% of the variation.
  Predictions perfectly match the actual values.

📏 Measures how well the model fits the data.
📊 Helps compare the model against a simple baseline (predicting the mean).
🔍 Shows how much variance in Y is explained by X.
🏆 Helps compare multiple regression models.

➕ Adding more features always increases R², even if the new features are not useful.
🚨 Therefore, a higher R² does not always mean a better model.
⚠️ A very high R² does not automatically mean overfitting, but it can be a warning sign.
```
  
![R2 Score Scikit Learn](Image/R2Score.png)

![R2 Goog or Bad](Image/R2Good.png)

<h3 name='ar2'>5. Adjusted R<sup>2</sup></h3>

```
📈 Adjusted R² is an improved version of R².
🔍 While R² always increases (or stays the same) when new features are added.
⚡ Adjusted R² increases only if the new feature actually improves the model.
📊 Therefore, Adjusted R² is a more reliable measure of model performance than R².
📉 Adjusted R² is usually lower than or equal to R².
🏆 It is especially useful when comparing models with different numbers of independent variables (features).
```

MAE or MSE or RMSE | R<sup>2</sup> | R<sup>2</sup> ( Adj )
:--- | :--- | :---
Good Model: Value closer to 0 | Good Model: Value closer to 1 | Increases only if new term improves model
MAE (Small errors), RMSE (Large errors) | Measures variability | Good if the dataset has many independent variables

<h2 name="logistic">Logistic Regression | Classification</h2>

```
🏷️ Classification is a ML technique used to predict a class label based on one or more input features.
🔍 Instead of predicting a number (like Regression), Classification predicts a label such as:
  Spam / Not Spam 📧
  Fraud / Not Fraud 💳
  Pass / Fail 🎓
  Disease / No Disease 🏥

1️⃣ Binary Classification: When there are only two possible classes.

Examples:
✅ Yes / ❌ No
😊 Positive / 😞 Negative
📧 Spam / Not Spam

2️⃣ Multiclass Classification: When there are more than two classes.

Examples:
🐱 Cat | 🐶 Dog | 🐰 Rabbit
🔴 Red | 🔵 Blue | 🟢 Green

⚖️ Balanced Dataset:
A good classification model works best when the dataset has a balanced distribution of classes.

Example of Balanced Data: Total Students = 100
👦 Boys = 50
👧 Girls = 50
This is balanced because both classes have similar numbers.

Example of Imbalanced Data: Total Students = 100
👦 Boys = 95
👧 Girls = 5
This is imbalanced and can lead to biased predictions.
```
- Predict the category or class label of a data point based on one or more independent features.
- Depending on the number of class labels in the target variable, it can be a Binary or Multiclass classification.
- The data set should contain a well-balanced class distribution. (e.g. Total Students = 100 | 50 Boys + 50 Girls)
- Good Classifier: 1 or 100% | Bad Classifier: < 0.5 or 50%

<h3 name='cm'>1. Confusion Matrix</h3>

```
📊 A Confusion Matrix is a table used to evaluate the performance of a classification model.
🔍 It shows how many predictions were correct and how many were incorrect.
🏷️ It helps us understand how well the model is classifying each class label.
🎯 Instead of looking only at accuracy, a confusion matrix provides a detailed breakdown of predictions.

It helps calculate important metrics:
📊 Accuracy
🎯 Precision
🔍 Recall
⚖️ F1 Score
These metrics are all derived from: TP, TN, FP, and FN.
```

![Classification](Image/Classification.png)

```
True Positive  (TP): Predicts 1 when Actual is 1 
True Negative  (TN): Predicts 0 when Actual is 0 
False Positive (FP): Predicts 1 when Actual is 0 | Type I Error  | Incorrect True Prediction 
False Negative (FN): Predicts 0 when Actual is 1 | Type II Error | Incorrect False Prediction 

📊 There is no single best evaluation metric for every problem.
🎯 The right metric depends on the business goal and the cost of different types of errors.
⚠️ Sometimes a False Positive (FP) is more costly, while in other cases a False Negative (FN) is more dangerous.
```

![Confusion Matrix](Image/ConfusionMatrix.png)

<h3 name='acc'>2. Accuracy</h3>

```
📊 Accuracy measures the percentage of predictions that the model got correct.
🤔 It answers the question: "Out of all predictions, how many were correct?"
🎯 In simple words, Accuracy tells us how often the model is right.
💡 The ratio of correct predictions to the total number of predictions.
⚖️ Accuracy score is good for balanced datasets, but misleading for imbalanced datasets.

📐 Formula: Accuracy =  TP+TN / TP+TN+FP+FN
	​
Where:
  ✅ TP (True Positive) = Correct Positive Predictions
  ✅ TN (True Negative) = Correct Negative Predictions
  ❌ FP (False Positive) = Wrong Positive Predictions
  ❌ FN (False Negative) = Wrong Negative Predictions

Use Accuracy when:
  ✅ Dataset is balanced
  ✅ TP, TN, FP, and FN are equally important
```

![Accuracy](Image/Accuracy.png)

<h3 name='pre'>3. Precision</h3>

- When the model says Yes/True/1, how often is it correct? Can I trust the positive predictions?
- Measures the **correctly identified positive cases** (TPs) from all the **predicted positive cases**.
- Precision is a crucial metric when minimizing **False Positives (FP)** is a priority. (e.g. Antivirus, Spam Filtering)
- **TP:** The number of instances that were correctly classified as positive.
- **FP:** The number of instances that were incorrectly classified as positive.

![Precision](Image/Precision.png)

<h3 name='tpr'>4. Recall | True Positive Rate (TPR) | Sensitivity</h3>

- Out of all actual positive cases, how many did the model find? Did the model miss any?
- The ratio of **true positive predictions** (TPs) to the **total actual positives**.
- Measures the **correctly identified positive cases** (TPs) from all the **actual positive cases**. 
- Recall is a crucial metric when minimizing **False Negatives (FN)** is a priority. (e.g. Medical Diagnosis, Corona, Fraud Detection)
- **FN:** The number of instances that were incorrectly classified as negative.

Example: Medical Diagnosis
1. Precision: FP (Incorrectly diagnosing a healthy person can lead to unnecessary treatment)
2. Recall: FN (Incorrectly diagnosing a sick person as healthy can lead to delayed treatment)

Example: Fraud Detection
1. Precision: FP (Flagging a genuine transaction as fraudelent can damage customer relationships)
2. Recall: FN (Failing to detect fraudelent claims can result in significant financial losses)

![Recall](Image/Recall.png)

<h3 name='fpr'>5. False Positive Rate (FPR) | Specificity</h3>

- Measures the **incorrectly identified positive** cases from all the **actual negative cases**. 
- **False Positive Rate**: Proportion of negative class that is incorrectly predicted as **positive**.

![FPR](Image/FPR.png)

<h3 name='f1'>6. F1 Score | F Measure</h3>

- F1 Score is a harmonic mean of precision and recall (Balance between precision and recall).
- Useful for imbalanced datasets (Uneven class distribution) and it also considers FP and FN.
- **Accuracy** is used when TP and TN are more important.
- **Precision** is used when FP is crucial (Antivirus is showing that the system is safe, even if it's affected by a virus)
- **Recall** is used when FN is risky (Medical diagnosis, Covid test is showing negative, even if the patient is affected)
- **F1 Score** is used when minimizing FN and FP are more crucial.
- **F1-score** is a better metric to evaluate in **real life application**.
- Best value for **F1 Score** is 1 | Worst value for **F1 Score** is 0.
- **Precision**, **Recall** and **F1 Score** are better metrics for imbalanced dataset.

![F1](Image/F1.png)

### Support
- Support refers to the number of actual occurences of each class in the dataset.
- It essentially counts how many times each class appears in the true labels of the data.

<h3 name='roc'>7. ROC | Receiver Operating Characteristic</h3>

- Explains the characteristics of curves by plotting, TPR on the Y-axis and FPR on the X-axis at different classification thresholds.
- The ROC curve helps to select the optimal threshold for a classifier.
- If the threshold is closer to 1.0 or 100%: **Classifications** get more accurate.

![ROC](Image/ROC.svg)

<h3 name='auc'>8. AUC | Area Under ROC Curve</h3> 

- Helps to understand the performance of a classification model across all the classification thresholds.

**Score** | **Classifier**
--- | ---
AUC = 1.0 | Perfect Classifier  
AUC > 0.75 | Good Classifier 
AUC > 0.5 | Bad Classifier 
AUC < 0.5 | Worst Classifier

![AUC](Image/AUC.png)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
