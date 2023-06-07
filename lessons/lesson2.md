---
layout: default
title: Lesson 2 - Storing and Displaying Data
nav_order: 2
parent: Lessons
---

{: .no_toc}  
# Lesson 2 - Storing and Displaying Data

You may have noticed that Python will only output the last expression in the program. In this lesson, you will learn how to display more data to the screen, as well as how to store data in variables.

<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## Lesson Objectives
- Use variables to store data
- Print data to the console

<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

## Variables

Rather than just using numbers in our calculator, we can initialize and store the number in a variable. With variables, we'll be able to store our data, but then we can also re-use it and even modify that data later on.

## Identifier Rules

All variables need identifiying names, more formerly called identifiers.

Before we use variables, we need to talk about Python's rules and restrictions regarding variable names, otherwise known as identifiers.
- Identifiers can consist of uppercase letters, lowercase letters, digits, and underscores.
- Identifiers cannot start with a digit.
- There are some identifiers reserved for Python's use only, it's usually common keywords like "and", "if", "or", etc.
  - You can find a full list here. https://www.w3schools.com/python/python_ref_keywords.asp

question about valid/invalid identifers

## Assigning Values to Variables

The format to initialize a variable is

<identifier> = <value>

Suppose we wanted to assign "myVariable" the value of 10. We would do

myVariable = 10

If we decide later on that we want to reassign the value of "myVariable" to something else, we would again just do

myVariable = <new value>

and that would set the value of myVariable to our new value.

## Using Variables in Math

Alright, perfect, now we have a variable with some value set to it. How do we use it in our math? Let's say, for some reason, we wanted to find out the value of myVariable if we add 100 to it. We can just do

100 + myVariable

and it'll output the answer.

## Key Points / Summary
TODO
