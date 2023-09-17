# Lab-04: Operators

**Not terribly _exciting_, perhaps...but terribly _useful_.**

## Overview

Python (and most other programming languages) use a variety of mathematical operators. Some of them are going to be familiar to you - but some of them are going to be a bit "huh?" when you first encounter them. This lab gives you the opportunity to read and write code using these operators.

### The Python math operators

| Name                 | Operator | Precedence | Example                        | Math equivalent                 |
| -------------------- | -------- | ---------- | ------------------------------ | ------------------------------- |
| Parentheses/brackets | `()`     | 1          | `x = (2 + 3)/2` <br> `x = 2.5` | $x = \frac{2 + 3}{5}$           |
| Exponentiation       | `**`     | 2          | `x = 3 ** 2` <br> `x = 9`      | $x = 3^2 $                      |
| Multiplication       | `*`      | 3          | `x = 3 * 2.5` <br> `x = 7.5`   | $x = 3\times 2.5 $              |
| Division             | `/`      | 3          | `x = 5 / 2` <br> `x = 2.5`     | $x = \frac{5}{2} $              |
| Integer Division     | `//`     | 3          | `x = 5 // 2` <br> `x = 2`      | N/A - round down after dividing |
| Modulo               | `%`      | 3          | `x = 5 % 2` <br> `x = 1`       | N/A - remainder after dividing  |
| Addition             | `+`      | 4          | `x = 2 + 2` <br> `x = 4`       | $x = 2 + 2 $                    |
| Subtraction          | `-`      | 4          | `x = 5 - 6` <br> `x = -1`      | $x = 5 - 6 $                    |

*Python follows the same precedence as standard math (BEDMAS). When two operators of the same precedence are on the same line, the operation happens from **left to right**.*

And now that you've started writing "real" code, that means you're ready to practice _tracing_ "real" code. I can almost _feel_ the joy emanating from the very core of your being!

## Assumptions

Besides the usual Codespace assumptions, I'm assuming you are comfortable with basic math concepts and terminology, and also know how to start a Python REPL session.

## Do These Things

### Step 01: Get ready to code

Create the Codespace for this lab as you've done for prior labs.

### Step 02: Do the following exercises

#### exercise-01: evaluate expressions w/ familiar operators

1. Evaluate these expressions by hand. Feel free to use paper, the whiteboard, or a text document.

    ```python
    2 * (20 / 4 + 1) + 5
    4 * 3 / 6
    4 / 6 * 3
    3 * 4 / 6
    ```

2. Use Python's REPL to check your work. If you find that you evaluated something incorrectly, **figure out why**. Don't ignore this step.

3. If you feel that any of the expressions are confusing due to order of operations, rewrite them with brackets to be less confusing.

_BTW - don't skip part 1 and just type the expressions into the REPL. If you do that, you're just being a code monkey. And you're going to set yourself up to be totally lost on the written exams you'll be writing._

---

#### exercise-02: evaluate expressions with `//` and `%`

Now repeat the steps in exercise-01 with these expressions: 

```python
4 // 6 * 3
3 * 4 // 6
7 % 3
4 + 7 % 3 - 5
(4 + 7) % 3 - 5
```

---

#### exercise-03: evaluate expressions containing variables

Assume we have the following variable definitions: 

```python
x = 2.5
y = -1.5
m = 18
n = 4
```

Repeat the steps in exercise-01 using the following expressions:

```python
x + n * y - (x + n) * y
m // n + m % n
5 * x - n // 5
1 - (1 - (1 - (1 - (1 - n))))
```

---

#### exercise-04: translate "standard" math expressions to code

**By hand**, write Python arithmetic expressions for each of the following. Assume the variables have already been declared and assigned. 

1. $A + \frac{B}{C + D}$
2. $(X - 1)(Y -4)$
3. $\frac{-B + X}{2A}$
4. $XY^2Z$

How would you check if your expressions are correct? Do that!

---

#### exercise-05: trace "real" code

For each of the following code snippets:

1. If you're able to, predict what will be printed to the screen when the snippet runs by "running" the code in your head. This might be too challenging at this point in your learning. If it is, or if you're not confident about the result, instead do a code trace in your instructor's preferred format. You should include all variables (with all intermediate values), as well as any output.

2. Check your prediction (or trace) by running the snippet in your Codespace. If you weren't correct, can you see why? If not, ask your instructor, because you've missed something!

_If all you're doing for this question is just running the code and not predicting anything, you're being incredibly short-sighted and definitely setting yourself up for failure._

##### snippet 1
```python
freeze = 32
boil = 212
freeze = 0
boil = 100

print(freeze)
print(boil)
```

##### snippet 2
```python
doughnuts = 6
friends = 3

print("We all get", doughnuts/(friends + 1), "doughnuts.")
```

##### snippet 3
```python
doughnuts = 6
friends = 3

total_peeps = friends + 1
whole_doughnuts = doughnuts // total_peeps
leftover = doughnuts % total_peeps

print("We all get", whole_doughnuts, "whole doughnuts!")
print("There are", leftover, "doughnuts left over.")
```

##### snippet 4
```python
beta = 9
alpha = 3 * beta
print(alpha, ",", beta)

alpha = alpha + 1
print("alpha,beta")

beta = beta + beta
print(alpha, ",", beta)
```

### Step 03: Push the work on your Codespace to the org repo

### Step 04: Confirm you pushed