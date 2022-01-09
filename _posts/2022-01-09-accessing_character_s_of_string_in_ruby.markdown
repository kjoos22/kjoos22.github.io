---
layout: post
title:      "Accessing Character(s) of String in Ruby"
date:       2022-01-09 22:02:32 +0000
permalink:  accessing_character_s_of_string_in_ruby
---



Strings are a data type that contain a sequence of letters, numbers, symbols, and whitespace. However, sometimes we need to access an individual character, or just a few characters, of a string. Thankfully Ruby provides a simple and straightforward way for doing so.

Before we get into how to access the character(s) of a string, it is important to understand an underlying concept of strings. Similar to an array, each character in a string has an index number, starting with 0. So for example in the string:

```
my_string = "String"
```

each character's corresponding index would be:

S: 0
t: 1
r: 2
i: 3
n: 4
g: 6

With this knowledge in hand, we can now proceed to accessing piece(s) of the string as needed. To do so, we will be leveraging Ruby's ```slice()``` method. For example:

```
my_string = "String"
my_string.slice(0)
>>> "S"
```

Or if we wanted to access multiple characters, we pass a range of indices to ```slice()```:

```
my_string = "String"
my_string.slice(2..6)
>>> "ring"
```

Additionally we can use negative indices to work backwards from the end of the string. For example:

```
my_string = "String"
my_string.slice(-1)
>>> "g"
my_string.slice(-3)
>>> "i"
```

With this knowledge in hand, we can easily access individual characters or groups of characters of a string in Ruby with ease.

