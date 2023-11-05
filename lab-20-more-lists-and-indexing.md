# Lab-20: More Lists and Indexing

**You didn't actually think this was over, did you?!?

## Overview

This lab continues with our work started in lab-19.

## Do These Things

Do the following exercises in order.

### Exercise 1

Building on the course management program introduced in lab-19, someone has written a function called `remove_all`. It is supposed to remove all courses matching a certain course code, but it is not working as expected.

Open the file `lab20_part1.py` and read the function. Then do the following:

1. Trace the function with the following function calls:
    ```python
    courses = ["COMP 1501", "GNED 1103", "GNED 1401", "MATH 1505"]
    remove_all(courses, "GEOL")
    remove_all(courses, "MATH")
    remove_all(courses, "GNED")
    ```
2. Does an error occur every time you call the function? If not, under what circumstances does the error occur? What *kind* of error occurs? The general error types are syntax, runtime, and logic.
3. Try to fix the function so that it behaves as intended. What additional test values should you consider to fully ensure the function is working as expected?

_Note: this is a deceptively challenging problem! If you do your trace carefully, you should find out what the problem is quickly. Fixing it, however, can be tricky!_

---

### Exercise 2

Assume you have two lists of **integer** quiz grades (0 - 100) for a class of students, `quiz1` and `quiz2`. Both lists have an equal number of elements. The first entry in each list is the mark for student 1, the second entry in each list is the mark for student 2, etc.

In `lab20_part2.py`, create a function called `best_quiz_grade` that takes the two lists as input and returns a *third* list containing the higher of the two quiz grades for each student. 

You can assume that the two lists are the same length and that each contains only valid numbers.