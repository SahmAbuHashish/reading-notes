# Reading Questions

## Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.


The concept of scope rules how variables and names are looked up in your code. It determines the visibility of a variable within the code.
The Python scope concept is generally presented using a rule known as the LEGB rule.stand for Local, Enclosing, Global, and Built-in scopes 

Several programming languages take advantage of scope for avoiding name collisions and unpredictable behaviors. Most commonly, you’ll distinguish two general scopes:

- Global scope: The names that you define in this scope are available to all your code.
x = value


- Local scope: The names that you define in this scope are only available or visible to the code within the scope.

def my_func():
   x = value


---

## How do the global and nonlocal keywords work in Python, and in what situations might you use them?
- The statement consists of the global keyword followed by one or more names separated by commas.
>>> counter = 0  # A global name
>>> def update_counter():
...     global counter  # Declare counter as global
...     counter = counter + 1  # Successfully update the counter

- With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.
>>> def func():
...     var = 100  # A nonlocal variable
...     def nested():
...         nonlocal var  # Declare var as nonlocal
...         var += 100
...
...     nested()
...     print(var)
...
>>> func()

---

## In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.

Big O Notation is a fundamental tool used to find out the time complexity of algorithms.Big O Notation allows programmers to classify algorithms depending on how their run time or space requirements vary as the input size varies.

---

## Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.

To simulate a dice roll using Python, you could use the random module. Specifically, you can use the randint(a, b) method, which returns a random integer between a and b inclusive. For a standard six-sided dice, we would set a to 1 and b to 6:

To calculate the probability of rolling a specific number, such as 6, over a large number of trials, we can simulate many dice rolls and count the number of times the desired number is rolled. We can then divide the number of times that the desired number was rolled by the total number of rolls to get the probability.
