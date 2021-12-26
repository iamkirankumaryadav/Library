<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# `Gradient Descent`

- An `optimization` algorithm used while training a model.
- Gradient descent starts from defining some initial parameter's values. 
- Gradient descent iteratively `adjust` the parameters values to `minimize` the given cost function ( loss | error )
- A `gradient` ( `m` ) measures how much the output of a function changes after little change in inputs.
- A `gradient` simply measures the change in weights ( `slope` ) with regard to the change in error.
- Higher the gradient, steeper the slope and faster a model can learn, once the slope is `0`, model stops learning. 

### `Learning Rate`

- `Size` of steps taken into the direction of the local minimum are determined by the `learning rate`
- It represents how `fast` or `slow` we will move towards the `global minimum`
- Learning rate should be set to an appropriate value, neither too low nor too high. 
- If the steps are too big, it will `overshoot` or `bounce` back and forth between convex function.
- If the steps are very small, gradient descent will take time to reach the local minimum.
- Flow can be tracked by plotting the `# iterations` on the x axis and the value of the cost function on the y axis.
- This helps you see the value of your cost function after each iteration of gradient descent.
- It provides a way to easily spot how appropriate your learning rate is performing.
- If gradient descent is working properly, the cost function should decrease after every iteration.
- Once the cost-function stops decreasing anymore and remains on the same level, it has converged.
