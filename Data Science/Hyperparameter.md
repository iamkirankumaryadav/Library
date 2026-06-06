<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

### 🎛️ Hyperparameters

```
✅ The settings or controls you choose before training ML model.
✅ Configuration variables that control the learning process of an ML model.
✅ Adjustable settings that must be tuned to obtain a model with optimal performance.
✅ Greatly impact the ML model's behaviour and performance.
✅ Significantly improve a model's accuracy, speed, and generalization.
```

### ⚙️ Parameters
```
✅ Values in a model that are updated during the training of the model.
✅ Learn from the data and automatically adjust during the training.
```

### 🤔 Hyperparameters vs Parameters
Hyperparameters |	Parameters
:--- | :---
Set before training |	Learned during training
Control the learning process | Store what the model has learned
Chosen by the user | Automatically updated by the model

### 🚀 Why Are Hyperparameters Important?
```
The right hyperparameters can help a model:
✅ Learn faster
✅ Become more accurate
✅ Avoid mistakes (overfitting/underfitting)
✅ Perform well on new data
```
### 🎯 Hyperparameter Tuning

```
✅ Process of finding the best hyperparameters for a ML model so that it performs as well as possible.
✅ Experimenting with different combinations of hyperparameters and evaluating the model's performance on a validation set.
✅ An iterative, time-consuming process that needs computing power, but essential for building high-performing models.
```

### 🔄 How It Works
```
1. Choose a set of hyperparameter values.
2. Train the model.
3. Test it on validation data.
4. Measure its performance.
5. Try another combination.
6. Repeat until the best settings are found.
```

### 🚀 Why is it Important?
```
The right hyperparameters can help a model:
✅ Achieve higher accuracy
✅ Learn more efficiently
✅ Make better predictions on new data
✅ Avoid overfitting and underfitting
```

### Hyperparameters:
- **Learning Rate:** Determines how quickly the model updates its parameters during the training.
- **Batch size:** Determines the number of data points used in each training iteration.
- **Regularization Strength:** Lasso (L1) or Ridge (L2) to prevent overfitting.
- **#epochs:** Determines the number of times the model sees the entire training dataset.
- **#layers:** Determines the number of layers in a neural network.
- **#nodes:** Determines the number of nodes/neurons in each layer of a neural network.
- **#trees:** Determines the number of decision trees in a random forest.
- **#clusters:** Determines the number of clusters in a clustering algorithm.

**Model** | **Hyperparameter**
:--- | :---
**Linear Regression** | Regularization parameter (alpha for Lasso or Ridge Regression)
**Logistic Regression** | C (Inverse of regularization strength), penalty (L1, L2)
**Decision Tree** | Max_depth, min_samples_split, min_samples_leaf, criterion
**K Nearest Neighbors** | n_neighbors, weights, metric
