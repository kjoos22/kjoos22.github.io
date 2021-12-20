---
layout: post
title:      "Ruby Map Method"
date:       2021-12-20 02:20:46 +0000
permalink:  ruby_map_method
---


The Ruby map method is a simple but powerful tool in any Ruby developer's arsenal. The map method is used when you need to transform data, and can be used on arrays, hases, and ranges. If you have one of the afforementioned data structures and need to alter each item in the collection in the same manner, then map is the method to use.

Your first instinct may be to use the each method, as that will allow you to iterate through a collection and do something with each individual entry in said collection. However, the each method does not collect the results of whatever action(s) you undertake on each entry in the collection. Ultimately, the each method will return the original unaltered collection. While you could tell the each method to store the altered collection entry in either a new collection, or in place in the original collection, this requires additional work, and could possibly lead to unintentional ambiguity in your code when read by others. Instead, use the map method, which inherently will return a new collection with the transformed data.

The syntax for map is very similar to the afforementioned each. Call the `.map` method on the necessary collection, have the working name for the invidividual elements in pipes, `|element|`, and finally contain the instructions for alteration either within a single line wrapped in curly braces, or make use of a do block. Examples for both approaches:

```
a = [1, 2, 3, 4]
a.map { |num| num * 3 }
=> [3, 6, 9, 12]
```

or

```
a = [1, 2, 3, 4]
a.map do |num|
     num * 3 }
end
=> [3, 6, 9, 12]
```

A common pitfal that may be encountered is using the map method on a collection, and later using the collection, only to find the original unaltered collection in place. This may seem to contradict what I mentioned earlier about how map differs from each, and beg the question of 'why is the collection in its unaltered state?'. This occurs when you do not point the map method to a variable for storage upon completion. You can either store the return value in the original collection, or if you need the original one as well, in a new collection. Examples for both approaches:

```
a = [1, 2, 3, 4]
a = a.map { |num| num * 3 }
a
=> [3, 6, 9, 12]
```

or 
```
a = [1, 2, 3, 4]
b = a.map { |num| num * 3 }
b
=> [3, 6, 9, 12]
a
=> [3, 6, 9, 12]
```

With the map method, you are ready to take on tranforming collections in Ruby, whatever the necessary transformations are. 

