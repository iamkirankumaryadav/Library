<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Gradient Descent
- An optimization algorithm used in training a neural network, starts by defining initial parameter values (weights) 
- Iteratively updates these parameters to minimize the cost function, difference between actual and predicted outputs.
- Measures how much the cost function changes when an input change slightly by one unit.
- Guides the magnitude and direction of change needed to minimize the cost function and reach a minimum point efficiently.
- Larger the gradient, means steeper the slope (m) and faster a model will learn, once the slope is 0, the model stops learning. 

## Learning Rate
- Learning rate determines the **step size** taken towards the minimum point of the cost function.
- It controls how fast or slow the model moves towards the minimum point.
- Learning rate must be set appropriately, neither too low nor too high. 
- If steps are too **large**, gradient descent will overshoot or bounce back and forth within the convex function.
- If steps are too **small**, gradient descent will take time to reach the local minimum point.
- If steps are **optimal**, gradient descent steadily moves toward minimum point, improving the model.
- Progress can be tracked by plotting **# iterations** on x-axis vs. the cost function value on y-axis.
- This helps to track the **cost function value** after every iteration of gradient descent.
- It helps to easily understand and visualize how appropriate your learning rate is performing.
- If the gradient descent is working perfectly, the cost function should decrease after every iteration.
- Once the cost function stops decreasing anymore, it has converged and reached the minimum point.

## Cost Function
- A cost function is a mathematical formula that measures how well a ML model performs.
- It calculates the difference between the actual values (ground truth) and the predicted values from the model.
- The goal is to minimize the cost function by adjusting model parameters to improve prediction accuracy.
- Cost functions guide the learning process during training.
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
- It is widely used for both **binary** and **multi-class classification** problems.

## Stochastic Gradient Descent Algorithm
- SGD is a variant of gradient descent optimized for large datasets.
- Instead of calculating the gradient using the entire dataset, SGD uses a small random subset (batch) of data points.
- This makes training faster and more memory-efficient compared to standard gradient descent.
- SGD is used for training deep neural networks (CNNs and RNNs) and GenAI models (VAEs and GANs)
- VAN: Variational Autoencoders | GAN: Generative Adversarial Networks.
