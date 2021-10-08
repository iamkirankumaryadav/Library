# Gradient Descent

- Gradient descent is an `optimization` algorithm that's used when training a model.
- Tweaks its `parameters` iteratively to minimize a given function to its local minimum.
- Start by defining the initial parameter's values. 
- Gradient descent uses calculus to iteratively adjust the values so they `minimize` the given cost-function ( `loss` )
- Cost function is loss ( Actual - Prediction )
- A gradient measures how much the output of a function changes if you change the inputs a little bit.
- A gradient simply measures the change in all weights ( slope ) with regard to the change in error.
- The higher the gradient, the steeper the slope and the faster a model can learn.
- But if the slope is `0`, the model stops learning. 

### Importance of Learning Rate

- The size of steps taken into the direction of the local minimum are determined by the learning rate.
- It represents how `fast` or `slow` we will move towards the optimal weights.
- For gradient descent to reach the local minimum we must set the learning rate to an appropriate value.
- Neither too low nor too high. 
- If the steps it takes are too big, it will overshoot or bounce back and forth between convex.
- If the steps are very small, gradient descent will eventually reach the local minimum but that may take time.
- We can check the flow of gradient descent by plotting the number of iterations on the x axis and the value of the cost function on the y axis.
- This helps you see the value of your cost function after each iteration of gradient descent.
- It provides a way to easily spot how appropriate your learning rate is performing.
- If gradient descent is working properly, the cost function should decrease after every iteration.
- When gradient descent can’t decrease the cost-function anymore and remains more or less on the same level, it has converged.
