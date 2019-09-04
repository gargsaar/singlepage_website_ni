---
layout: post
title:  "Efficient Vs Elegant Coding"
date:   2019-07-08
header-style: text
lang: en
tags:
  - Coding
  - Technology
---
The dilemma of efficiency versus elegance is an interesting one. It is always difficult to decide between an elegant and short solution, and a more convoluted but faster solution. For example, I can write code to calculate exponent of a number in two ways:

Efficient but non elegant solution:

```
function power(base, exponent) { var base_loc = base;
if (exponent == 0) return 1;
else { for (var count=1; count &lt; exponent; count ++) {base_loc = base_loc * base; } return base_loc;} }
```

This is a basic approach of using loops, and to me it looks old. Loops are said to affect the control flow of a program. They change the order in which statements are executed.

Elegant solution but not efficient:

```
function power(base, exponent) {
if (exponent == 0) return 1;
else return base * power(base, exponent - 1);}
```

This is rather close to the way mathematicians define exponentiation, and to me it looks elegant and a lot nicer than the earlier version. It sort of loops, but there is no While, For, or even a local side effect to be seen. By calling itself, the function produces the same effect but in most browsers this piece of code will run slowly.

So what to choose between the two?

The basic rule, which has been repeated by many programmers and with which I agree to a greater degree, is to not worry about efficiency until your program is probably too slow. When it is, find out which parts are too slow, and start exchanging elegance for efficiency in those parts.

Of course, the above rule doesn't mean one should start ignoring performance altogether. The reason I am making a big deal out of this is that surprisingly many programmers focus fanatically on efficiency, even in the smallest details. The result is bigger, more complicated, and often less correct programs, which take longer to write than their more straightforward equivalents and often run only marginally faster. 

*The bottom line is - always remember the basic rule before actually making your code more efficient. Enjoy coding!*
