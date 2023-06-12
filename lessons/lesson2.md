---
layout: default
title: Lesson 2 - Storing and Displaying Data
nav_order: 2
parent: Lessons
---

{: .no_toc}  
# Lesson 2 - Storing and Displaying Data

You may have noticed that Python will only output the last expression in the program. In this lesson, you will learn how to display more data to the screen as well as how to store data in variables.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Use variables to store data.
- Print data to the console.
- Use comments to make notes in our program.

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## Variables

Rather than just using numbers in our calculator, we can initialize and store the number in a variable. With variables, we'll be able to store our data, but we can also re-use it and even modify that data later on.

## Identifier Rules

All variables need identifying names, more formerly called identifiers.

Python has some rules and restrictions for identifiers.
- Identifiers can consist of uppercase letters, lowercase letters, digits, and underscores.
- Identifiers cannot start with a digit.
- There are some identifiers reserved for Python's use only; they're usually common keywords like "and", "if", "or", etc.
  - You can find a full list here: <https://www.w3schools.com/python/python_ref_keywords.asp>
- Identifiers are case-sensitive.
  - `myVariable` and `MYVARIABLE` are considered two different variables.

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> Which of the following are valid variable names?
>
> - myVariable
> - _digits
> - 10_hp
> - finally
> - NAME
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> > 
> > - myVariable is a valid variable name.
> > - _digits is a valid variable name.
> > - 10_hp is **not** a valid variable name because it begins with a digit.
> > - finally is **not** a valid variable name because it's one of Python's reserved keywords.
> > - NAME is a valid variable name.
>   </div>
> </details>

## Assigning Values to Variables

The format to create a variable is:

```python
identifier = value
```

Suppose we wanted to assign `myVariable` the value of 10. We would do

```python
myVariable = 10
```

The line above is read as "`myVariable` is assigned the value of 10."

If we decide later on that we want to reassign the value of `myVariable` to something else, we would again do

```python
myVariable = <new value>
```

and that would set the value of `myVariable` to our new value.

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the value of **a** after this code is executed?
>
> ```python
> a = 5
> b = 10
> a = b
> b = 2
> ```
> 
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> > 
> > The value of **a** is 10.
> > 
> > - Going step-by-step, **a** is assigned the value of 5.     (a = 5)  
> > - Then, **b** is assigned the value of 10.                  (a = 5, b = 10)  
> > - **a** is assigned the value of **b**, which is 10.            (a = 10, b = 10)  
> > - Finally, **b** is assigned the value of 2.                (a = 10, b = 2)
>   </div>
> </details>

## Using Variables in Math

Perfect, now we have a variable with some value set to it. How do we use it in our math? Let's say, for some reason, we wanted to find out the value of myVariable if we add 100 to it. We can just do

```python
100 + myVariable
```

and it outputs the answer.

## Displaying Data to the Console

Take a look at the code block below.

```python
50 * 0.9
50 * 0.5
```

What do you think will be shown if we run both lines in the same code block? After trying it out, you'll discover that it only outputs the answer of one of the lines. That's because Python will only show you the last line that returns data.

If we want to display more data to the screen, we have to use the `print()` function to "print" it to the console.

<div class="code-example" markdown="1">
{: .label }
Input
```python
print(50 * 0.9)
print(50 * 0.5)
```

{: .label .label-green }
Output
```
45
25
```
</div>

## Writing Comments in your Code

Sometimes, it's useful to write yourself (or others) comments about your code. They can be used to explain pieces of code, and generally, they make the code more readable.

Python considers everything after a `#` symbol a comment and ignores it when executing the code.

<div class="code-example" markdown="1">
{: .label }
Input
```python
# print() displays information to the screen.
print(50 * 0.9)
print(50 * 0.5)
```

{: .label .label-green }
Output
```
45
25
```
</div>

Since Python ignores comments, you can also use it to prevent lines of code from being executed. This is particularly useful when troubleshooting issues with your code.

<div class="code-example" markdown="1">
{: .label }
Input
```python
# print() displays information to the screen.
# print(50 * 0.9)
print(50 * 0.5)
```

{: .label .label-green }
Output
```
25
```
</div>

## Key Points / Summary
- You can use variables to store data.
- The `print()` function can print data to the console.
- You can use comments to document and explain your code.
