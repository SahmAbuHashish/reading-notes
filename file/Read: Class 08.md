# Reading Questions


## What is the basic syntax of Python list comprehension, and how does it differ from using a for loop to create a list? Provide an example of a list comprehension that squares the elements in a given list of integers.

List comprehension methods are an elegant way to create and manage lists. 
In Python, list comprehensions are a more compact way of creating lists. 
More flexible than for loops, list comprehension is usually faster than other methods.

 create a list using list comprehension
  squares = [x**2 for x in range(10)]

  print(squares)

---


## What is a decorator in Python?

A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure

---


## Explain the concept of decorators in Python. How do they work, and what are some common use cases for them? Provide an example of a simple decorator function from the reading.

A Python decorator is a function that takes in a function and returns it by adding some functionality.

def plus_one(number):
    def add_one(number):
        return number + 1


    result = add_one(number)
    return result
plus_one(4)

output // 5
