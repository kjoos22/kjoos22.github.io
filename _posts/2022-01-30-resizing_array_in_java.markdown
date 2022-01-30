---
layout: post
title:      "Resizing Array in Java"
date:       2022-01-30 18:43:17 +0000
permalink:  resizing_array_in_java
---


If you have worked in other languages and then come to Java, one thing that can take some getting used to is the fact that arrays in Java are of a fixed size. This means that once the array is declared and memory is allocated for it, that the number of elements can not be changed. This can lead to some difficulties depending on the use of your array, and what information you had at the time of creation. While there are several ways to work around this issue, including the use of the dynamically sized ArrayList class from the java.util package, today we are going to focus on the ```copyOf()``` method.

The ```copyOf()``` method does exactly what it sounds like it does, it creates a copy of the array it is called upon. However, that is not the extend of the method's functionality. The ```copyOf()``` method accepts two arguments. The first argument is the original array of which you wish to make a copy, the 2nd argument is the size of the new array. In the case that the new array is larger than the original array, the new array will be padded at the end with 0 element(s). In the case that the new array is smaller than the original array, the new array will be truncated from the original contents.

Example:

```
int arr[] = new int[]{1, 2, 3, 4, 5};

int new_arr[] = Arrays.copyOf(arr, 6);

System.out.println(new_arr);
System.out.println("Size: " + new_arr.length);
```
Output:
```
[1, 2, 3, 4, 5, 0]
Size: 6
```

This is just one of the many ways to copy and/or resize an array in Java. 
