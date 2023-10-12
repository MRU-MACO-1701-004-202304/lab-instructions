# Lab-13: More Decisions

**The risk of a wrong decision is preferable to the terror of indecision. (Maimonides)**

## Overview

This lab will give you further practice working with Booleans and decision structures.

You'll be practicing:

- Evaluating Boolean expressions.
- Creating a software solution involving decision structures for a simple problem.

## Python language focus

The focus of this lab will be on:

- Writing valid Python functions that involve decision structures.

## Do These Things

### Part 1: Code Analysis

1. Trace the code in `lab13_part1.py` and **predict** what the output will be when you run the program. 

2. Now run the code. If the output is not what you predicted, try to figure out why. If the output _was_ what you predicted, how confident were you of your answer? (_A lucky guess is in some ways worse than being certainly wrong._)

3. Without modifying `abstract_decisions`, determine how to make the program produce the opposite output by inverting the value of just one of the arguments passed from `main`. Make the change and test to see if you were correct.

4. Next, restore the code to its original form. Can you invert a different variable to achieve the same effect? If so, which one?	

---

### Part 2: Code Creation

_Meal delivery service BypassTheCleaning has hired you to write their app. They offer free delivery for orders of $40 or more, and they want your app to display the amount remaining to get free delivery._

1. Using the template provided in `lab13_part2.py`, **design** a program that prompts the user for the dollar amount of their current order, then prints out a message according to the following table:

    | Amount                   | Message                                                 |
    | ------------------------ | ------------------------------------------------------- |
    | amount $\lt 0$           | `Invalid entry, orders must be positive`                |
    | $0 \leq$ amount $\lt 40$ | `Add $xx.xx to your order to qualify for free delivery` |
    | amount $\geq 40$         | `You get free delivery!`                                |
    
    You can assume the user input data type is always correct (e.g. a number will be entered when it is expected by the program). You may add additional functions, but make sure that your `check_free_delivery` function header doesn't change and that it `print`s the appropriate message.

    The program should look like the following when run, where 25.30 is an examples of user input.

    <pre>
    What is the dollar amount of the current order? <span style="font-style: italic; font-weight: bold;">25.30</span>
    Add $14.70 to your order to get free delivery</pre>

    Note that by default, Python will not print out exactly two decimal places. This is a good chance to practice your [f-string](https://docs.python.org/3/tutorial/inputoutput.html#tut-f-strings) skills.

1. **Implement** the program from step 1. Is there anything you forgot during the design stage?
   > _Are there any magic numbers in your code? Can any of them become constants?_

1. Write down examples of amounts that could be entered when running your program to test all possible outcomes. Speaking of which...how many possible outcomes are there?

1. **Test** the program using the `test_free_delivery_selection_structure`, `test_constants`, and `test_formatting` automated tests in `test_lab13.py`. If you're not running green, determine why!

## Bonus challenge
In Part 2, you wrote a program to check if a user gets free delivery based on their order amount. Now, BypassTheCleaning wants you to make sure that only users within **20 km** get free delivery. 

1. Modify your `main` function to prompt the user for their delivery distance after getting the order amount.

1. Implement the `check_free_delivery_bonus` function to print messages according to the following table:

    | Distance                   | Message                                         |
    | -------------------------- | ----------------------------------------------- |
    | distance $\lt 0$           | `Invalid entry, distance must be positive`      |
    | $0 \leq$ distance $\lt 20$ | Check amount as before                          |
    | distance $\geq 20$         | `Sorry, you are not eligible for free delivery` |

    _Hint: you will want to call your working `check_free_delivery` function inside your `check_free_delivery_bonus` code somewhere. Where?_

1. Write down examples of distances and amounts that could be entered when running your altered program to test all possible outcomes. Speaking of which...how many possible outcomes are there?

1. **Test** the program using the automated `test_free_delivery_bonus_selection_structure` test in `test_lab13.py`.