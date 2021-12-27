---
layout: post
title:      "Single Line Conditional Python"
date:       2021-12-27 03:32:38 +0000
permalink:  single_line_conditional_python
---


Ever wanted to make your code be even briefer, and pershaps even easier to read? One of the ways to do that in the Python programming language is to be make use of the single line conditional statement for an if/else block. First, lets take a look at what an if/else block looks like in Python when not written as a single line.

```
if num == 0:
     print("Number is zero!")
else:
     print("Number is not zero!")
```

While not particularly difficult to read, it can be collapse down even further to:

```
print("Number is zero!") if num == 0 else "Number is not zero!")
```

To help remember, it's

```
<conditional-true> if conditional else <conditional-false>
```
