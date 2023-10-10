# Lab-10: Booleans

**This is not not going to be fun.**

## Overview

This lab will give you practice working with Boolean variables and expressions.

You'll be practicing:

- Evaluating Boolean expressions by hand (and checking your work in Python).
- Creating Boolean-returning functions.

## Python language focus

The focus of this lab will be on:

- Writing valid Python functions that return a Boolean.

## Do These Things

### Part 1: Evaluating Boolean Expressions

This part of the tutorial is intended to get you used to working with Boolean expressions and variables. 

Working on paper or the whiteboard, work through the following exercises. You can check your answers using the Python interpreter, **but try to solve them by hand first**.

_Hint: when evaluating Boolean expressions, [short-circuit evaluation](https://www.geeksforgeeks.org/short-circuiting-techniques-python/) can make your job easier!_

1. Assume we have the following variables:
    
    ```python
    w = 10
    x = 5
    y = 3
    z = 8
    ```
    Evaluate the following Boolean expressions:
    1. `(x == 5 and y < 3) or (w != 0 and z < 10)`
    2. `(z > 5 or w <= 10) and x > 5`
    3. `z > 5 or (w <= 10 and x > 5)`
    4. `(y == 3 or not (w > 10)) and (not (x < 10) or (z != 5))`

2.  Assume we have the following variables:

    ```python
    x = True
    y = False
    z = True
    ```

    Evaluate the following Boolean expressions:
    1. `x and y or x and z`
    2. `(x or not y) and (not x or z)`
    3. `x or y and z`
    4. `not (x or y) and z`
    5. `not (z or y) or x`
    6. `y and x and z`
    7. `not z or (y or not x)`
    8. `x or x and y`

3. Match each Boolean expression in the left (numbered) column with the equivalent expression in the right (lettered) column:

    |   |                                  |   |                     |
    |---|----------------------------------|---|---------------------|
    | 1 | `not (x != y) and y == z`        | a | `x < y and y < z`   |
    | 2 | `not (x <= y or y < z)`          | b | `x > y and y >= z`  |
    | 3 | `(y < z or y == z) or x == y`    | c | `x != y or y == z`  |
    | 4 | `not (x >= y) and  not (y >= z)` | d | `x == y or y <= z`  |
    | 5 | `not (x == y and y != z)`        | e | `x == y and y == z` |

4. The following expressions make sense in English, but are incorrect according to Python's rules of syntax. Rewrite them as legal Python expressions which evaluate as intended. Assume all variables are of type `int`.

    1. x and y are greater than zero		
    2. x is equal to neither y nor z
    3. x is equal to y and z
    4. x is equal to at least one of y and z
    5. x is equal to at most one of y and z
    6. x is equal to y or z, but not both		


### Part 2: Designing Boolean-returning Functions

**Before beginning this next part, create a script file to hold your work.**

1. Design and test a function called `is_factor(x, y)`, where both x and y are integers. It returns True if x is a factor of y.

    ```python
    is_factor(2, 4) # should return True, since 2 is a factor of 4
    is_factor(3, 7) # should return False, 3 is not a factor of 7
    ```

2. Design and test a function `is_even(x)`, where x is an integer. It returns True if x is an even number. You must use your `is_factor` function in your solution.

    ```python
    is_even(8)   # should return True, since 8 is an even number
    is_even(11)  # should return False, since 11 is not an even number
    ```

3. Let us define a **cardinal number** as a number we use for counting in English (1, 2, 3, 4...). Design and test a function `is_cardinal(x)` that takes in a number x - **but you don't know whether x will be a `float` or an `int`**. It returns True if x is a cardinal number.

   _Note: You might have to do a bit of research for this one: how can you tell whether an argument is an integer?_

    ```python
    is_cardinal(3)   # should return True, since 3 is an cardinal number
    is_cardinal(0)   # should return False, since 0 is not an cardinal number
    is_cardinal(3.0) # should return False, since 3.0 is not an cardinal number
    ```

4. (BONUS) Design and test a function which takes a year (as an integer). It returns True if that year is a leap year.  

   1. To begin, design and implement the function so that it determines whether or not the year is evenly divisible by 4.
   2. Actually, century years (years divisible by 100) are an exception.  They are divisible by 4, but are **not** leap years. Update your function definition.
   3. Actually, there is one last exception: 4th century years (years divisible by 400) are leap years! Update your function definition one last time.

    You should test your function thoroughly, as it's a bit of a tricky cuss. You can find lists of leap years in various places, [like this one](https://www.pleacher.com/mp/mlessons/algebra/mobleap.html).

