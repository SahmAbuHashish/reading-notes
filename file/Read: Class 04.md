# Reading Questions

## What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?

- Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.

ex: Take the example of a dog as an object.
There are different varieties of dogs that means different varieties of objects according to the dog class. For example, one dog has black color, another dog may have grey color, or white, etc.
However, we can notice that most of the behaviours are the same like barking, wagging their tail, eating, sleeping, etc.

- A class can be understood as a template or a blueprint, which contains some values, known as data members, and some set of rules, known as behaviors or methods. The data and methods that are defined in the class are automatically taken when an object is created. The class is a template or blueprint for objects. One can make as many objects as they want to be based on a class.

ex: For example, the template for the car is created first after that multiple units or objects of cars can be created based on the template. And each of the objects must have the data and methods mentioned in the blueprint.

---

## Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?

The process of solving large problems by breaking them down intosmaller, more simple problems that have identical forms.

- Identify the base case
- Define the recursive case
- Call the function recursively, Call the function itself with the smaller subproblem as input, until the base case is reached.


---

## What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project.

Fixtures define the steps and data that constitute the arrange phase of a test ,In pytest, they are functions you define that serve this purpose. They can also be used to define a test’s act phase; this is a powerful technique for designing more complex tests.

- fixtures have explicit names and are activated by declaring their use from test functions, modules, classes or whole projects.

- fixtures are implemented in a modular manner, as each fixture name triggers a fixture function which can itself use other fixtures.

- fixture management scales from simple unit to complex functional testing, allowing to parametrize fixtures and tests according to configuration and component options, or to re-use fixtures across function, class, module or whole test session scopes.

- teardown logic can be easily, and safely managed, no matter how many fixtures are used, without the need to carefully handle errors by hand or micromanage the order that cleanup steps are added.

---



## Things I want to know more about

