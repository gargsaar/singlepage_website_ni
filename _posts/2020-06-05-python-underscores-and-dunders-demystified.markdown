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
Class Pubber:
  def __init__(self):
    self.name = 'Bond, James'
    self._age = 33 #private variable, shhh...don't ask
```

If a leading underscore is used in the variable name, it is generally not enforced by the Python interpreter and is only meant as a hint to the programmer. 

It is like conveying to other programmers - *"Hey, this is not meant to be used outside the interface of this class. Better leave it alone!"*

Leading underscore can be used for defining a private function or a method. 

```
# pub_shubs.py

  def _menu_tonight(): #private function
    something_special
```

A private function in module if imported as a wildcart will not be accessible. Don't worry, regular import still works. 

```
from pub_shubs import * #wildcard import
_menu_tonight() #NameError: "name '_internal_func' is not defined"

import pub_shubs #regular import
pub_shubs._menu_tonight() #No Error
```

2. ### Single Trailing Underscore:**var_**

Append Single trailing underscore (postfix) after variable or function name to avoid naming conflicts with Python keywords.

```
Class class: #SyntaxError: "invalid syntax"

Class class_ #No problem
```

3. ### Leading Dunders:**__var**

**'dunders' means double underscores**

A double underscore prefix can be used in Python to avoid naming conflicts in subclasses.

```
Class Pubber:
  def __init__(self):
    self.name = 'Bond, James'
    self._age = 33
    self.__address = 'Mars'
```
Let’s take a look at the attributes on this object using the built-in dir()function:

```
>>> guest = Pubber()
>>> dir(guest)
['_Pubber__address', '__class__', '__delattr__', '__dict__','__dir__', '__doc__', '__eq__', '__format__', '__ge__','__getattribute__', '__gt__', '__hash__', '__init__','__le__', '__lt__', '__module__', '__ne__', '__new__','__reduce__', '__reduce_ex__', '__repr__','__setattr__', '__sizeof__', '__str__','__subclasshook__', '__weakref__', '_age', 'name']

```

Did you notice the very first item in the dir list - '_Pubber__address'? 

This is called name mangling. The Python interpreter changes the name of the variable in a way that makes it harder to create collisions when the class is extended. It changes it to: _ClassName__VariableName

Now let's see how this variable behaves.

```
>>> guest.name
'Bond, James'
>>> guest.__address
AttributeError:"'Pubber' object has no attribute '__address'"
```
Don'r worry you can still access it:
```
>>> guest._Pubber__address
'Mars'
```
Does name mangling also apply to method names? It sure does, try it out!

Now this is going to surprise you:
```
_Pubber__address = 'Mars' #global variable
Class Pubber:
   def address(self):
       return __address
```
```
>>> Pubber.address()
'Mars'
```
Hoohoo! _Pubber__address was declared as a global variable, but when declared inside the context of a class, I was able to reference it as it. All because of name mangling.


4. ### Leading and Trailing Dunders:**\_\_var\_\_**

Names that have both leading and trailing double underscores are reserved for special use in the language, and are left unscathed by Python interpreter.

5. ### Single Underscore:**_**

Use a single stand-alone underscore as a name to indicate that a variable is temporary or insignificant.

```
for _ in range(5):
  do_something
```
You can also use single underscores in unpacking expressions as a "don’t care” variable to ignore particular values.
```
>>> beer = ('light', 'bitter', 70, 153)
>>> color, _, _, calories = beer
```
At times, while unpacking a tuple into separate variables, you're only interested in the values for the specific fields. You can use, _.
```
>>> color
'light'
>>> calories
'153'
>>> _
70
```
Besides its use as a temporary variable, “_” is a special variable in most Python REPLs that represents the result of the last expression evaluatedby the interpreter.