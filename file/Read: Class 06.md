# Reading Questions


## How can the random module be utilized in Python to generate random numbers or make selections from a list, and what are some common functions available within the module?

- The random() function in the python random module is used to generate random numbers between 0 and 1. When executed, the random() function returns a floating point number between 0 and 1.

- If you want a larger number, you can multiply it by a larger value. For example, to create a random number between 0 and 100, you can multiply the output of the random() function by 100 as shown below.

import random
random.random() * 100

- The shuffle() Function
As the name suggests, the shuffle function shuffles the elements in the list in place. The shuffle() function takes a list as an input argument. After execution, the elements of the list are shuffled in a random order as shown in the following example.

from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)

Output:
 print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
 of course your results will vary


---


## In the context of software development, what is risk analysis, and what are the key steps involved in conducting a risk analysis for a software project?

risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.
How to perform Risk Analysis?

- There are three steps:

- Searching the risk

- Analyzing the impact of each individual risk

- Measures for the risk identified

---


## What is test coverage and why is it an important (or potentially misleading) metric in software testing?

Test coverage is a useful tool for finding untested parts of a codebase. Test coverage is of little use as a numeric statement of how good your tests are.

Certainly low coverage numbers, say below half, are a sign of trouble. But high numbers don't necessarily mean much, and lead to ignorance-promoting dashboards. Sufficiency of testing is much more complicated attribute than coverage can answer. I would say you are doing enough testing if the following is true:

You rarely get bugs that escape into production, and
You are rarely hesitant to change some code for fear it will cause production bugs

---


## What is Big O notation, and how is it used to describe the performance of an algorithm? Give an example of an everyday task (not software related) that demonstrates O(n) time complexity.

big o is an equation that describes how the run time scales with respect to some input values 


if we want to describe the time to mow a square plot of land as o(a) will a be equal to the area of grass