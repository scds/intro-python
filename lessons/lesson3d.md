---
layout: default
title: Lesson 3d - Containers
nav_order: 4
parent: Lesson 3 - Data Types
grand_parent: Lessons
---

{: .no_toc}  
# Lesson 3d - Containers
Suppose we had to keep track of the class average. We can’t just make a variable for each mark because there could be dozens, maybe hundreds, of marks to store. This is where containers come in.

Containers can hold an arbitrary amount of data. There are different kinds of containers, and we’ll be going over four of them today. Lists, tuples, sets, and dictionaries.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Use containers to store data.
- Learn the differences between lists, tuples, sets, and dictionaries.
- Use the `help()` function to discover more functions.

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## Lists
Lists are the most common type of container because of their ease of use.

They can hold any number of objects, which can also change throughout the program. This means that we can add and remove data from the list after its initial declaration. 

The contents of a list are also ordered.

{: .note }
> In the context of containers, for a container to be ordered, there's always a "first" element, followed by a "next" element.
> 
> It **does not** mean that it sorts the data.

Lists are created by surrounding data with square brackets [ ]. The line of code below creates a list with some pieces of data.

```python
myList = [1, 2.0, 3, "hello", 2]
```

### Length of a List

You'll notice in the next few sections that lists behave a lot like strings in a lot of scenarios. Just like with strings, you can find the number of items a list contains by using the `len()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]

print(len(myList))
```

{: .label .label-green }
Output
```
5
```
</div>

### List Indexing

You can also access a particular index of a list using the square bracket notation we use when working with strings.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]

print(myList[2])
```

{: .label .label-green }
Output
```
3
```
</div>

{: .warning }
Just like with strings, Python will give you an error if you try to access a list index that does not exist. Using `myList = [1, 2.0, 3, "hello", 2]` as an example, accessing the 8th index by doing `myList[8]` will give you an error because the 8th index does not exist.

### List Slicing

Once again, just like strings, we can also slice portions of lists.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]

print(myList[1:3])
```

{: .label .label-green }
Output
```
[2.0, 3]
```
</div>

### Multidimensional Lists
Lists can also contain other lists!

```python
myList = [ [1, 2, 3], ["a", "b", "c"] ]
```

To access the integer `3` from the first list inside the list, we have to do the following.

```python
myList[0][2]
```

`myList[0]` will give us `[1, 2, 3]`. Since we want the `3`, we need to index again, adding another `[2]` to it. This leaves us with `myList[0][2]`.

{: .new-title }
> Exercise 1                                           <!-- This is where you edit the title -->
> 
> How would you access the `"b"` string in the second list of `myList`?
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> > 
> > ```python
> > myList[1][1]
> > ```
> > 
> > `myList[1]` will give us `["a", "b", "c"]`. Since we want the `"b"`, we need to index again, adding another `[1]` to it. This leaves us with `myList[1][1]`.
>   </div>
> </details>

### Dot Notation for Functions

Unlike all of the functions we've used before, the following couple functions have a different syntax. You'll see that it follows the following format:

```python
variable.function()
```

Functions that follow the dot notation above are unique to that particular data type. In this case, `append()` will only work on lists.

To get a full list of dot notation functions for any variable and data type, use the `help()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2, 3, 4]
help(myList)
```

{: .label .label-green }
Output
```
Help on list object:

class list(object)
 |  list(iterable=(), /)
 |  
 |  Built-in mutable sequence.
...
```

**Output is too large to put here, try it out in your Python interpreter!**
</div>

### Adding Elements to a List

The easiest way to add an element to a list is to use the `append()` function. The `append()` function adds an element to the end of the list.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
myList.append(24)
print(myList)
```

{: .label .label-green }
Output
```
[1, 2.0, 3, "hello", 2, 24]
```
</div>

Alternatively, you can use the `insert()` function if you'd like to insert an element at a specific index.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
myList.insert(3, 24) # Insert the value 24 into index 3
print(myList)
```

{: .label .label-green }
Output
```
[1, 2.0, 3, 24, "hello", 2]
```
</div>

### Removing Elements from a List

To remove the last element in a list, you can use the `pop()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
myList.pop()
print(myList)
```

{: .label .label-green }
Output
```
[1, 2.0, 3, "hello"]
```
</div>

If you want to remove a specific index, you can use the `pop()` function again, but specify which index to remove.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
myList.pop(3)
print(myList)
```

