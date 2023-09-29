# Lab-07: Functions

**Come - join the Function Fan Club!**

## Overview

Functions are incredibly, incredibly useful things. They _do_ have one downside, though - tracing code that involves functions can definitely be a bit tricky...but you have to learn how to do it!

This lab will have you:
- tracing code that uses functions
- debugging code that uses functions
- creating valid Python functions that perform specified tasks

## Python language focus

The focus of this lab will be on:

- Reading Python functions, including functions involving `type hints` (a.k.a. `type annotations`)
- Writing valid Python functions that use type hints.

## Do These Things

### Trace code that uses functions

With a partner or small group, work through the following problems **by hand**.  (Yes, you can work alone...but maybe take this opportunity to get out of that comfort zone a bit?)

#### problem 1

Here is a program:

```python
def test(a: int, b: int, c: int) -> None:
    print(a, b, c)

def main() -> None:
    a = 1
    b = 2
    c = 3
    test(a, b, c)
    test(b, a, c + 7)

main()
 ```

1. Identify the following items in the program:

    - function headers
    - function bodies
    - function definitions
    - function calls
    - function arguments
    - function parameters
    - local variables

2. Fill in the table below with the values of the parameters `a`, `b`, and `c` *inside* the `test` function for each of the two function calls:

    | Call to `test` | `a` | `b` | `c` |
    | -------------- | --- | --- | --- |
    | First call     |     |     |     |
    | Second call    |     |     |     |


#### problem 2

Trace the following program. Show the values assigned to each local variable and parameter in `main` and `display`, then write the program output.

```python
def display(a: int, b: int) -> None:
    c = 2 * a + b
    print (a, b, c)

def main() -> None:
    n = 3
    display(5, n)
    display(n, n)
    display(n * n, 12)

main()
```

After - and only after! - you do this, run the script in your Codespace to see if your trace's expected output matches the actual output.

> _You might be thinking "Hey, these aren't descriptive variable names!". You would be correct. These are nonsensical little programs where I want you to focus on the variable **scope** and values - what the function is doing is actually not particularly relevant._

---

### Debug code that uses functions

The following programs do not work. See if you can find out why!

#### buggy program 1

This program _should_ greet a person between 1 and 10 times. It uses the `random` module to determine how many times (the use of the `random` module is not the part that is broken). Alas, this code is busted!

```python
import random

def greeting(name: str) -> None:
    n_times = random.randint(1, 10)
    print(f"Hello, {name}! " * n_times)

def main() -> None:
    name = input("What is your name? ")
    greeting()

main()
``` 

1. Read the code and see if you can spot the single issue it has. Don't skip this step, because this is a kind of thing you'll be doing on your written tests with no computer in sight to help!

2. Now create a Python file in your Codespace and paste the code into it. Run the program to see if your hypothesis from step 1 is correct or not.

3. Fix the problem and confirm that your fix worked!

#### buggy program 2

This program _should_ display the hypotenuse of a right-angle triangle, given one angle in degrees and the length of the side opposite the angle. Unfortunately, it's got a few issues.

```python
def hypotenuse(angle: float, side: float) -> None:
    hyp = side / math.sin(math.radians(angle))
    print(f"The hypotenuse is {hyp:.2f}.")

def main() -> None:
    angle = float(input("Enter the angle in degrees: "))
    side = float(input("Enter the length of the opposite side: "))
    hypotenuse(side, angle)

main()
```

1. Read the code and see if you can spot the issues: there are two. Don't skip this step, because this is a kind of thing you'll be doing on your written tests with no computer in sight to help!

2. Now create a Python file in your Codespace and paste the code into it. One of the errors should jump out at you now (look at those  squiggles in the editor!), while the other is more...subtle. 

3. Fix the obvious issue and confirm that the code is, indeed, misbehaving by finding an example of inputs that produce incorrect outputs. (This will mean doing the math by hand, yes. Welcome to programming.)

4. Use those inputs to trace the code to figure out what is wrong.

5. Fix the issue and confirm your fix worked!

---

### Design some functions

Try planning out the following exercises by hand, _then_ implementing them in Python scripts. Remember, you need to both **define** and then **call** your functions, preferably from a `main` function - use the code examples earlier in this lab as a reference.

#### problem 1

Design a function to compute and display the annual rate of inflation for a given item. The function is passed two prices for the same item: the price one year ago and the price today. The inflation rate should then be displayed as percentage with one decimal place (e.g. 5.3%). 

Here are the steps you should take to develop this - and **any** - function:

1. Ensure you understand what the function is supposed to _do_. What _inputs_ does it need for that? What - if anything - should it _return_? What - if anything - should it _output_? (Remember that **output** and **return** are DIFFERENT THINGS!)
2. Develop an *algorithm* that will make the function behave in the desired way.
3. Write the function definition, implementing the algorithm in the function body.
4. **Test** your function by calling it with some test values that you've chosen - make sure you clearly understand what the result of the calls should be! 

    _For example, if we wanted to use our function to calculate the expected inflation rate for a car that cost $20,000 last year and $23,000 today, what is the expected result? Does the function you've created deliver that result?_

#### problem 2

Following the same strategy as above, design a function which, given three sides of a triangle $a$ $b$ and $c$, computes and displays the area of the triangle. The area can be calculated using Heron's formula:
    
$$A = \sqrt{s(s - a)(s - b)(s - c)}$$

where $s$ is the semiperimeter of the triangle:

$$s = \frac{a + b + c}{2}$$

You will likely find it useful to create TWO functions here, one for the area and one for the semiperimeter.