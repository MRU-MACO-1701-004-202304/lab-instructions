# Lab-19: Lists and Indexing

**You can't have one without the other.**

## Overview

This tutorial is intended to familiarize you with the `list` datatype and methods.

## List methods, functions, and operators
You may find the following methods or functions useful. For a given list `a_list`:

| Method or function                            | Description                                          |
| --------------------------------------------- | ---------------------------------------------------- |
| `a_list = [element0, element1, ... elementN]` | Initializes the list with any number of elements     |
| `a_list.append(element)`                      | Adds the element to the end of the list              |
| `len(a_list)`                                 | Returns the length of the list                       |
| `a_list.insert(i, element)`                   | Inserts the element between position `i` and `i + 1` |
| `del a_list[i]`                               | Removes the element at position `i`                  |
| `a_list.remove(element)`                      | Removes the first instance of `element`              |

Additionally, there are the following list operators:

| Operator            | Description                                                           |
| ------------------- | --------------------------------------------------------------------- |
| `a_list[i]`         | Accesses the element at position `i` (read or write, but must exist!) |
| `a_list == b_list`  | Evaluates to `True` if both lists contain the exact same elements     |
| `a_list + b_list`   | Concatenates the two lists together                                   |
| `a_list * N`        | Evaluates to a new list with `a_list` elements repeated `N` times     |
| `element in a_list` | Returns `True` if `element` is in the list                            |

## Do These Things

Do the following exercises in order.

### Exercise 1

Open `ex_1.py`, read the comments, and complete the code accordingly.

If your code is working correctly, it should behave something like this:

#### Example 1

<pre>
Enter the name of a course to add, or press Enter to finish: <b><u>COMP 1701</u></b>
Enter the name of a course to add, or press Enter to finish: <b><u>MATH 1505</u></b>
Enter the name of a course to add, or press Enter to finish:
2 courses added
</pre>

#### Example 2

<pre>
Enter the name of a course to add, or press Enter to finish:
no courses added
</pre>

#### Example 3

<pre>
Enter the name of a course to add, or press Enter to finish: <b><u>COMP3512</u></b>
Enter the name of a course to add, or press Enter to finish: 
1 course added
</pre>

---

### Exercise 2

Assume that your previous function returns the following list:
   ```python
   courses = [
      "COMP 1501", 
      "MATH 1505", 
      "GNED 1401", 
      "GNED 1103", 
      "MKTG 2150",
      "COMP 1502", 
      "COMP 2511", 
      "MGMT 3210", 
      "HRES 2170", 
      "GNED 1101"
      ]
   ```
   _You can split lists across multiple lines to enhance readability._

In `ex_2.py`, design a **function** that takes your course list as an argument and returns the course with the **highest course number**. For this example, the return value of your function should be the string `MGMT 3210`. If the course list is empty, the return value should be an empty string.

Assume there will always be a single space between the subject (COMP, GNED, etc.) and the course number.

Test your function with a variety of assertions.