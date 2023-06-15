---
layout: default
title: Lesson 3c - Strings
nav_order: 3
parent: Lesson 3 - Data Types
grand_parent: Lessons
---

{: .no_toc}  
# Lesson 3c - Strings

Another one of Python's built-in data types are strings. Strings represent a sequence of characters.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Learn about strings
- Explore some of the operations and functions Python has to offer for strings.
- Convert variables into strings.
- Format strings for more informative `print()` output.

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## Creating a String
In Python, strings are surrounded by single quotes (' ') or double quotes (" ").

{: .warning }
Don't mix and match! You can't have a string start with single quotes and end with double quotes.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "Hello, World!"

print(myString)
```

{: .label .label-green }
Output
```
Hello, World!
```
</div>

## Using Quotations Inside Strings

If you need to use single quotes ' ', use double quotes " " to define the string.

```py
myString = "I'm happy!"
```

If you need to use double quotes " ", use single quotes ' ' to define the string.

```py
myString = 'He said "hello".'
```

If you need to use both single quotes ' ' and double quotes " ", you need to put a backslash \ before every quotation you defined the string with.

```py
myString = "He said that \"He's happy\""
myString = 'He said that "He\'s happy"'
```

## String Concatenation and Repetition

You can combine string together by using the `+` operator.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "abc"
myString2 = "ABC"

print(myString + myString2)
```

{: .label .label-green }
Output
```
abcABC
```
</div>

Similarly, you can repeat a string by using the `*` operator.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "abc"

# Repeats myString 5 times.
print(myString * 5)
```

{: .label .label-green }
Output
```
abcabcabcabcabc
```
</div>

## String Operations and Functions

### Length of a String
Before we get to indexing and slicing strings, let's briefly mention the `len()` function. It returns the number of characters in a string.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "abc"

print(len(myString))
```

{: .label .label-green }
Output
```
3
```
</div>

### Indexing
If we wanted to get the character at a specific index of a string, we have to use a special notation. It's best to show an example.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "Hello."

print(myString[0])
print(myString[1])
print(myString[2])
print(myString[3])
print(myString[4])
print(myString[5])
```

{: .label .label-green }
Output
```
H
e
l
l
o
.
```
</div>

As you can see, to index a string, you have to mention the variable name followed by a number surrounded by square brackets [ ].

{: .important }
In most programming languages, including Python, the first index starts at 0. If we want to get the 1st character of a string, we need to get the 0th index. If we want to get the 4th character of a string, we need to get the 3rd index.

{: .warning }
Python will give you an error if you try to access a string index that does not exist. Using `myString = "Hello."` as an example, accessing the 8th index by doing `myString[8]` will give you an error because the 8th index does not exist.

### Backwards Indexing

You can also index starting from the end of the string by using negative numbers for your index.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "Hello."

print(myString[-1])
print(myString[-2])
print(myString[-3])
print(myString[-4])
print(myString[-5])
print(myString[-6])
```

{: .label .label-green }
Output
```
.
o
l
l
e
H
```
</div>

You can see here that the last character can be found by using -1 as your index.

### Slicing
Using indexes, we can also slice the string into a substring.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "Hello."

print(myString[1:3])  # Gets index 1 (inclusive) to index 3 (exclusive).
print(myString[1:])   # Gets index 1 (inclusive) to the end of the string.
print(myString[:3])   # Gets the entire string up until index 3 (exclusive).
```

{: .label .label-green }
Output
```
el
ello.
Hel
```
</div>

### Skipping Letters and Reversing a String
Using the same notation as slicing, we can also reverse a string.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "Hello."

print(myString[::2])   # From the start to the end of the string, get every 2nd letter
print(myString[::-1])  # From the start to the end of the string, go backwards
```

{: .label .label-green }
Output
```
Hlo
.olleH
```
</div>

### Membership Checking
Using membership checking, we can check if a string is part of another string.

There are two operators for Membership Checking.

in
: Checks if a string **is** part of another string.

not in
: Checks if a string **is not** part of another string.

<div class="code-example" markdown="1">

{: .label }
Input
```python
myString = "Hello! Welcome to the SCDS."
animal = "Penguin."

print("Welcome" in myString)   # Checks if the string "Welcome" is in myString.
print(animal not in myString)  # Checks if the string "Penguin." is not in myString.
```

{: .label .label-green }
Output
```
True
True
```
</div>

## Converting Variables to Strings
The `str()` function converts a variable into a string. 

<div class="code-example" markdown="1">

{: .label }
Input
```python
testScore = 18/24*100

# str(testScore) turns the test score into a string, and appends it into a sentence. 
print("Your test score was " + str(testScore) + "%.")
```

{: .label .label-green }
Output
```
Your test score was 75.0%.
```
</div>

## String Formatting
Another way to insert variables into strings is by using the `format()` function.

<div class="code-example" markdown="1">

{: .label }
Input
```python
numerator = 18
denominator = 24

print("Your test score was {}/{}.".format(numerator, denominator))
```

{: .label .label-green }
Output
```
Your test score was 18/24.
```
</div>

The `format()` function has a lot of other cool functionalities, [which can be found here.](https://www.w3schools.com/python/ref_string_format.asp)

You can also accomplish the same thing by adding the letter `f` at the start of the string, before the surrounding quotes.

<div class="code-example" markdown="1">

{: .label }
Input
```python
testScore = 18/24*100

print(f"Your test score was {testScore}%.")
```

{: .label .label-green }
Output
```
Your test score was 75.0%.
```
</div>

## Key Points / Summary

- Strings are sequences of characters.
- The first character in a string is at index 0.
- You can convert variables into strings.
