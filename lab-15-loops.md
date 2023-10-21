# Lab-15: Loops

**"Repetition is the reality and seriousness of life." - Søren Kierkegaard**

## Overview

This tutorial is intended to get you used to designing loops and recognizing common patterns. 

In small groups, working on the whiteboard or paper, work through the following exercises. You can check your answers using the Python interpreter, but try to solve them by hand first.

## Python language focus

The focus of this lab will be on:

- Writing valid Python functions that involve repetition via the `while` loop.
- Reading valid Python functions that involve repetition via the `while` loop.

## Loop Design Steps

When you design loops, you **must** decide the following things:

1. **what** you want to repeat (i.e. what needs to go into the loop body)
2. what you will use as a **loop control variable** (or **LCV**)
3. what the **terminal condition** will be
4. how the LCV will be **initialized**
5. how the LCV will be **updated**

## Do These Things

### Part 1: Trace a loop

The following code fragment is supposed to add up all the multiples of five between 5 and 50 (inclusive), but it has two **logic** errors.

```python
sum = 0
count = 5
while count < 50:
   sum = sum + count
   count = count + 1

print("The sum is", sum)
```

1. Identify the:
   1. Body of the loop (statements to iterate)
   2. Loop Control Variable (LCV)
   3. Terminating conditions
   4. Initial conditions
   5. LCV update
2. Trace the code to see what it does. You need only trace enough to know what is happening, not every single iteration.
3. Describe what the code is actually doing.
4. Fix the code so that it actually sums the multiples of five between 5 and 50 (inclusive).

### Part 2: Design some loops

For each of the following, create and test an algorithm that solves the problem.

When you're convinced that your algorithm is sound, implement it using a Python `while` loop. Test your resulting code to make sure it works as expected.

1. Create a program that reads in 10 integers from the keyboard and prints out the sum of those integers. You can assume the user will enter valid input.
2. Create a modified version of the previous program that keeps reading integers until the user enters an empty string. After the empty string is read, the sum of the entered integers should be printed.
3. Create a program that reads in words from the keyboard until a word containing an exclamation mark is entered, at which point it should print out how many words were entered **and** how many of those words had at least one vowel (aeiou).
4. Create a modified version of the previous program; this time, report what the shortest word entered was. If there is a tie, the first word wins.

### Extra tracing practice

Consider the following Python code:

```python
choice = int(input("Enter a positive integer >= 2: "))
num_divisors = 0
possible_divisor = 2

while possible_divisor <= choice // 2:
    if choice % possible_divisor == 0:
        print("D", end="")
        num_divisors += 1
    else:
        print(".", end="")
    
    possible_divisor += 1

if num_divisors == 0:
    print(" prime!")
else:
    print(f" not prime ({num_divisors} divisors)")
```

#### Do the following:
   1. Identify the loop body.
   2. Identify the loop control variable.
   3. Identify its pre-loop initialization point.
   4. Identify the loop test.
   5. Identify the termination condition.
   6. State the termination condition for an input of 7.
   7. Identify the update of the loop control variable.
   8. State the loop's purpose.
   9. Trace the code for inputs of 11 and 12.