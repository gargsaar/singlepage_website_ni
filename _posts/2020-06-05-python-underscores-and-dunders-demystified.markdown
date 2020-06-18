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
Python has so many awesome, but unknown features that even knowing a few of them can put you in the league of advanced programmers. One of them is **Underscores** and **Dunders**.

In this post, I’ll discuss all the five underscore patterns available in Python, and how they affect the behavior of Python programs.

Single and double underscores have a meaning in Python variable and method names. Some of that meaning is merely by convention and intended as a hint to the programmer—and some of it is enforced by the Python interpreter.

1. ### Single Leading Underscore:**_var**

Python doesn't have a strong distinction between "private" and "public" variables like Java does. So, to indicate that a variable is meant for internal use, a single leading underscore (prefix) is used before the variable name.

```
Class Pub:
  def __init__(self):
    self.name = 'Bond, James'
    self._age = 32 #private variable, shhh...don't ask
```

If a leading underscore is used in the variable name, it is generally not enforced by the Python interpreter and is only meant as a hint to the programmer. 

It is like conveying to other programmers - *"Hey, this is not meant to be used outside the interface of this class. Better leave it alone!"*

Leading underscore can be used for defining a private function or a method. 

```
# pub_shubs.py

  def _menu_tonight(): #private function
    'something special'
```

A private function in module if imported as a wildcart will not be accessible. Don't worry, regular import still works. 

```
from pub_shubs import * #wildcard import
_menu_tonight() #NameError: "name '_internal_func' is not defined"

import pub_shubs
pub_shubs._menu_tonight() #No Error
```

2. ### Single Trailing Underscore:**var_**

Append Single trailing underscore (postfix) after variable or function name to avoid naming conflicts with Python keywords.

```
Class class: #SyntaxError: "invalid syntax"

Class class_ #No Error
```

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