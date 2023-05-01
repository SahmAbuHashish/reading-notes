# Reading Questions

## What is the purpose of dunder methods in Python? Provide an example of a commonly used dunder method.

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __ init __ or __ str __.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:
>>>class LenSupport:
>>> def __len__(self):
>>>return 42
>>>
>>> obj = LenSupport()
>>> len(obj)
>>>42

---

## In the video “AI Guru makes $238,800 with misleading paid course,” what was the main ethical issue raised concerning the use of developers’ work, and how might this have been avoided?

taking and using another developer's code and not crediting the developers in a proper way

---

## Describe the Python statistics module and give an example of a function within the module that can be used to perform a common statistical operation.

The statistics module in Python provides a set of functions for calculating basic statistical properties of numeric data. The module includes functions for calculating measures of central tendency, measures of dispersion (e.g., variance, standard deviation), and other summary statistics.

- import statistics
- data = [1, 2, 3, 4, 5]
- mean = statistics.mean(data)
- print(mean)  # 3.0
