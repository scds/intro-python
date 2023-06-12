---
layout: default
title: Lesson 4 - Control Structures
nav_order: 4
parent: Lessons
---

{: .no_toc}  
# Lesson 4 - Control Structures

Up until now, we've been executing lines sequentially, one after another. With control structures, we can execute lines conditionally or even create loops of instructions.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Conditionally execute code using `if` statements.
- Loop code using `while` loops and `for` loops.
- Learn about the `pass`, `break`, and `continue` keywords.

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

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the output of the code block below?
>
> ```py
> myNumber = 7
> if myNumber < 6:
>   print(f"{myNumber} is smaller than 6")
>
> if myNumber > 6:
>   print(f"{myNumber} is larger than 6")
> ```
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> > 
> > 7 is larger than 6
>   </div>
> </details>

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

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the output of the code block below?
>
> ```py
> myList = [3, 5, 7, 2, 4]
> if 6 in myList:
>   print("6 is in the list")
> else:
>   print("6 is not in the list")
> ```
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> > 
> > 6 is not in the list
>   </div>
> </details>

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

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the output of the code block below?
>
> ```py
> mark = 67
> if mark > 80:
>   print("You got an A!")
> elif mark > 70:
>   print("You got a B!")
> elif mark > 60:
>   print("You got a C!")
> elif mark > 50:
>   print("You got a D!")
> else:
>   print("Better luck next time!")
> ```
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> > 
> > You got a C!
>   </div>
> </details>

### Extra Exercises

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the output of the code block below?
>
> ```py
> mark = 74
> if mark > 80:
>   print("You got an A!")
> if mark > 70:
>   print("You got a B!")
> if mark > 60:
>   print("You got a C!")
> if mark > 50:
>   print("You got a D!")
> else:
>   print("Better luck next time!")
> ```
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> >
> > You got an A!  
> > You got a B! 
>   </div>
> </details>

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the output of the code block below?
>
> ```py
> heads = [True, False]
> if heads[0]:
>   if heads[1]:
>     print("You got 2 heads!")
>   else:
>     print("You got 1 head.")
> else:
>   if heads[1]:
>     print("You got 1 head.")
>   else:
>     print("You got 0 heads.")
> ```
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> >
> > You got 1 head.
>   </div>
> </details>

## Loops

In Python, there's often a need to repeat pieces of code multiple times, whether they're exactly the same or with a slight variance. There are two different control structures to deal with looping, `while` loops and `for` loops.

### `while` Loops

`while` loops are used to repeat a piece of code until an expression evaluates to be `False`.

```python
while expression:
  line1
  line2

line3
```

The code above would run line1 and line2 repeatedly until the `expression` is `False`. You can easily run into an infinite loop if you forget about the expression. For the loop to terminate, a part of the code inside the while loop has to modify the expression in some way.

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the output of the code block below?
>
> ```py
> myList = []
> x = 2
>
> while len(myList) < 5:
>   myList.append(x)
>   x = x * 2
>
> print(myList)
> ```
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> >
> > [2, 4, 8, 16, 32]
>   </div>
> </details>

### `for` Loops

`for` loops also repeat pieces of code, just like `while` loops. However, the number of times a `for` loop repeats is based on the number of items in an "iterable". An iterable is an object that is capable of returning items one at a time. A great example of an iterable is a list.

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

{: .new-title }
> Exercise                                             <!-- This is where you edit the title -->
> 
> What is the output of the code block below?
>
> ```py
> myList = ["Jeremy", "Charlotte", "Brian", "Angelica"]
>
> for name in myList:
>   print(f"Hi {name}!")
> ```
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> >
> > Hi Jeremy!  
> > Hi Charlotte!  
> > Hi Brian!  
> > Hi Angelica!
>   </div>
> </details>

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

### Pass, Break, and Continue

There are three keywords that occasionally find use in loops, `pass`, `break` and `continue`.

#### Pass
If you want to create an conditional statement or loop and leave it empty, you need to use the `pass` keyword. Python will give you an error if you leave it blank. 

```py
if expression:
  pass

for x in range(5):
  pass
```

#### Break

If you decide you want to "break" out of a `while` loop before the condition evaluates to `False`, or a `for` loop before it finishes iterating over the items, you can use `break`.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [5, 3, "word", 2, 6]
mySum = 0

for item in myList:
  # If the item is not an integer, reset the sum, send an error message, and break out of the loop.
  if type(item) != type(1): 
    mySum = 0
    print("ERR: This list contains an item that is not an integer.")
    break
  else:
    mySum = mySum + item

print(f"The sum is {mySum}.")
```

{: .label .label-green }
Output
```
ERR: This list contains an item that is not an integer.
The sum is 0.
```
</div>

#### Continue

Rather than breaking out of a loop, you can also `continue`. `continue` skips the rest of the current iteration and moves onto the next one.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myList = [5, 3, "word", 2, 6]
mySum = 0

for item in myList:
  # If the item is not an integer, send an error message and continue to the next iteration of the loop.
  if type(item) != type(1): 
    print("ERR: This list contains an item that is not an integer.")
    continue
  else:
    mySum = mySum + item

print(f"The sum is {mySum}.")
```

{: .label .label-green }
Output
```
ERR: This list contains an item that is not an integer.
The sum is 16.
```
</div>

## Key Points / Summary

- You can use the `if`, `else`, and `elif` to create conditionally executed code.
- You can also use `for` and `while` to create loops.
- Use `pass` to fill up empty conditional statements or loops and prevent errors.
- `break` and `continue` can skip iterations of a loop, or stop the loop completely.
