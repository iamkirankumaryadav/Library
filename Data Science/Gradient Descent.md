<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# **Gradient Descent**
- **Gradient Descent** is an optimization algorithm used while training a model, starting from defining some initial parameter values. 
- Iteratively it adjusts the values of the parameters to minimize the given **cost function**.
- **Gradient (m)** measures how much the output of a function changes after a unit change in input.
- **Gradient (m)** tells us in which direction to move to minimize the cost function quickly.
- The higher the gradient, the steeper the slope and the faster a model can learn, once the slope is 0, the model stops learning. 

### **Learning Rate**
- Determines the step size taken into the direction of the local minimum point.
- It represents how fast or slow the model will move towards the local minimum point.
- Learning rate should be set to an appropriate value, neither too low nor too high. 
- If the steps are too big, they will overshoot or bounce back and forth within the convex function.
- If the steps are minimal, gradient descent will take time to reach the local minimum point.
- Flow can be tracked by plotting the # iterations on the x-axis and the value of the cost function on the y-axis.
- This helps to track the value of the **cost function** after each iteration of gradient descent.
- It provides a way to easily spot how appropriate your learning rate is performing.
- If gradient descent works properly, the cost function should decrease after every iteration.
- Once the cost function stops decreasing anymore and remains on the same level, it has converged (reached the local minimum point).