{: .label .label-green }
Output
```
[1, 2.0, 3, 2]
```
</div>

If you'd rather remove a specific element from a list (a value rather than an index), you can use the `remove()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
myList.remove(3)
print(myList)
```

{: .label .label-green }
Output
```
[1, 2.0, "hello", 2]
```
</div>

{: .note }
The `remove()` function will only remove the first occurrence of a value.

### List Concatenation and Repetition

Just like strings, we can concatenate and repeat lists.

#### Concatenation
<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
myList2 = [5, 2, 1]
print(myList + myList2)
```

{: .label .label-green }
Output
```
[1, 2.0, "hello", 2, 5, 2, 1]
```
</div>

#### Repetition
<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2]
print(myList * 3)
```

{: .label .label-green }
Output
```
[1, 2, 1, 2, 1, 2]
```
</div>

### Other Useful List Functions

If you want to find what the index of a particular value, you can use the `index()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
print(myList.index(3))
```

{: .label .label-green }
Output
```
2
```
</div>

{: .note}
Just like the `remove()` function, `index()` will only find the first occurrence of a value.

If you want to find the amount of times a particular value appears in a list, you can use the `count()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2.0, 3, "hello", 2]
print(myList.count(2))
```

{: .label .label-green }
Output
```
2
```

In this case, it considers 2.0 and 2 to have the same value.
</div>

If you want to sort the contents of a list, you can use the `sort()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [53, 23, 12, -2, 43.2, 43]
myList.sort()
print(myList)
```

{: .label .label-green }
Output
```
[-2, 12, 23, 43, 43.2, 53]
```
</div>

And finally, if you want to reverse the contents of a list, you can use the `reverse()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [53, 23, 12, -2, 43.2, 43]
myList.reverse()
print(myList)
```

{: .label .label-green }
Output
```
[43, 43.2, -2, 12, 23, 53]
```
</div>

## Tuples

Tuples are similar to lists in a lot of ways. Tuples are also containers that store ordered data, and they index and slice the exact same way as lists.

What makes tuples unique is that, once they’re created, they can’t be modified. This means that you can’t add or remove new elements from a tuple. To do so would mean creating a duplicate tuple with the new changes.

Tuples are less commonly used because of this trait, but it does speed up some computational processes.

To create a tuple, you use round brackets ( ) rather than square brackets [ ].

```python
myTuple = (1, 2, 3, 4)
```

{: .note }
> If a tuple contains only one object, you need to include a comma inside the brackets. If you don't, Python will see the brackets as indicating the order of operations.
> 
> ```python
> myTuple = (1,)
> ```

## Sets

Sets are also similar to lists in a few ways. They are also containers that store data, and this container **can** be modified (meaning you can add and remove elements). Sets, however, are not ordered and they do not allow for duplicate elements (much like mathematical sets).

To create a set, you use curly brackets { }.

```python
mySet = {1, 2, 3, 4}
```

Since sets are unordered, you can't slice or index them. There isn't a "first" or "second" element in a set.

The most common use-case for a set is to remove duplicate elements from a list. You can turn a list into a set by using the `set()` function, and similarly, you can turn a set into a list using the `list()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [1, 2, 5, 2, 2, 4, 2, 4, 6, 4]

mySet = set(myList)

print(mySet)
```

{: .label .label-green }
Output
```
{1, 2, 4, 5, 6}
```
</div>

## Dictionaries

Dictionaries are the most distinct of all the containers. They consist of "key-value pairs". Rather than using index numbers to index values in the list, dictionaries use "keys" for indexing. 

They work very similarly to dictionaries in real life. The key would be the word, whereas the value would be the definition. To find the definition of a word, you need to search the dictionary for its key (the word itself). See the code below for an example.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myDict = {"x": 1, "y": 3, "z": -2}
print(myDict["x"])
print(myDict["z"])
```

{: .label .label-green }
Output
```
1
-2
```
</div>

Dictionaries are defined similarly to sets, using curly braces { }. However, because they consist of key-value pairs, the curly braces contain `<key>: <value>` "objects". After the dictionary is created, you can access any of the values by referencing its key. We defined "x" to have a value of 1, so when we index "x" in the print statements later on, we get back 1.

Just like sets, dictionaries cannot contain duplicate keys (they can however contain duplicate values.) 

## Key Points / Summary

- Containers store multiple "cells" of data.
- Lists, tuples, sets, and dictionaries are all containers.
- You can use the `help()` function to list out all functions unique to a particular data type.
