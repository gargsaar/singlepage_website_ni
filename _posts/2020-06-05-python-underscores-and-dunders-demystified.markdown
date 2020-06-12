---
date: 2020-06-05T08:18:58.000Z
layout: post
title: Python Underscores and Dunders Demystified
subtitle: Underscores and Dunders every Python programmer must know.
description: Underscores and Dunders every Python programmer must know.
image: /assets/images/post_images/python-features-programmer-must-know.webp
optimized_image: /assets/images/post_images/python-features-programmer-must-know.webp
category: Python
tags:
  - Coding
  - Tools
author: sarthakgarg
paginate: true
---
Python has so many hidden gems that even knowing a few of them can put you in the league of advanced programmers. And one of them is **Underscores and Dunders**.

In this post, I’ll discuss all the five underscore patterns available in Python, and how they affect the behavior of Python programs.

Single and double underscores have a meaning in Python variable and method names. Some of that meaning is merely by convention and intended as a hint to the programmer—and some of it is enforced by the Python interpreter.

1. ### Single Leading Underscore:**_var**

Python doesn't have a strong distinction between "private" and "public" variables like Java does. 

A single underscore (prefix) before variable name can be used to indicate that the variable is meant for internal use. 

```
Class Pub:
  def __init__(self):
    self.name = 'John Doe'
    self._age = 16
```

If a leading underscore is used in the variable name, it is generally not enforced by the Python interpreter and is only meant as a hint to the programmer. 

It is like conveying to other programmers - *"Hey, this is not meant to be used outside the interface of this class. Better leave it alone!"*

2. ### Single Trailing Underscore:**var_**

Append Single trailing underscore (postfix) after variable or function name to avoid naming conflicts with Python keywords.

3. ### Leading Dunders:**__var**

**'dunders' means double underscores**

A double underscore prefix causes the Python interpreter to rewrite the attribute name in order to avoid naming conflicts in subclasses.

This is also called name mangling—the interpreter changes the name of the variable in a way that makes it harder to create collisions when the class is extended. It changes it to: _ClassName__VariableName

4. ### Leading and Trailing Dunders:**\_\_var\_\_**

Names that have both leading and trailing double underscores are reserved for special use in the language, and are left unscathed by Python interpreter.

5. ### Single Underscore:**_**

Use a single stand-alone underscore as a name to indicate that a variable is temporary or insignificant. Example:.

```
for _ in range(5):
  do_something
```