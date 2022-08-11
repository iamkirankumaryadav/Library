<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# NumPy
- **Numerical** Python 
- `Linear Algebra`, `Arithmetic`, `Statistical` and `Mathematical` operations.
- Searching, Sorting, Counting, and Stacking.
- `Element wise` arithmetic operations | `Scientific` and `Financial` calculations.
- `Array` processing | `N` **dimensional** array | Fast `Vector` and `Matrix` operations.
- **Statistical** and **algebraic** computations | `Broadcasting` ( Arithmetic operations between array of different shape and size ) 
- Most advanced `built in` functions. 
- Essential for `OpenCV` Computer Vision applications.
- Statsmodel, Matplotlib, Scikit Learn, Scipy and Pandas also use most of the NumPy's functions.
- Rich set of Attributes: `shape`, `size`, `ndim`
- Rich set of functions: `array()`, `arange()`, `unique()`, `repeat()`, `random.randint()`, `argmax()`, `reshape()`, `count_nonzero()`, `zeros()`, `ones()`, `ravel()`, `hsplit()`, `vsplit()`, `hstack()`, `vstack()` [...](https://towardsdatascience.com/21-numpy-functions-that-will-boost-your-data-analysis-process-1671fb35215)

### [Python List vs NumPy Array](https://github.com/KIRANKUMAR7296/NumPy)

<table align="center">
  <tr>
    <th colspan="4"><h3>Dimensions ( Array )</h3></th>       
  <tr>
  <tr>
    <td colspan="4"><img src="Image/Dim.png" alt="Dimensions"></td>
  </tr>
  <tr>
    <td>0 Dimension</td>
    <td>1 Dimension</td>
    <td>2 Dimensions</td>
    <td>3 Dimensions</td>
  </tr>  
  <tr>
    <td>Point</td>
    <td>Line</td>
    <td>Square</td>
    <td>Cube</td>
  </tr>  
   <tr>
    <td>Scalar</td>
    <td>Vector ( Row or Column )</td>
    <td>Matrix ( Table or Data Frame )</td>
    <td>Tensor</td>
  </tr>  
  <tr>
    <td>Rank 0 Tensor</td>
    <td>Rank 1 Tensor</td>
    <td>Rank 2 Tensor</td>
    <td>Rank 3 Tensor</td>
  </tr>    
</table>

Operator |	Description
:--- | :---
`np.array([1, 2, 3])` |	`1D` Array
`np.array([(1, 2, 3), (4, 5, 6)])` | `2D` Array
`np.arange(start, stop, step)` | `Range` Array

### Placeholders 

Operator | Description
:--- | :---
`np.linspace(0,2,9)` |	Add evenly spaced values between interval to array of length.
`np.zeros((1,2))`	| Create an array filled with `zeros`
`np.ones((1,2))` |	Creates an array filled with `ones`
`np.random.random((5,5))` |	Creates an array with `random` numbers.
`np.empty((2,2))` |	Creates an `empty` array.

`Python List` | `NumPy Array`
:--- | :---
No support for vectorized operations | Supports vectorized operations ( Addition, Multiplication )
No fixed data type ( List is `Heterogeneous` ) | Fixed data type ( `Homogeneous` )
For loop not efficient ( Check data type ) | For loop is efficient 
Consumes more memory | Consume `less` memory ( `6x` less memory than `List` )
Slower as compared to `NumPy` array | `100x` faster than `List`
`List` stores object type, reference count, object value, object size | `NumPy` only stores element values

Python List ( Ordered, Subscriptable, Mutable, Heterogeneous, Duplicate, Indexing, Slicing, Iterable )
```python
List = [1, 2, 3]
```

NumPy Array
```python
import numpy as np

Array = np.array([1, 2, 3])
```
<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
