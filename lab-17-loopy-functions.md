# Lab-17: Loopy Functions

**Round and round we go.**

## Overview

More loops. More functions. More fun.

## Do These Things

These exercises can be done in any order.  
I think they get progressively more challenging.

For each, create a value-returning function with type hints. Each function should use a `while` loop to get the task done.

### Exercise: Comma-separated Count Up

**Inputs**: an integer upper bound.

**Returns**: a string consisting of the numbers 0 through the upper bound (inclusive), each separated by a comma. There is no comma after the last number in the string! If the upper bound is less than 0, an empty string is returned.

**Assumptions**: you may assume only integers are passed to this function.

**Examples**

Your function should return:
- "0,1,2,3,4" if given `4` as input
- "0" if given `0` as input
- "" if given `-3` as input

---

### Exercise: Comma-separated In-between

**Inputs**: integer upper and lower bounds.

**Returns**: a string consisting of the numbers from the upper bound to the lower bound (inclusive on the upper end, but exclusive on the lower end), each separated by a comma. There is no comma after the last number in the string! If the lower bound is greater than the upper bound, or if both bounds are equal, an empty string is returned.

**Assumptions**: you may assume only integers are passed to this function.

**Examples**

Your function should return:
- "4,3,2,1" if given `4,0` as input
- "-3" if given `-3,-4` as input
- "" if given `5,8` as input
- "" if given `-1,-1` as input

---

### Exercise: Alternating Case String In-between

**Inputs**: 2 strings, each of length 1.

**Returns**: a string consisting of the letters strictly between the two strings provided. If there are no such letters, return the empty string. As an extra wrinkle (sorrynotsorry), the letters in the resulting string should alternate between lower and uppercase.

**Assumptions**: you may assume only single-character strings in the range `a` to `z` are passed to this function. You may also assume the first string provided comes before (or is the same as) the second.

**Examples**

Your function should return:
- "bC" if given `a,d` as input
- "bCdEfG" if given `a,h` as input
- "b" if given `a,c` as input
- "" if given `b,b` as input
- "" if given `b,c` as input

**Hint**: you will have to use the built-in functions `str`, `ord` (seen before in lab-14) and `upper` to complete this task. 

---

### Exercise: Interval Validator

**Inputs**: a prompt, an integer lower bound, an integer upper bound

**Behaviour**: prompts the user for a number between the lower and upper bounds, inclusive. Validates any number entered by the user - if it's out of range, re-prompts the user and gets another number. Keeps doing this until an in-range number is entered.

**Returns**: an integer between the lower and upper bounds, inclusive on both ends.

**Assumptions**: you may assume the lower and upper bounds are both integers, and that the lower bound <= the upper bound.

**Examples**

Let's assume you've named your function `foo` (don't do that). Also assume we've got a `main` like this:

```python
def main() -> None:
    valid_num = foo("Enter a number", 1, 6)
    print (f'''You entered {valid_num}. That's valid.''')
```

Then here's something that could happen if `main` was called:

<pre>
Enter a number between 1 and 6: <b>0</b>
Enter a number between 1 and 6: <b>7</b>
Enter a number between 1 and 6: <b>6</b>
You entered 6. That's valid.
</pre>
