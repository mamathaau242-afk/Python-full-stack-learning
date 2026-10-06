# Day 11

## Key Learnings

## NumPy Array Shape

### Shape of an Array
The shape of an array is the number of elements in each dimension.

### Get the Shape of an Array
NumPy arrays have an attribute called shape that returns a tuple with each index having the number of corresponding elements.

Example:
Print the shape of a 2-D array:
```python
import numpy as np
arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])
print(arr.shape)
```
The example above returns (2, 4), which means that the array has 2 dimensions, where the first dimension has 2 elements and the second has 4.

## NumPy Array Reshaping

### Reshaping arrays
Reshaping means changing the shape of an array.
The shape of an array is the number of elements in each dimension.
By reshaping we can add or remove dimensions or change number of elements in each dimension.

### Reshape From 1-D to 2-D
Example:
Convert the following 1-D array with 12 elements into a 2-D array.
The outermost dimension will have 4 arrays, each with 3 elements:
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])
newarr = arr.reshape(4, 3)
print(newarr)
```
### Reshape From 1-D to 3-D
Example
Convert the following 1-D array with 12 elements into a 3-D array.
The outermost dimension will have 2 arrays that contains 3 arrays, each with 2 elements:
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])
newarr = arr.reshape(2, 3, 2)
print(newarr)
```
### Flattening the arrays
Flattening array means converting a multidimensional array into a 1D array.
We can use reshape(-1) to do this.

Example:
Convert the array into a 1D array:
```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
newarr = arr.reshape(-1)
print(newarr)
```
## Codes
### 1
```python
#range
import numpy as np
arr = np.arange(1,5)
print(arr)

arr = np.arange(0,5)
print(arr)
```
### 2
```python
#operations
import numpy as np
arr = np.sum([1,2,3])
print(arr)

arr = np.sum([[1,2,3],[4,5,6]])
print(arr)

arr = np.mean([1,2,3])
print(arr)

arr = np.median([1,2,3,4])
print(arr)

arr = np.min([1,2,3])
print(arr)

arr = np.max([1,2,3])
print(arr)
```
