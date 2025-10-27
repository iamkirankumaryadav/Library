<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Gradient Descent
- An optimization algorithm which is used while training a model, starts with defining some initial parameter values. 
- Iteratively it adjusts the values of the parameters to minimize the given **cost function** (Actual - Predicted)
- **Gradient (m)** measures how much the output of a function changes after a unit change in input.
- **Gradient (m)** guides with the magnitude and direction to minimize the cost function (reach the local minimum point) quickly.
- The higher the gradient, the steeper the slope and the faster a model can learn, once the slope is 0, the model stops learning. 

## Learning Rate
- Determines the step size taken into the direction of the local minimum point.
- It represents how fast or slow the model will move towards the local minimum point.
- Learning rate should be set to an appropriate value, neither too low nor too high. 
- If the steps are too big, they will overshoot or bounce back and forth within the convex function.
- If the steps are minimal, gradient descent will take time to reach the local minimum point.
- Flow can be tracked by plotting the **# iterations** on the x-axis and the value of the cost function on the y-axis.
- This helps to track the value of the **cost function** after each iteration of gradient descent.
- It provides a way to easily understand and visualize how appropriate your learning rate is performing.
- If the gradient descent is working perfectly, the cost function should decrease after every iteration.
- Once the cost function stops decreasing anymore and remains on the same level, it has converged (reached the local minimum point).

## Cost Function
- A cost function is a mathematical formula used to measure how well a ML model is performing.
- It calculates the difference between the actual values (ground truth) and the predicted values from the model.
- The cost function is used to guide the model's learning process by minimizing the overall cost.
- The goal is to minimize the cost function, adjusting the model's parameters to make predictions as accurate as possible.
- Type of cost functions: Predictions (MSE, MAE) and Classification (Cross Entropy Loss)

Feature | MAE | MSE
:--- | :--- | :---
Definition | Average of the absolute differences between actual and predicted values | Average of the squared differences between actual and predicted values
Sensitivity to Outliers | Less sensitive (treats all errors equally) | Highly sensitive (squares large errors)
Error Penalization | Penalizes all errors linearly | Penalizes larger errors more heavily

## Cross Entrophy Loss
- It measures the difference between the actual class labels and the predicted probabilities from a model.
- **Low Cross-Entropy Loss:** The predicted probability for the correct class is high (Correct Classification).
- **High Cross-Entrophy Loss:** The predicted probability for the correct class is low (Wrong Classification).
- It works well for both binary and multi-class classification problems.

## Stochastic Gradient Descent Algorithm
- SGD is a variant of gradient descent optimized for large datasets.
- Instead of calculating the gradient using the entire dataset, SGD randomly selects a small random subset (batch) of data points.
- SGD is used for training deep neural networks (CNNs and RNNs) and GenAI models (VAEs and GANs)
- VAN: Variational Autoencoders | GAN: Generative Adversarial Networks.
