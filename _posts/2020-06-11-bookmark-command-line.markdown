---
date: 2020-06-11T19:14:44.000Z
layout: post
title: Features every Python Programmer must know
subtitle: A curated list features every Python programmer must know.
description: A curated list features every Python programmer must know.
image: /assets/images/post_images/python-features-programmer-must-know.webp
optimized_image: /assets/images/post_images/python-features-programmer-must-know.webp
category: Python
tags:
  - Python
  - Cheatsheet
author: sarthakgarg
paginate: true
---
### UNDERSCORES AND DUNDERS 

'dunders' means double underscores

• Single Leading Underscore: **_var**

Use a single underscore  (prefix) before variable name to indicate that the variable is meant for internal use. It is generally not enforced by the Python interpreter and is only meant as a hint to the programmer.

• Single Trailing Underscore: **var_**

Append Single trailing underscore (postfix) after variable or function name to avoid naming conflicts with Python keywords.

• Double Leading Underscore: **__var**

A double underscore prefix causes the Python interpreter to rewrite the attribute name in order to avoid naming conflicts in subclasses.

This is also called name mangling—the interpreter changes the name of the variable in a way that makes it harder to create collisions when the class is extended. It changes it to: _ClassName__VariableName

• Double Leading and Trailing Underscore: **\_\_var\_\_**

Names that have both leading and trailing double underscores are reserved for special use in the language, and are left unscathed by Python interpreter.

• Single Underscore: **_**

Use a single stand-alone underscore as a name to indicate that a variable is temporary or insignificant. Example:.

```
for _ in range(5):
  do_something
```