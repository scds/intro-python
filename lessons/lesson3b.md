---
layout: default
title: Lesson 3b - Booleans
nav_order: 2
parent: Lesson 3 - Data Types
grand_parent: Lessons
---

{: .no_toc}  
# Lesson 3b - Booleans

Booleans are one of the simplest data types. It consists entirely of "True" and "False".

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Learn what a boolean is
- Use boolean operators
- Compare numerical values

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## What's a Boolean?

Named after George Boole, a boolean is a value that is either true or false. It's most commonly used in logic. In Python, it's useful for creating conditional statements and loops, which we'll talk about in [lesson 4](lesson4).

## Creating a Boolean Value

In Python, declaring a boolean value is similar to declaring a number. Rather than using a numerical constant, you need to use `True` or `False`.

{: .note }
Make sure `True` and `False` are capitalized!

<div class="code-example" markdown="1">

{: .label }
Input
```python
a = True

print(type(a))
```

{: .label .label-green }
Output
```
<class 'bool'>
```
</div>

## Boolean Operators

Just like integers and floats, booleans have their own set of algebraic rules known as Boolean Algebra.

The three most common operations are listed in the table below.

| Boolean Operator | Keyword |
|------------------|:-------:|
| AND              |   and   |
| OR               |    or   |
| NOT              |   not   |


### AND

The AND operator results in True if both booleans are already True. Otherwise, it becomes False.

<div class="code-example" markdown="1">

{: .label }
Input
```python
a = True
b = True
c = False

print(a and b)
print(a and c)
```

{: .label .label-green }
Output
```
True
False
```
</div>

### OR

The OR operator results in True if at least one boolean is True. Otherwise, it becomes False.

<div class="code-example" markdown="1">

{: .label }
Input
```python
a = True
b = True
c = False

print(a or c)
print(c or c)
```

{: .label .label-green }
Output
```
True
False
```
</div>

### NOT

The NOT operator reverses the current value. True becomes False, and False becomes True.

<div class="code-example" markdown="1">

{: .label }
Input
```python
a = True
c = False

print(not a)
print(not c)
```

{: .label .label-green }
Output
```
False
True
```
</div>

## Numerical Comparisons

We can also compare the values of expressions to generate a boolean as well.

The six comparison operators are shown in the table below.

| Comparison            | Symbol |
|-----------------------|:------:|
| Less than             |    <   |
| Less than or equal    |   <=   |
| Greater than          |    >   |
| Greater than or equal |   >=   |
| Equality              |   ==   |
| Inequality            |   !=   |

<div class="code-example" markdown="1">
{: .label }
Input
```python
print(5 < 8)
print(2 < 1)
print(3 == 3.0)
```

{: .label .label-green }
Output
```
True
False
True
```
</div>

## Key Points / Summary

- A boolean is a True/False value.
- `and`, `or`, and `not` are three boolean operators.
- You can compare numerical values.