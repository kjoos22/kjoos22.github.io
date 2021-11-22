---
layout: post
title:      "Length of an Object in Python"
date:       2021-11-22 00:46:41 +0000
permalink:  length_of_an_object_in_python
---


Need to find the length of an object in Python? Meet your new friend, the `len()` function. The official Python [documentation's](https://docs.python.org/3/library/functions.html?highlight=len#len) definition of `len()` is: 

*Return the length (the number of items) of an object. The argument may be a sequence (such as a string, bytes, tuple, list, or range) or a collection (such as a dictionary, set, or frozen set).*

As noted by the documentation, `len()` can be used on multiple different object types. The first thing that comes to most people's minds when talking about length, is the length of a string. For example:

`>>> phrase = "Hello there, General Kenobi"`

`>>> len(phrase)`

`27`

However `len()` can also be used on other objects, such as lists:

`>>> colors = ["Red", "Blue", "Green"]`

`>>> len(colors)`

`3`

or tuples:

`>>> cars = ("Mustang", "Corvette")`

`>>> len(cars)`

`2`

or range objects:

`>>> numbers = range(1, 30, 2)`

`>>> len(numbers)`

`15`

As seen, the `len()` function is a powerful tool in Python. However, there are some objects that will cause a TypeError, as their object type "has no len()". These include integers, booleans, floats, and complex numbers. That's all there is for the `len()` function, a simple tool, that has multiple applications that can be used in your Python code. 
