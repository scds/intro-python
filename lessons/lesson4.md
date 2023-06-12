---
layout: default
title: Lesson 4 - Control Structures
nav_order: 4
parent: Lessons
---

{: .no_toc}  
# Lesson 4 - Control Structures

Up til now, we've been executing lines sequentually, one after another. With control structures, we can execute lines conditionally or create loops of instructions.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- A learning objective.
- Second learning objective.
- Another learning objective.

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## Conditional Statements

### `if` Statements

With conditional statements, we can test a boolean expression to decide whether or not to execute lines of code. In Python, this is done using an `if` statement.

```python
if expression:
  line1
  line2
line3
```

Take a look at the code block above. This is the general structure of an `if` statement. If the `expression` is evaluation to be `True`, line1 and line2 will execute. Otherwise, if the `expression` is evaluated to be `False`, Python will skip over line1 and line2.

An important part of Python that we haven't discussed yet is the indentation. With `if` statements, anything you want to be included within the conditional statement needs to be indented with a `Tab`. In the example above, line1 and line2 are conditionally executed, whereas line3 will always be executed since it is not part of the if statement.

### `else` Blocks

Occasionally, you'll need to have two seperate pieces of code. One if the condition succeeds, and one if the condition fails. You can use the `else` keyword to do just that!

```python
if expression:
  line1
  line2
else:
  line3
```

In the example above, line1 and line2 are executed if the expression evaluates to be `True`. Otherwise, if the expression evaluates to be `False`, line3 will be executed.

### `elif` Blocks

Sometimes, `if` and `else` is not enough. You might need to test multiple ranges of numbers. This is where the `elif` keyword comes in.

```python
if expression:
  line1
elif expression2:
  line2
else:
  line3
```

In the example above, line1 is executed if `expression` evalutes to be `True`. If and only if `expression` evaluates to be `False`, it will test `expression2`. If `expression2` is `True`, line 2 will be executed. Otherwise, line3 will be executed.


## Loops

In Python, there's often a need to repeat pieces of code multiple times, whether it be exactly the same or with a slight variance. There are two different control structures to deal with looping, `while` loops and `for` loops.

### `while` Loops

`while` loops are used to repeat a piece of code until an expression evaluates to be `False`.

```python
while expression:
  line1
  line2

line3
```

The code above would run line1 and line2 repeatedly until the `expression` is `False`. You can easily run into an infinite loop if you forget about the expression. For the loop to terminate, a part of the code inside the while loop has to modify the expression in some way.

### `for` Loops

`for` loops also repeat pieces of code, just like `while` loops. However, the amount of times a `for` loop repeats is based on the number of items in an "iterable". An iterable is an object that is capable of returning items one at a time. A great example of an iterable is a list.

```python
for x in [1,2,3]:
  line1
```

In the code block above, line1 will execute 3 times. Every time a new loop starts, `x` is set to the value of the current iterable, meaning that we can use `x` as part of our code.

<div class="code-example" markdown="1">

{: .label }
Input
```python
for x in [1,2,3]:
  print(x)
```

{: .label .label-green }
Output
```
1
2
3
```
</div>

`count()` is a useful function for creating `for` loops. `count(x)` automatically creates a list from 1 to `x` (inclusive) for the loop to iterate over.

<div class="code-example" markdown="1">

{: .label }
Input
```python
for x in count(5):
  print(x)
```

{: .label .label-green }
Output
```
1
2
3
4
5
```
</div>

## Key Points / Summary

- Remind the student about what they just learned.
- You can also note down any key information to keep in mind.

## Additional Resources (optional)

- Here, you can list some additional resources the student can access to learn more about this lesson.
