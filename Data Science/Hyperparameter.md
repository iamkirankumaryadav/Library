<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Hyperparameter
- Hyperparameters are configuration variables that control and determine the learning process of an ML model.
- Hyperparameters are adjustable parameters that must be tuned to obtain a model with optimal performance.
- Model parameters learn from the data and adjust during the training, hyperparameters are set before training begins.
- Parameters are values in a model that are updated during the training of the model.
- The values of hyperparameters can greatly impact the ML model's behaviour and performance.
- The right hyperparameters can significantly improve a model's accuracy, speed, and generalization.

### Hyperparameter Tuning/Optimization
- Finding the optimal hyperparameter values is crucial for achieving the best possible performance from an ML model.
- It involves experimenting with different combinations of hyperparameters and evaluating the model's performance on a validation set.
- An iterative process that can be time-consuming but essential for building high-performing models.

### Hyperparameters:
- **Learning rate:** Determines how quickly the model updates its parameters during the training.
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
