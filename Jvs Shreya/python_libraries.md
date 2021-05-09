# Python Libraries

## 1. NumPy
### 1.1 Arrays
* importing:
```python
import numpy as np
```
* For help(on say arrays):- `np.array?`; to search:- `np.lookfor('add array')`; search by letters:- `np.co*?`
* To create array:- `x=np.array([[1,2,3],[2,3,4]])`. `x.ndim` gives dimension(here 2). `x.shape` gives no. of rows, columns(here 2,3).
* See following different functions on arrays
  ```python
  import numpy as np
  a = np.arange(10)
  b = np.arange(1, 9, 2)      # start, end (exclusive), step
  c = np.linspace(0, 1, 5, endpoint=False)
  d = np.ones((3, 3))
  e = np.zeros((2, 2))
  f = np.eye(3)               # identity
  g = np.diag(np.array([1, 2, 3, 4]))
  h = np.random.rand(4)       # uniform in [0, 1]
  i = np.random.randn(4)      # Gaussian
  np.random.seed(1234)        # Setting the random seed
  j = np.array([1+2j, 3+4j, 5+6*1j])

  print(a,'\n\n',b,b.dtype,'\n\n',c,'\n\n',d,d.dtype,'\n\n',e,'\n\n',f,'\n\n',g,'\n\n',h,'\n\n',i,'\n\n',j,j.dtype,'\n') 
  # notice datatype of b,d and and how they are printed differently. Bool and other datatypes also exist

  print(a[::-1],'\n',a[2:9:3]) #reverses, slices
  ```
  Output:
```
  [0 1 2 3 4 5 6 7 8 9] 

 [1 3 5 7] int64 

 [0.  0.2 0.4 0.6 0.8] 

 [[1. 1. 1.]
 [1. 1. 1.]
 [1. 1. 1.]] float64 

 [[0. 0.]
 [0. 0.]] 

 [[1. 0. 0.]
 [0. 1. 0.]
 [0. 0. 1.]] 

 [[1 0 0 0]
 [0 2 0 0]
 [0 0 3 0]
 [0 0 0 4]] 

 [0.19151945 0.62210877 0.43772774 0.78535858] 

 [-0.72058873  0.88716294  0.85958841 -0.6365235 ] 

 [1.+2.j 3.+4.j 5.+6.j] complex128 

[9 8 7 6 5 4 3 2 1 0] 
 [2 5 8]
```
* When we slice an array and assign it to another variable. Now when we modify the new variable, the original array also changes unless the `.copy()` is enforced while assigning. To check if they occupy same memory, use `np.may_share_memory()`.
* Arrays can be sliced using boolean expressions too:-  
  ```python
  a = np.arange(1,30,2)
  mask = (a%3==0)
  print(a,'\n',mask,'\n',a[mask],a[[4,7,2]])
  ```
  Output:
  ```
  [ 1  3  5  7  9 11 13 15 17 19] 
   [False  True False False  True False False  True False False] 
   [ 3  9 15] [ 9 15  5]
  ```
  > 10-05-2021, 02:26 AM
### 1.2 Operations
* 
