---
layout: post
title:      "Algorithms - Binary Search"
date:       2021-10-31 19:40:25 +0000
permalink:  algorithms_-_binary_search
---


One of the core areas of software engineering is the use of algorithms. Algorithm is defined as "a set of steps that are followed in order to solve a mathematical problem or to complete a computer process". Often software engineers will find themselves implementing algorithms to accomplish various goals. Today's blog post will discuss one of the first algorithms that many come across when studying the topic - Binary Search.

Binary search is an algorithm for finding a target value (or its index) in a sorted array. If the array is not pre-sorted, then it must be sorted before binary search will work. Since the array is sorted, it is often best to compare the target value to the final (or greatest) value in the array, and if that value is less than the target, then you can immediately return a "target not found". Next, determine the middle of the array, and to compare the target value to the middle value. If the middle value is greater than the target value, then eliminate the second half of the array, and repeat the process. Conversely, if the middle value is less than the target value, then eliminate the first half of the array, and repeat the process. Doing this will eventually determine where in the array the target lies, if at all. 

Binary search has an algorithmic efficiency, or Big O notation, of O(log n), with a best case scenario (mid value is target value) of O(1). If you're unfamiliar with Big O, you can read more about it [here](https://www.freecodecamp.org/news/big-o-notation-why-it-matters-and-why-it-doesnt-1674cfa8a23c/). Binary search can also be used to determine the next closest value to the target that is present in the array, in the case that the target is not. Binary search can also be extended to perform approximate matches. Due to this it can be a very powerful algorithm in the right situation.

There are different ways to implement binary search. It can be implemented via either a recursive or iterative approach. Some languages even include binary search in their standard library for use, including Python, Ruby, Java, and many others. A common pitfall when writing an implementation of binary search is not [flooring](https://www.mathsisfun.com/sets/function-floor-ceiling.html) the index when determining the middle of the array.

That's all for this week on binary search. Be sure to check back in the future for more algorithm discussion. 


