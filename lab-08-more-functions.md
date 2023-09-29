# Lab-08: More Functions

**You can never have too many functions!**

## Overview

This lab continues in the same vein as lab-07. You'll be getting practice:

- Tracing and debugging a value-returning function.
- Writing a fairly complex value-returning function.

## Python language focus

The focus of this lab will be on:

- Reading Python code involving functions that use type hints.
- Writing valid Python functions that use type hints.

## Do These Things

### Trace and debug code that uses functions

You and a friend are developing a recipe app where the user enters ingredients and quantities in grams. Your friend started writing the code, but there's a mysterious bug that they've asked you to fix.

1. Open the file `ingredients.py` and inspect the function header of `add_ingredient`. What data types are should be passed as arguments? What type should be returned?
2. Trace the code **manually**. What data type is actually returned?
3. Run the code. Did it produce what you expected?
4. **Without modifying the `main` function**, fix the code so that it still prints the output, but doesn't print `None` anymore.

> _What do you think of `add_ingredient` as the function's name? Does it accurately indicate to the reader what it's doing?_

### Write a fairly complex function

As part of the same recipe app, we're going to add a new file named `cooking_time.py`. Eventually this will have a number of functions related to cooking times, but for now we're just going to calculate time to bake a cake.

1. Create a new file named `cooking_time.py` in the same folder as `ingredients.py`.

2. Define a new function named `cake_time` that takes the following **arguments** and returns the baking time **rounded up to the nearest minute**. Make sure to use descriptive variable names for your parameters.
   
   | Argument type | Description                 | Range     |
   | ------------- | --------------------------- | --------- |
   | `int`         | Oven temperature in °F      | 300 - 450 |
   | `float`       | Cake pan diameter in inches | 6 - 12    |

   The time to bake a cake is calculated as follows. (This is a completely made up formula. Cake results not guaranteed. :) )

   $$t = 20 + \frac{350 \times (area(d) - area(6))}{2 \times temp}$$

   where:
   - $t$ is the time being calculated
   - $area(d)$ is a function that calculates the area of a circle with a diameter $d$
   - $temp$ is the temperature in °F

   You will have to define and implement an `area` function as well as `cake_time`! Import the `math` library so you can use `math.pi` in this function. 
   
   I also haven't shown you how to round up, so you may have to do some research on this. Make sure to cite any sources used.

3. Create a standard `main` at the bottom of the file. In it, prompt your user to input the oven temperature and cake pan diameter.

   Assume that your user has no knowledge of the algorithm - you need to tell them what the numeric ranges are to avoid nonsensical values like 1000 °F! (_Note to those who've programmed before: you do NOT need to actually validate user input - just create a reasonable prompt._)

4. In `main`, call your `cake_time` function, passing in the user's input values to `cake_time`, and use the result to let the user know how many minutes the cake will require. 

5. At the bottom of the file, call `main`!

   Here's an example of what a fully functioning program might look like, where **bold** text indicates user input:

   <pre>
   Enter the temperature in °F (between 300 and 450): <b>350</b>
   Enter the cake pan diameter in inches (between 6 and 12): <b>8.5</b>
   Your cake should take about 35 minutes to bake.</pre>

## Run tests to check your work

This lab has 3 tests: One for the debugging problem, one for your `area` function, and one for your `cake_time` function. See if you can get all of them running green!
