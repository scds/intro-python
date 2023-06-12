---
layout: default
title: Lesson 3a - Numbers
nav_order: 1

# Notice the two lines below. Since this is a sub-lesson of a lesson (Lesson 3a), it's parent is lesson 3 and it's grandparent is Lessons. Make sure to include this if you decide to have sub-lessons.
parent: Lesson 3 - Data Types
grand_parent: Lessons 
---

{: .no_toc}  
# Lesson 3a - Numbers 

Python has several "types" of data. We've worked with numbers a lot already, but there are also booleans, strings, and containers. 

In this lesson, we'll be working further with numbers. Python separates numbers into three categories: integers, floats, and complex numbers.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Use the `type()` function to see data types.
- Explore the differences between integers, floats, and complex numbers.

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## What Data Type Am I Working With?

The best way to see what type of data a variable is holding is by using the `type()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
apples = 25      # Integer
liters = 12.5    # Float (decimal)
q = 8.4 + 3j     # Complex Numbers

# We can use the print function to display the output of the type() function.
print(type(myVariable))
print(type(liters))
print(type(q))
```

{: .label .label-green }
Output
```
<class 'int'>
<class 'float'> 
<class 'complex'>
```
</div>

## Integers

Integers in Python, unlike other programming languages, don't have a size limit. If you give Python enough memory resources, you could have 1000... with a million zeroes if you desired.

As we mentioned in a previous lesson, we can use math operations on integers. Addition (+), subtraction (-), multiplication (*), division (/), modulus (%), exponentiation (**), and floor division (//). 

{: .note}
> Division, regardless of whether it produces an integer value, turns the output into a float value. 
> 
> <div class="code-example" markdown="1">
> {: .label }
> Input
> ```python
> a = 6
> b = 2
> print(type(a))
> print(type(b))
> 
> c = a / b       # This is 6/2, which should become 3 
> print(c)
> print(type(c))
> ```
> 
> {: .label .label-green }
> Output
> ```
> <class 'int'>
> <class 'int'>
> 3.0
> <class 'float'>
> ```
> </div>
>
> Despite it being 3, the output becomes 3.0, making it a float.

## Floats

Floats refer to the real number set; integers and decimals. However, it's important to note that floats are approximations (they're only accurate to 7 decimal places). Floats are great for most use cases, but they shouldn't be used when exact precision is required.

<div class="code-example" markdown="1">

{: .label }
Input
```python
# This should add up to 1.0
0.1 + 0.1 + 0.1 + 0.1 + 0.1 + 0.1 + 0.1 + 0.1 + 0.1 + 0.1
```

{: .label .label-green }
Output
```
0.9999999999999999
```
</div>

You can also use scientific notation for numbers. 

<div class="code-example" markdown="1">

{: .label }
Input
```python
G = 6.67430e-11
print(G)

g = 0.0000000000667430
print(g)
```

{: .label .label-green }
Output
```
6.6743e-11
6.6743e-11a
```
</div>

## Complex Numbers

Python supports complex numbers, but they're not often used.

```python
# The imaginary number i is represented by the letter j in Python.
z = 3 + 1j
```

There are some interesting functions available for use with complex numbers that are supported by Python. If you're interested, an in-depth tutorial on complex numbers [can be found here.](https://realpython.com/python-complex-numbers/#getting-to-know-python-complex-numbers)

## Key Points / Summary
- You can use the `type()` function to inspect the data type of a variable.
- Floats are only approximations of decimal numbers and they can lead to rounding errors.
- Integers, floats, and complex numbers are the different number types Python supports.