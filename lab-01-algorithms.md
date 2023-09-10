# Lab-01: Algorithms

**The ability to create algorithms is fundamental to programming.**

## Overview

You won't be programming in Python for this lab (don't worry, you will be soon enough). Instead, you'll be practicing writing some algorithms.

So why use a Codespace at all? To practice, practice, practice.

## Assumption

I assume you've successfully completed [Lab-00: Hello, Codespaces](https://github.com/MRU-MACO-1701-004-202304/github-classroom-content-links).

If that's not the case, complete that lab before starting this one.

## Do These Things

### Step 01: Get the content for this lab

Get the content for this lab from the GitHub Classroom content page for our course. _I'm not linking to it on purpose, as I'd like you to remember on your own where to find it._

Don't forget to "star" your resulting repo. _Why should we do that?_

### Step 02: Open the content in a Codespace

The resulting Codespace is super-boring. But you're about to change that.
 
### Step 03: Create a file on your Codespace to hold your work

1. Create a file called `exercises.txt` in your Codespace. I won't tell you exactly how to do this, but I'll give you a hint: you'll need to start by clicking on the Explorer icon in your Codespace:
   
    ![explorer icon](./images/lab-01-explorer-icon.png)

    _After you get into the Explorer, there are a couple of ways to create your new file. You could look for some promising-looking icons, or - my favorite habit - right-click and see what happens._

### Step 04: Type up your answers to the following exercises

Now you have a file to put stuff into. Let's put stuff into it.

In `exercises.txt`, put your answers to the following exercises, labelled in a way that a rational human could find them.

---

#### exercise-01

Assume we're living in an alternate reality where the only currency are pointy rocks, chickens (worth 11 pointy rocks), and 10-dollar bills (worth 2 chickens).

Using pseudocode, write a currency conversion algorithm that asks for the number of chickens and bills being received and outputs how many pointy rocks should be provided in exchange.

**After you're done this exercise, push your work as you did in Step 4 of lab-00.  Use a helpful comment ('Complete exercise 1', for example.) Doing these pushes as you work - especially while you're coding - is a very important habit to get into.**

---

#### exercise-02

You have created a new animal, called a **Doggo**, that's like a dog but marginally smarter - smart enough to follow simple algorithms.

Doggos understand the following commands: `BARK`, `ROLLOVER`, and `BLOVIATE`.  
A human can interact with a Doggo by clapping at it; the Doggo can count these claps.

Using pseudocode, create an algorithm for a Doggo that would make it behave in the following way when interacting with a human:

| number claps heard by Doggo | Doggo response |
| :-------------------------: | -------------- |
|              1              | BARK           |
|              3              | ROLLOVER       |
|              4              | BLOVIATE       |

**After you're done this exercise, push your work.**

---

#### exercise-03

You have created a new animal, called a **Kitteh**, that's like a cat but...well, I'm not sure how intelligent cats are, because they play their cards pretty close to the chest. But I digress. Kittehs can understand algorithms for sure.

Kittehs understand the following commands: `NYAA`, `SCARF`, `SIGH`, and `DOZE`  
A human can interact with a Kitteh by offering it treats; the Kitteh can weigh these treats.

Using pseudocode, create an algorithm for a Kitteh that would make that Kitteh behave like this when it approaches a human victim:

_NYAA at the human to gain its attention. If offered a treat of the "right" weight (more than 5g and less than 8g), SCARF the treat. If offered a treat of the "wrong" size, SIGH. If 4 treats of the right size have been SCARF'd, then DOZE; otherwise, continue the process._


> Aside: I first encountered the words **Doggo** and **Kitteh** in the card game [Trash Pandas](https://gamewright.com/product/Trash-Pandas) by Gamewright Games.

**After you're done this exercise, push your work.**

### Step 05: Confirm you pushed

I'd suggest using the method provided in our [Boatload](https://docs.google.com/document/d/1m42bfAUVuybxIFOoW0vJ5ZyR-WOJWwCZ9KhP0iOCGOE/edit#bookmark=id.956mn4x49etk) document.


---
  
---



# Want some more practice?

Here are some additional exercises you can try.

## Additional Exercises
1. Otto the robot is not very smart.  In fact, his knowledge base includes only five instructions.  However, he can follow any sequence of instructions and does exactly what he is told, as long as they are known instructions.  He executes instructions in sequential order.

    Otto's knowledge base ("Otto language") consists of the following instructions:

    | Instruction                     | Details                                   |
    | ------------------------------- | ----------------------------------------- |
    | Stand up                        | must be sitting                           |
    | sit down                        | must be standing                          |
    | take a step                     | takes one step forward – must be standing |
    | turn                            | turns right 90 degrees – must be standing |
    | repeat x times  [ instruction ] | x must be a positive whole number         |

    Assumptions:
    - Otto starts in a **seated position**.
    - Otto must end in a seated position in the same chair.

    1. Write a sequence of instructions which direct Otto to walk forward five steps and then return to his resting state.

    2. Write a sequence of instructions which direct Otto to walk in a square which is three steps on each side.  All turns are left-hand turns.

2. In pseudocode, write an algorithm which reads a four-digit positive integer, and writes the number which is formed by placing the ones digit in the tens column and the thousands digit in the ones column. For example, if the input is 8052, the output is 28. If the input is 1234, the output is 41.

    You may assume the following arithmetic operations are available: +, –, ×, div and mod. "x div y" gives the whole quotient of x ÷ y, whereas "x mod y" gives the remainder.

3. In pseudocode, design an algorithm which reads a sequence of one or more numbers, and determines how many of the numbers in the list are larger than the first.

4. Pretend that you are designing "Otto v2.0".
   1. Can you think of a useful modification to his current knowledge base, to shorten programs like the solution to 1a)?
   2. Re-write your solution to 1 b) for Otto 2.0 using your proposed modification.
   3. Can you suggest any other useful features to add to Otto v2.0's language?
   4. Otto lacks a decision making instruction.  Pretend that Otto v2.0 will be equipped with a proximity sensor.  This will enable him to sense whether or not he's too close to an object to take a step forward.  Design one or two instructions to add to his knowledge base so that an Otto programmer could make good use of them
   
5. In pseudocode, design an algorithm which will read three numbers and determine which is the largest and which is the smallest.