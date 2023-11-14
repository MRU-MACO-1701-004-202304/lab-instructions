# Lab-21: File IO

**The lowly text file is a mighty useful thing.**

## Overview

This lab will have you reading through text files and processing the data therein in some way. It's kinda neat how you can do this.

## Before You Begin

The file `trick-or-treat.txt` contains counts of numbers of trick or treaters for 100 households over one Halloween night. Each line in the file contains a single integer.

Note where the file is located in your Codespace's directory structure. This will be important.

You should also take a look at the file; in fact, getting into the habit of looking through data files ahead of time is very, very useful habit.

## Do These Things

Do the following exercises in order.

### step-01: extract file data into a list

Write a Python function that takes in the name of a file with trick or treater data and returns that data as a **list of integers**. 

Remember, to read from a file, we follow these general steps:
   1. Open the file object  
      _Remember that the file path is relative to your **current working directory**_
   2. Read the file and do processing
   3. Close the file object

Test your function out by calling it with the data file you've been given and then examining the resulting list (via a `print` or in the debugger are probably the easiest ways to do this). Do you see the results you expect?

---

### step-02: ponder error handling

The following errors are commonly encountered with file input. Think about how you might approach dealing with these issues.

1. Open `trick-or-treat.txt` in a text editor and add an **empty line** somewhere in the middle. What happens? What changes could you make to your function to deal with this problem?
1. Now, modify one of the lines of `trick-or-treat.txt` so that it has a `float` instead of an `int` (e.g. change `30` to `30.0`). What kind of error occurs this time? How would you deal with it?
1. Finally, modify `trick-or-treat.txt` so that it has **two numbers** on one line. What kind of error happens this time? How would you handle this unexpected input?

---

### step-03: work with the data

Now that you have a solid way of getting a list of trick-or-treat data from a file, you can do all sorts of things with that data. 

Create 4 well-named functions that take in the list from step-01 and return the following things:
   1. The **highest** number of trick-or-treaters
   2. The **average** number of trick-or-treaters
   3. The number of households with **over 100** trick-or-treaters
   4. The number of households with **exactly 21** trick-or-treaters

You should try to get at least **two** of these functions done during the lab.

_Each of these functions will look similar with an **accumulator loop**. For the purposes of this exercise, do not use Python's built-in functions or methods like `max`, `count`, or `sum`! Build those coding muscles._

#### Testing your functions

It'd be great to test your functions, right? But how? Doing all the work by hand seems onerous - because it is.

I have 2 suggestions:
1. Create a smaller file that has a much smaller number of numbers in it. Then you _can_ do the work by hand. If your code works for a few things, it should work for a larger number as well.
2. Use a spreadsheet like Google Sheets or Excel to test your work. You can copy and paste the numbers into the spreadsheet and do the calculations you need pretty easily.

