# Bias | Variance | Underfitting | Overfitting

Bias | Variance
:--- | :---
**High** Bias ( High Error on **Train** Set \| **Underfitting** ) | **High** Variance ( High Error on **Test** Set \| **Overfitting**  )
**Low** Bias ( Low Error on **Train** Set \| Model is Trained **Well** ) | **Low** Variance ( Low Error on **Test** Set \| **Prediction** is `Close` to **Actual** )
Model is not **Trained** Properly | Model does not **Generalize** well on **New Unknown Data**
**Simple** Model is Created | **Complicated** Model is Created
Model make **Simplified Assumptions** while Learning | Model **Learn** Data with **Noise** and **Confusion**
Model do not Capture Hidden Patterns and Relations properly | Model **Memorize** Patterns and Relations + Noise + Error
Low Bias Algorithms ( Decision Tree, KNN, SVM ) | Low Variance Algorithms ( Regression, LDA )
High Bias Algorithm ( Regression ) | High Variance Algorithm ( Decision Tree, KNN, SVM ) 

> Bias | Error = Predicted - Actual ( Difference between the `Expected` Value and `True Actual` Value  )

- A `Linear` Algorithms **Learns Fast** which often lead to High Bias
- Simple the Algorithm, more Bias it will Introduce ( Capture Data with Noise and Error ).
- Non Linear Algorithms often have **Low Bias**.

### How to Reduce Bias?
- K Fold **Cross Validations** and **Resampling** | Split Data Set into K Numbers and Each Set is used as Testing Set.
- Use Algorithms that works on Non Linear Data
- **Bootstrapping** and **Boosting** | Iteratively Resampling a Data Set with Replacement.

### Bias Variance Trade Off

Increasing Bias decreases Variance and Increasing Variance decreases Bias,

Trade Off - Find the Correct Balance : Low Bias and Low Variance.   

### Underfitting | Simple Model : High Bias + Low Variance
- **High** Bias : **High** Error on Training Data ( **Underfitting** )
- The Model Fails to Characterize the Basic Data Correctly. 
- The Model and Algorithm does not Fit the Data Well enough.

### Overfitting | Complex Model : Low Bias + High Variance
- **Low** Bias : **Low** Error on Train Data ( Model is **Trained** very Well + **Noise** )
- **High** Variance : **High** Error on Test Data ( Performs Bad on **New Unseeen Data** )
- When a Massive Amount of Data Trains a Machine Learning Model, it tends to Learn from **Noise** and **Inaccurate** Data.
- Random Error and Noise | Complex Model | Too Many Parameters ( Columns ) relative to the number of Observations ( Rows ) 
- Poor **Predictive** Performance | Do not **Genralize** well on the **New Unseen Data**
- Difference between the Prediction on the Unseen Data Point and the Actual Data Point is High ( High Variance )
- Model Tries to Fit the Training Data so closely that it does not Generalize well to New Unseen Data.

Bias and Variance helps us Improve the Data Fitting | Training Process resulting in more Accurate Models.

### Error due to Bias 
- Difference between the **Expected Prediction** of our Model and the Correct Value which we are trying to Predict.
- Due to Randomness in Data Set, Bias Measures How Far off these Model's Predictions are from the Correct Value.

### Error dur to Variance
- **Variability** of a Model Prediction from an Actual Data Point
- How much the Predictions for a given point vary between different Models.

### Good Fit Model ( Low Bias and Low Variance )
- `Prediction` is Actually **Close** to the `Actual` True Data and **Model** is Trained Well
- Generalized enough to Work with any New Unseen Data ( Low Variance ) 
- **Captures** Less `Noise` and `Error` at the Time of **Training** ( Low Bias )
