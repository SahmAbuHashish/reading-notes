# Reading Questions

### What are the key principles of Test-Driven Development (TDD) in Python, and how do they contribute to the overall quality of code?

- Write a unit test and make it fail. 
- Write the feature and make the test pass!. 
- Refactor the code.

The greatest advantage about TDD is to craft the software design first
Your code will be more reliable.

### Explain the purpose of the if __name__ == '__main__': statement in Python scripts. What are some use cases for including this conditional in your code?

Every Python module has it’s __name__ defined and if this is ‘__main__’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.
If you import this script as a module in another script, the __name__ is set to the name of the script/module.
Python files can act as either reusable modules, or as standalone programs.
if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.


### Describe the concept of recursion in Python.

The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called a recursive function. Using a recursive algorithm, certain problems can be solved quite easily. A recursive function solves a particular problem by calling a copy of itself and solving smaller subproblems of the original problems. Many more recursive calls can be generated as and when required. It is essential to know that we should provide a certain case in order to terminate this recursion process. So we can say that every time the function calls itself with a simpler version of the original problem.

### What is the difference between Python modules and packages? Explain how to create, import, and use them in your Python programs.

### modules:

- A module can be written in Python itself.
- A module can be written in C and loaded dynamically at run-time, like - the re (regular expression) module.
- A built-in module is intrinsically contained in the interpreter, like the itertools module.
- A module’s contents are accessed the same way in all three cases: with the import statement. "import <module_name>"

### packages:
Suppose you have developed a very large application that includes many modules. As the number of modules grows, it becomes difficult to keep track of them all if they are dumped into one location. This is particularly so if they have similar names or functionality. You might wish for a means of grouping and organizing them.

Packages allow for a hierarchical structuring of the module namespace using dot notation. In the same way that modules help avoid collisions between global variable names, packages help avoid collisions between module names.

Creating a package is quite straightforward, since it makes use of the operating system’s inherent hierarchical file structure.



### Things I want to know more about