# Day 8

## Key Learnings

### Python File Open
File handling is an important part of any web application.
Python has several functions for creating, reading, updating, and deleting files.

### File Handling
The key function for working with files in Python is the open() function.
The open() function takes two parameters; filename, and mode.
There are four different methods (modes) for opening a file:
- "r" - Read - Default value. Opens a file for reading, error if the file does not exist
- "a" - Append - Opens a file for appending, creates the file if it does not exist
- "w" - Write - Opens a file for writing, creates the file if it does not exist
- "x" - Create - Creates the specified file, returns an error if the file exists

### Open a File on the Server
Assume we have the following file, located in the same folder as Python:

### demofile.txt
```python
Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!
To open the file, use the built-in open() function.
```
The open() function returns a file object, which has a read() method for reading the content of the file:
```python
f = open("demofile.txt")
print(f.read())
```
### What is NumPy?
NumPy is a Python library used for working with arrays.
It also has functions for working in domain of linear algebra, fourier transform, and matrices.
NumPy was created in 2005 by Travis Oliphant. It is an open source project and you can use it freely.
NumPy stands for Numerical Python.

### Example
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

## NumPy Creating Arrays

### Create a NumPy ndarray Object
NumPy is used to work with arrays. The array object in NumPy is called ndarray.
We can create a NumPy ndarray object by using the array() function.
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
print(type(arr))
```
### Dimensions in Arrays
### 0-D Arrays
0-D arrays, or Scalars, are the elements in an array. Each value in an array is a 0-D array.
```python
import numpy as np
arr = np.array(42)
print(arr)
```

### 1-D Arrays
An array that has 0-D arrays as its elements is called uni-dimensional or 1-D array.
These are the most common and basic arrays.

Example
Create a 1-D array containing the values 1,2,3,4,5:
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
print(arr)
```
 ### 2-D Arrays
An array that has 1-D arrays as its elements is called a 2-D array.
These are often used to represent matrix or 2nd order tensors.
NumPy has a whole sub module dedicated towards matrix operations called numpy.mat
```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr)
```
### 3-D arrays
An array that has 2-D arrays (matrices) as its elements is called 3-D array.
These are often used to represent a 3rd order tensor.
```python
import numpy as np
arr = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])
print(arr)
```
### Example
Check how many dimensions the arrays have:
```python
import numpy as np
a = np.array(42)
b = np.array([1, 2, 3, 4, 5])
c = np.array([[1, 2, 3], [4, 5, 6]])
```
### Higher Dimensional Arrays
An array can have any number of dimensions.
When the array is created, you can define the number of dimensions by using the ndmin argument.

### Example
Create an array with 5 dimensions and verify that it has 5 dimensions:
```python
import numpy as np
arr = np.array([1, 2, 3, 4], ndmin=5)
d = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])
print(a.ndim)
print(b.ndim)
print(arr)
print('number of dimensions :', arr.ndim)
```

print(c.ndim)
print(d.ndim)
```
