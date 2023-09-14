# Lab-02: Tracing

**Being able to _trace_ code & algorithms is arguably more important than being able to _write_ code & algorithms.**

## Overview

Most of your time spent as a developer will be spent reading code; and a good chunk of _that_ time will be spent tracing that code. So here are some exercises for you to practice developing that vital skill.

## Assumption

I assume you've successfully completed prior labs to the extent that dealing with Codespaces and the editor at this point is _fairly_ comfortable.

## Do These Things

### Step 01: Get the content for this lab

### Step 02: Open the content in a Codespace
 
### Step 03: Create a file on your Codespace to hold your work

1. Create a file called `exercises.txt` in your Codespace.

### Step 04: Type up your answers to the following exercises

In `exercises.txt`, put your answers to the following exercises, labelled in a way that a rational human could find them.

#### exercise-01

Examine the following algorithm:

```
ask user for number

set under = number - 1
set over = number + 1

write "{number} is between {under} and {over}"
```

1. Trace the algorithm, assuming the user enters 9. Make sure you show the state of all variables and also show the output.

#### exercise-02

Examine this algorithm:

```
ask user to enter their name

set length = number of letters in name

response = "long"

if length <= 3 then
    response = "very short"
else if length <= 6 then
    response = "pretty short"
else 
    response = "pretty long"

output "That's a {response} name!"
```

1. Trace the algorithm, assuming the user enters 'Augusto'. Make sure you show the state of all variables, as well as the output.
2. Trace the algorithm again, assuming the user enters 'Fumiko'. Make sure you show the state of all variables, as well as the output.
3. Briefly explain in English what the purpose of this algorithm seems to be.

#### exercise-03

Examine this algorithm (it was used in A1 last year and was partially completed in lec-02):

```
ask user for number
set small = number
set large = number

ask user for another number
while user provides a positive number
    if number > large
    then
        set large = number
    otherwise
        if number < small
        then
            set small = number
    
    ask user for yet another number

share with user (large - small)
```

1. Trace the algorithm, assuming the user provides these 5 numbers: 4, 6, 11, 3 and -2 when asked to by the algorithm. Express the state of all variables at each step, as well as the final output.
2. In grammatically complete sentences, express the purpose of the entire algorithm. Not what each step produces, but rather, describe the original problem the programmer intended to solve.

### Step 05: Push the work on your Codespace to the org repo

The process is the same as you did in Step 4 on the last lab.

### Step 06: Confirm you pushed
