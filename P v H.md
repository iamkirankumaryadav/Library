# **Parameters vs Hyperparameters**

### **Parameters:**

- **Learned from Data:** These are the fundamental elements a model learns during training.
- They directly represent the relationships and patterns discovered within the data.
- Coefficients in linear regression (weight of each feature)
- Weights and biases in neural networks (connections between neurons)
- Decision tree split points.

### **Hyperparameters:**

- **Set Before Training:**  These are external knobs that control how the model learns from the data.
- They are not directly learned but are crucial for guiding the learning process.
- Learning rate (controls how much the model updates its parameters)
- Number of hidden layers or neurons in a neural network
- Number of trees in a random forest. Regularization parameters (control model complexity)

**Key Differences:**

1. **Learning Process:** Parameters are **learned**, while hyperparameters are **pre-defined**.
2. **Impact:** Parameters directly affect the model's **predictions**, while hyperparameters influence the **learning process** itself.
3. **Tuning:** Parameters are not usually tuned, while hyperparameter tuning is essential to optimize the model's performance.

**Choosing the Right Values:**

* **Parameters:** The model learns the optimal values for its parameters automatically through the training process.
* **Hyperparameters:** Finding the best hyperparameters requires experimentation (grid search, random search, etc.) to evaluate the model's performance with different settings.
