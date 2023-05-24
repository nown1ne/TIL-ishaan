# NumPy:
Its a multidimensional array library which contains fixed type elements, its used over lists as
  - List  -> Very Slow
  - NumPy -> Very Fast
    - Uses Less Memory and 
    - No type checking when interating through objects
    - Contiguous Memory
      - SIMD(Single Instruction and Multiple Data Stream) Vector Processing
      - Effetive Cache Utilisation 

### [NumPy Notebook](https://www.kaggle.com/code/orhansertkaya/numpy-tutorial-for-beginners#Computation-on-NumPy-Arrays:-Universal-Functions)
## Load in NumPy:
```python
import numpy as np
```

## Basics:
### Declaring the array:
```python
import numpy as np
a = np.array([1, 2, 3], dtype('int16'))   # Specify the data type     
print(a)                                  # [1 2 3]
```

### Get Dimension:
```python
a = np.array([1,2,3])
b = np.array([[9.0,8.0,7.0],[6.0,5.0,4.0]])
a.ndim                                        # 1
b.ndim                                        # 2
```

### Get Shape (m x n):
```python
a = np.array([1,2,3])
b = np.array([[9.0,8.0,7.0],[6.0,5.0,4.0]])
a.shape                                        # (3,)
b.shape                                        # (2, 3)
```

### Get Type:
- Gives information about the type of data present in your NumPy
```python
a = np.array([1,2,3])
b = np.array([[9.0,8.0,7.0],[6.0,5.0,4.0]])
a.dtype                                        # dtype('int32')
```

### Item Size:
- Gives information about the amount of bytes you data takes up in your NumPy
```python
a = np.array([1,2,3])
b = np.array([[9.0,8.0,7.0],[6.0,5.0,4.0]])

# Size of an element
a.itemsize                                        # 4 (4 bytes,32 bits)

# Total Size
a.itemsize * a.size                               # 12 (4 x 3(number of elements))
a.nbytes                                          # 12
```

## Accessing/Changing specific elements, rows, columns:
```python
a = np.array([[1,2,3,4,5,6,7],[8,9,10,11,12,13,14]])
print(a)

O/P
#[[ 1  2  3  4  5  6  7]
# [ 8  9 10 11 12 13 14]]

# Get a specific element [r, c]
a[1, 5]                           # 13

# Get a specific row 
a[0, :]                           # array([1, 2, 3, 4, 5, 6, 7])

# Get a specific column
a[:, 2]                           # array([ 3, 10])

# Getting a little more fancy, jumping indexes [startindex:endindex:stepsize]
a[0, 1:-1:2]                      # array([2, 4, 6])

#Changing Values
a[1,5] = 20
a[:,2] = [1,2]
print(a)

O/P
# [[ 1  2  1  4  5  6  7]
# [ 8  9  2 11 12 20 14]]

# 3-D Example:
b = np.array([[[1,2],[3,4]],[[5,6],[7,8]]])
print(b)

O/P
# [[[1 2]
#  [3 4]]
#
# [[5 6]
#  [7 8]]]
```

## Initializing Different Types of Arrays:
### All 0s matrix:
```python
np.zeros((2,3))

O/P
# array([[0., 0., 0.],
#      [0., 0., 0.]])
```

### All 1s matrix:
```python
np.ones((4,2,2), dtype='int32')

O/P
#array([[[1, 1],
#        [1, 1]],
#
#      [[1, 1],
#        [1, 1]],
#
#       [[1, 1],
#        [1, 1]],
#
#       [[1, 1],
#        [1, 1]]])
```

### Any other Number:
```python

# Making a new NumPy
np.full((2,2), 99, dtype=float32)
O/P
# array([[99., 99.],
#       [99., 99.]], dtype=float32)

# Making a New NumPy based on another NumPy
a = np.array([[1,2,3,4,5,6,7],[8,9,10,11,12,13,14]])
np.full_like(a, 4)

O/P
# array([[4, 4, 4, 4, 4, 4, 4],
#       [4, 4, 4, 4, 4, 4, 4]])
```

### Random Number:
```python
# Random decimal numbers
np.random.rand(4,2)

O/P
# array([[0.07805642, 0.53385716],
#       [0.02494273, 0.99955252],
#       [0.48588042, 0.91247437],
#       [0.27779213, 0.16597751]])

# Random Integer values
np.random.randint(-4,8, size=(3,3))

O/P
# array([[-2, -4, -4],
#       [ 6,  6,  3],
#       [ 3,  2,  2]])
```

### Identity Matrix:
```python
np.identity(5)

O/P
# array([[1., 0., 0., 0., 0.],
#       [0., 1., 0., 0., 0.],
#       [0., 0., 1., 0., 0.],
#       [0., 0., 0., 1., 0.],
#       [0., 0., 0., 0., 1.]])
```

### Repeat an Array:
```python
# Repeat an array
arr = np.array([[1,2,3]])
r1 = np.repeat(arr,3, axis=0)
print(r1)

O/P
# [[1 2 3]
# [1 2 3]
# [1 2 3]]
```

### Example:
Making a costume array
```python
output = np.ones((5,5))
print(output)

z = np.zeros((3,3))
z[1,1] = 9
print(z)

# Change values of 1->3 colums and rows of output to z
output[1:-1,1:-1] = z     ((or))      output[1:4,1:4] = z
print(output)

O/P
#[[1. 1. 1. 1. 1.]
# [1. 1. 1. 1. 1.]
# [1. 1. 1. 1. 1.]
# [1. 1. 1. 1. 1.]
# [1. 1. 1. 1. 1.]]
#[[0. 0. 0.]
# [0. 9. 0.]
# [0. 0. 0.]]
#[[1. 1. 1. 1. 1.]
# [1. 0. 0. 0. 1.]
# [1. 0. 9. 0. 1.]
# [1. 0. 0. 0. 1.]
# [1. 1. 1. 1. 1.]]
```

### Copying Arrays:
```python
a = np.array([1,2,3])
b = a
b[0] = 100

print(a)

O/P
# [100 2 3]

# To solve this issue use copy function
a = np.array([1,2,3])
b = a.copy()
b[0] = 100

print(a)

O/P
# [1 2 3]
```

## Mathematics:
```python
a = np.array([1,2,3,4])
print(a)                        # [1 2 3 4]

# Sum
a + 2                           # array([3,  4,  5,  6])

# Difference
a - 2                           # array([-1,  0,  1,  2])

# Multiplication
a * 2                           # array([2, 4, 6, 8])

# Division
a/2                             # array([0.5, 1. , 1.5, 2. ])

# Add 2 arrays
b = np.array([1,0,1,0])
a + b                           # array([2, 2, 4, 4])

# Power
a ** 2                          # array([ 1,  4,  9, 16], dtype=int32)

# Trig
np.cos(a)                       # array([ 0.54030231, -0.41614684, -0.9899925 , -0.65364362])
```
