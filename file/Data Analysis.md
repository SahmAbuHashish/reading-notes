# Readings: Data Analysis

## Reading Questions:


### What are the key features and benefits of Jupyter Lab, and how does it differ from Jupyter Notebook?

Jupyter notebook only offers a very simple interface using which users can open notebooks, terminals, and text files. Jupyter lab offers a very interactive interface that includes notebooks, consoles, terminals, CSV editors, markdown editors, interactive maps, and mor

---


### What are the main functionalities provided by the NumPy library, and how can it be useful in Python programming, particularly for scientific computing and data manipulation tasks?

NumPy is a basic level external library in Python used for complex mathematical operations. NumPy overcomes slower executions with the use of multi-dimensional array objects. It has built-in functions for manipulating arrays. We can convert different algorithms to can into functions for applying on arrays.

NumPy can be used to perform a wide variety of mathematical operations on arrays. It adds powerful data structures to Python that guarantee efficient calculations with arrays and matrices and it supplies an enormous library of high-level mathematical functions that operate on these arrays and matrices.

---

### Explain the basic structure and properties of NumPy arrays, and provide examples of how to create, manipulate, and perform operations on them.

NumPy (Numerical Python) is a powerful Python library that provides support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.

basic properties of NumPy arrays:

- All elements of a NumPy array must be of the same data type.
- NumPy arrays are homogenous, all elements in an array must be of the same type.
- NumPy arrays are mutable, you can modify the elements in the array after it has been created.

Creating NumPy Arrays
You can create a NumPy array using the np.array() function.

>>>import numpy as np
>>>arr1 = np.array([1, 2, 3, 4, 5])
>>>print(arr1) ---> Output: [1 2 3 4 5]

>>>arr2 = np.array([1.0, 2.5, 3.7, 4.2, 5.9])
>>>print(arr2) ----> Output: [1.  2.5 3.7 4.2 5.9]

Manipulating NumPy Arrays
NumPy provides many functions to manipulate arrays, including reshaping, transposing, and concatenating.


>>>arr1 = np.array([1, 2, 3, 4, 5, 6])
>>>print(arr1.reshape((2, 3)))
>>> Output:
>>>[[1 2 3]
>>> [4 5 6]]


>>>arr3 = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
>>>print(arr3.T)

