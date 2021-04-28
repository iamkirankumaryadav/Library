<h4 align=right><a href="https://github.com/KIRANKUMAR7296/Library/blob/main/AI/AI.md">Back to AI</a></h4>

# Convolutional Neural Network ( CNN )

- A **Deep Learning Algorithm** which takes **Image** as Input, **Extract Information** and **Learn** from **Image** ( Weights and Biases )
- CNN is used with **Computer Vision** designed to process **Pixel Data**.
- **Face Recognition** | **Image Classification** : Breeds of Dogs | Cat or Dog | **Video Recognition** : Recognize Object or Person in a Video.

![Channels](Image/3Channels.png)

### Why should we Use CNN ?
- Suppose we are working with **MNIST** Dataset, Each Image is 28 x 28 x 1 Channel ( 0 or 1 ), This Size is Manageable.
- What if Image Size is 1000 x 1000 which means 10<sup>6</sup> Neurons in **Input Layer**. 
- Simply **CNN** Extract the Feature of Image and Convert into Lower Dimension without loosing Characteristics.

e.g.
- Initial Size of Image is 224 x 224 x 3 ( If you Proceed without Convolution : **1,00,352** number of Neurons in Input Layer )
- But by using CNN : Input Tensor Dimension is reduced to 1 x 1 x 1000 ( i.e. You need only **1000** Neurons in First Layer )

### Few Definitions you should know before Understanding CNN

### A. Image Representation
- We Understand Image by its **Height** and **Width** ( 2D Matrix ) but due to **Color**, we use **Tensors** ( 3 Dimensions )
- Images are encoded in **Color Channels**, Image Data is represented into each **Color Intensity**.
- Information contained into a Image is the Intensity of each Channel Color. 

### B. Edge Detection
- Image has Vertical and Horizontal Edges which combines to form an Image.
- Convolution Operation is used with some Filters for Detecting Edges.
- e.g. Image Dimension is 6 x 6 and Filter choice is 3 x 3 we get 4 x 4 Image.

### C. Stride and Padding ( Hyperparameters )
- **Steps** we move in Convolution ( By Default is One ) Slide over Matrix by **Stride** Length = `1`.
- **Size** of **Output** is **Smaller** than **Input**, to Maintain the **Dimension** of **Output** as an **Input**, we use **Padding**.
- **Padding** : Adding `Zeros` to **Input** `Matrix` **Symmetrically** from all the **Sides**.

<table align=center>
  <tr><th>Stride</th><th>Padding</th></tr>
  <tr><td><img src="Image/Stride.gif" width='400px' height='400px'></td><td><img src="Image/Padding.gif" width='400px' height='400px'></td></tr>
</table>

### CNN Architecture ( Stack of Distinct Layer )

![CNN Layer](Image/CNNLayers.png)

### 1. Input Layer : Image Data ( 3D Matrix )
- **Input** is a `3` Dimensional **Matrix** ( Height x Width x Channels )
- **Kernels** we call it **Filters** it is also a `3` Dimensional **Matrix** ( **h** x **w** x **channels** )
 
### 2. Convolution Layer ( Feature Extraction ) + Activation Function ( ReLu )
- **Feature** of `Image` is Extracted in this Layer. 
- Slide **Filter** | **Kernel** over the Image by a **Stride = 1** until we go through the Whole Image.
- Uses `ReLu` **Activation Function** to make all **Negative Value** to `Zero`.

### 3. Pooling Layer ( Dimensionality Reduction | Flattens )
- `Pooling` : **Down Samples** the **Spatial Volume** of Input `Image` | **Flattens Input** for Next **Convolution** Layer.  
- e.g ( Input = ( 1, 10, 64 ) to Output = ( 640 ) i.e 1 x 10 x 64 = 640 )
- Decreases **Computation Power** to Process Data. 
- `Max` Pooling : Returns **Maximum** Value from the portion of the **Image**.
- `Average` Pooling : Returns **Average** Value from the portion of the **Image**.

![Max Pool](Image/MaxPool.png)

### 4. Fully Connected Layer ( Feed Forward Connected Layers ) + Activation Function ( ReLu )
- The Input to the **Fully Connected Layer** is the output from the **Final Pooling** or **Convolutional Layer**. 
- Input is **Flattened** and then fed into the **Fully Connected Layer**.
- Takes **Weighted Sum** of all the **Inputs** from Previous Layer and Generates **Output** for **Last Layer**. 
- **Connects** Neurons in One Layer to Neurons in Last Layer and **Classify** Images between Different Category.

### Activation Function : Softmax | Logistic + Dropout
- `ReLu` : **Negative Value** to `Zero`
- `Logistic` : **Binary** Classification `0` or `1` 
- `Softmax`  : **Multiclass** Classification ( Converts Numbers into Probabilities and the Vector Sum Ups to 1 )
- When all the **Features** are Connected in a **Fully Connected Layer** it can cause **Overfitting**.
- `Dropout` : Few Neurons are **Dropped** Randomly from the **Neural Network** to Prevent from **Overfitting**.

### 6. Output Layer
- `Label` of the `Image` is in form of **One Hot Encoded** ( `One Hot Vector` )
- `Label` is assigned with each `Image` ( What the Driver is Actually doing in the Vehicle ? )

### Example

- [Distracted Driver Classification](https://github.com/KIRANKUMAR7296/Distracted-Driver-Classification)

[CNN](https://towardsdatascience.com/covolutional-neural-network-cb0883dd6529)
