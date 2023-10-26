# Lab-12: Decisions

**Do or do not.**

## Overview

This tutorial is intended to get you used to working with simple and compound decisions.

## Python language focus

The focus of this lab will be on:

- Reading and understanding Python code that uses decision structures.
- Writing valid Python decision structures.

## Do These Things

### Part 1: Working with Simple Decision Structures

#### Exercise

Write an algorithm that prints risk when the value of a variable named pressure is above 160, otherwise it prints no risk. 
What test values would you use to ensure your algorithm is correct? Don't skip this.

#### Exercise

1. Trace the following code segment and write the final value of result for the given input values.

    ```python
    result = 10
    total = float(input("Please enter the total: "))
    if total > 100:
        print("Total is", total)
        result = 25
    else:
        print("Total is", total)
        result = 80

    print("Result is", result)
    ```

    | input | result |
    | ----- | ------ |
    | 100   |        |
    | 155   |        |
    | 80    |        |

1. How could the previous program be made simpler without changing its behaviour?

---

### Part 2: Working with Complex Decision Structures

#### Exercise

1. Write a **Python function** that takes 3 integers representing dice rolls as inputs. If all 3 are the same value, return `"3 of a kind!"`. If 2 are the same, return `"A pair!"`. Otherwise, return `"Roll again"`. To check your results, trade answers with another group and trace their code.

    Try this on paper first, to practice what you'll be experiencing on your written exams.

    Use the following incomplete program to get you started:
    ```python
    def roll_results(                              ) -> str:
        """

        """
    ```
1. Choose inputs that will test your program - make sure you create enough test inputs that you're sure each possible outcome is correctly returned. Test your "paper code".

1. Create a script in VS Code and add your code plus the following `main` to it. Does the script run as expected? Fix any issues you encounter!


    ```python
    import random

    # Add your roll_results() function here.

    def main() -> None:
        a = random.randint(1, 6)
        b = random.randint(1, 6)
        c = random.randint(1, 6)
        result_str = roll_results(a, b, c)
        print(f"You rolled {a}, {b} and {c}. {result_str}")

    main()
    ```

#### Exercise

1. Design an **algorithm** for the following problem:

    Get the GPA of a student from the keyboard, then print a message dependent on the value of the GPA:

      | GPA        | Message                                        |
      | ---------- | ---------------------------------------------- |
      | 3.0 to 4.0 | Keep up the great work!                        |
      | 2.0 to 2.9 | Room for improvement, but you're getting there |
      | 1.0 to 1.9 | You're falling behind, is everything okay?     |
      | 0.0 to 0.9 | :(                                             |

    _If the user enters a number above 4.0 or below 0.0 the algorithm should display the message `Invalid Input`._

1. Choose a variety of test data that would confirm that the algorithm handles all desired outcomes.

1. Enter your algorithm as a script in VS Code and use your test data to confirm it's working as expected.

#### Exercise

A mythical country has the following tax structure:

| Tax rate | No dependents        | Dependents           |
| -------- | -------------------- | -------------------- |
| 0%       | Less than \$20,000   | Less than \$40,000   |
| 10%      | \$20,000 to \$60,000 | \$40,000 to \$60,000 |
| 20%      | \$60,000 and over    | \$60,000 and over    |

Write a **Python program** that asks how many dependents the user has and how much money they made, then prints out the amount of tax owing. 

How would you test whether this program is working correctly?

Compare your solution to the problem with other folks in your lab. How many different solutions do see? Can you think of other ways of simplifying your code?