---
title: everything in python is an object
date: 2022-09-15
---

A popular concept in programming languages is the concept of primitive and non-primitive data types and these data types are represented in different ways
across different programming languages. In languages like C for example, a primitive data type such as an integer is represented directly in the language
implementation i.e if you assign a variable `a` to an integer value `2` in C, `a` would refer to an address in memory that stores the actual value `2`. 
This is one of the reasons why variables in C have to be explicitly declared as a specific type so that a memory location is properly allocated for storing the variable's value.

Meanwhile, python is a dynamically typed language, you can assign variable names directly and even change the type of the variable anywhere in a program and without any constratints.
Why is this possible? This is possible because while the variables in c holds the real values, python variables only refer to objects. 
So what do we mean when we make a statement like `a = 2` in python? This means that the variable `a` holds a reference to an object that represents the value `2`.
Now what object? An Integer object.

In python's [data model](https://docs.python.org/3/reference/datamodel.html) python uses objects as an abstraction for it's data hence it has classes with methods
defined for each data type. The integer datatype implements an abstract base class called Integral and you can see the source code 
[here](https://github.com/python/cpython/blob/3.10/Lib/numbers.py).

You can call methods defined in the integer class on variables assigned to the integer as seen in the code snippet below.

```
>>> a = 2
>>> a.__xor__(2) # same as doing the bitwise operation a ^ 2
0
>> a.__float__() # same as doing float(a)
2.0
```

And just like that everything in python is an object, think about just anything, lists, dictionaries, functions, and even classes.
