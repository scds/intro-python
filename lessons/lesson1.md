---
layout: default
title: Lesson 1 - Using Python as a Calculator
nav_order: 1
parent: Lessons
---

{: .no_toc}  
# Lesson 1 - Using Python as a Calculator

The simplest thing we can do with Python is use it as a calculator. Addition, subtraction, multiplication -  you name it!

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Learn about some of the mathematical operations Python supports.
- Use the math library to get access to more math functions.

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## Math Operations

Using Python as a calculator works exactly as you think it should.

<div class="code-example" Markdown="1">
{: .label }
Input
```python
5 + 7
```

{: .label .label-green }
Output
```
12
```
</div>

By default, Python supports addition (+), subtraction (-), multiplication (*), division (/), modulus (%), exponentiation (**), and floored division (//). 

If there are multiple operations in the same line, they follow the order of operations outlined in the table below. Operations at the top have higher precedence. Rows with multiple operations have equal precedence and are evaluated from left to right in the expression.

<!-- https://www.tablesgenerator.com/markdown_tables -->

|                       Operation                       |        Symbol       |
|-------------------------------------------------------|:-------------------:|
|                      Parentheses                      |       `(` `)`       |
|                       Exponents                       |         `**`        |
| Multiplication, Division, Floor Division, and Modulus | `*`, `/`, `//`, `%` |
|                Addition and Subtraction               |       `+`, `-`      |

<div class="code-example" Markdown="1">
{: .label }
Input
```python
5 + 2 * (2**3 / 2)
```

{: .label .label-green }
Output
```
13
```
</div>

Although we've only been using integers for our math, Python supports decimal numbers as well as complex numbers. We'll briefly talk about complex numbers later in [Lesson 3a.](lesson3a)

<div class="code-example" Markdown="1">
{: .label }
Input
```python
3.2 * 5 + 0.102
```

{: .label .label-green }
Output
```
16.102
```
</div>

## Other Math Functions
Other math functions, such as log, sin, and cos, are supported in some of Python's math libraries. A library is a package of functions or values. To gain access to these functions, we need to add an extra line of code at the top.

<div class="code-example" Markdown="1">

{: .label }
Input
```python
import math

math.cos(0)
```

{: .label .label-green }
Output
```
1.0
```
</div>

The first line, `import math`, tells Python to include some math functions that are not included by default.

In the second line, we're using the `cos()` function from the `math` library. Since `cos()` only needs one input value, we put it inside the brackets.

A full list of functions and values that the math library provides can be found here: <https://www.w3schools.com/python/module_math.asp>.

## Key Points / Summary
- You can use Python as a calculator.
- To get access to more math functions, you have to `import` the math library.