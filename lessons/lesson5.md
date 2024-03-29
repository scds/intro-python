---
layout: default
title: Lesson 5 - Functions
nav_order: 5
parent: Lessons
---

<!-- Script to resize H5P elements -->
<script src="https://h5pstudio.ecampusontario.ca/modules/contrib/h5p/vendor/h5p/h5p-core/js/h5p-resizer.js" charset="UTF-8"></script>

{: .no_toc}  
# Lesson 5 - Functions

In the previous lessons, we've used lots of functions like `print()`, `range()`, and `sort()`. Functions allow for the ability to reuse code. Aside from the pre-defined functions, you can also create your own functions.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Creating and using functions.
- Understanding the difference between parameters and arguments.

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## What Are Functions?

A function contains lines of code that are run when the function is called. Functions can take in any number of inputs, or no inputs at all. Functions can also output a value, but they don't have to either.

Python provides lots of built-in functions, but you can also make your own.

## When Should I Use Functions?

If you find yourself using the same set of code multiple times throughout your program, you should make a function for it.

Benefits of functions:
- You avoid repeating the same set of code.
- You only have to edit the code once for it to apply to all areas you use the function.


## Creating a Function

In Python, a function is defined using the `def` keyword.

```python
def myFunction():
  print("Hello!")
```

## Calling a Function

As we've already done with other functions, we can call functions using the function name followed by parentheses ( ).

<div class="code-example" markdown="1">

{: .label }
Input
```python
# Any lines of code inside the function will only run when the function is called
def myFunction():
  print("Hello!") 

myFunction()
```

{: .label .label-green }
Output
```
Hello!
```
</div>

## Function Arguments

We can pass data into functions as arguments. Inside the function, these arguments are assigned to a variable which you can use in your code.

<div class="code-example" markdown="1">

{: .label }
Input
```python
def greetings(name):
  print(f"Hello {name}!")

greetings("James")
greetings("Charlotte")
```

{: .label .label-green }
Output
```
Hello James!
Hello Charlotte!
```
</div>

Of course, if the function expects 1 argument, you must provide 1 argument. Providing more or less than what it expects results in an error.

## Parameter vs Argument

The terms parameter and argument often get mixed up and used interchangebly. They do however have different meanings.

**Parameter**
: The variable inside the function definition. In the last example, this would be the `name`.

**Argument**
: The value that is sent to the function. In the last example, this would be "James" and "Charles".

## Positional and Keyword Arguments

By default, the order you put your arguments in should be the same order that the parameters are listed. This is known as Positional Arguments.

<div class="code-example" markdown="1">

{: .label }
Input
```python
def greetings(name, age, country):
  print(f"{name} from {country} is {age} years old.")

greetings("James", 12, "Canada")
```

{: .label .label-green }
Output
```
James from Canada is 12 years old.
```
</div>

If you know the names of the parameters rather than the order, you can use Keyword Arguments instead.

<div class="code-example" markdown="1">

{: .label }
Input
```python
def greetings(name, age, country):
  print(f"{name} from {country} is {age} years old.")

greetings(name = "James", country = "Canada", age = 12)
```

{: .label .label-green }
Output
```
James from Canada is 12 years old.
```
</div>

## Default Arguments

In our function, we can assign our parameters a default argument value. If the function is called without specifying an argument for that parameter, it'll use the default value instead.

{: .note }
Non-default parameters must come before the default parameters in the function declaration. 

<div class="code-example" markdown="1">

{: .label }
Input
```python
def greetings(name, age, country = "Norway"):
  print(f"{name} from {country} is {age} years old.")

greetings(name = "James", country = "Canada", age = 12)
greetings(name = "Charlotte", age = 13)
```

{: .label .label-green }
Output
```
James from Canada is 12 years old.
Charlotte from Norway is 13 years old.
```
</div>

## Return Values

Functions can also return values using a `return` statement. Once a `return` statement is reached, the function returns the value and terminates. No lines of code after `return` are executed.

<div class="code-example" markdown="1">

{: .label }
Input
```python
def quadraticFormula(a, b, c):
  # An exponent to 0.5 is the same as a square root
  x1 = ( -b + (b**2 - 4*a*c)**0.5 ) / (2 * a)
  x2 = ( -b - (b**2 - 4*a*c)**0.5 ) / (2 * a)
  return [x1, x2]

roots = quadraticFormula(1, 5, 6)
print(f"The two roots of x^2 + 5x + 6 are {roots[0]} and {roots[1]}.")
```

{: .label .label-green }
Output
```
The two roots of x^2 + 5x + 6 are -2.0 and -3.0.
```
</div>

<!-- {: .new-title }
> Exercise                            
> 
> Try creating a function with a "number" parameter. The function should return that number multiplied by 2.
>
>
> <details>
>   <summary> See Answer </summary>
>   <div markdown="1">
>   {: .note-title }                                   
> > Answer
> >
> > ```py
> > def multiplyBy2(number):
> >   newNumber = number * 2
> >   return newNumber
> > ```
>   </div>
> </details> -->

<iframe src="https://h5pstudio.ecampusontario.ca/h5p/57509/embed" style="border: solid 2px #7a003c" width="100%" height="350" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

## Empty Functions

If you want to leave a function blank and come back to work on it later, Python won't let you. As mentioned in [lesson 4](lesson4) with control structures, you have to use a `pass` statement.

```python
def quadraticFormula(a, b, c):
  # TODO
  pass
```

## Variable Scope

One thing that we haven't mentioned is the lifecycle of variables. Variables created inside functions are destroyed once the function terminates.

<div class="code-example" markdown="1">

{: .label }
Input
```py
def myFunction():
  a = 5
  b = 6

myFunction()
print(a)
```

{: .label .label-green }
Output
```
NameError: name 'a' is not defined
```
</div>

## Key Points / Summary

- You can create reusable pieces of code using functions.
- Parameters are the variables inside the function declaration, whereas arguments are the values passed to the function.
- Variables inside of functions are destroyed after the function terminates.
