# Lab-05: Incan Gold

**Shall. We. Play. A. Game?**

## Overview

This lab and the next are meant to give you a taste of what it's like to program "for real". You'll be given a problem to solve (from an actual board game) and your job will be to understand the problem, design an algorithm, implement that algorithm as code, and test it out to make sure it "works".

## Assumptions

I'm assuming you've worked through, and are reasonably comfortable with, the topics and skills covered in prior labs and lectures.

## Python language focus

The focus of this lab and the next will be on:

- User input
- Data types
- Operators, especially `%` and `//`
- Formatted output via `f-Strings`

## Step 1: Understand the problem

There is a fun little game out there in the Real World called [Incan Gold](https://www.eaglegames.net/Incan-Gold-2018-p/102197.htm), where players explore a temple room-by-room and try to collect as many gems as they can...without dying horribly. 

Gems are split equally between each player in a given room, with any leftovers staying in the room. Because obviously temple raiders are nothing if not very polite. 

Your job is to create a small application that figures out how to properly split the gems in a given room equally between the players in that room - and also figure out how many gems get left behind.

#### before you just "dive in"

_Check your understanding of the problem by working through a couple of examples by hand, such as **11 gems and 4 players**, or **13 gems and 5 players**. Think of some other examples on your own as well - thinking of different data to test your algorithm is a vital skill in programming._

## Step 2: Design an algorithm

Write an algorithm that gets the **total number of gems** and **number of players** from a user, calculates **how many gems are received by each player** and **how many are leftover**, and then displays the results.

Write out the steps of the algorithm in pseudocode, as a flowchart, or in point form...whatever makes the most sense to you. Toss some numbers into your algorithm and make sure it behaves the way you want. (_People often skip this step because they think it's somehow a waste of time. They're very wrong - it's much easier to deal with issues in your algorithm **before** you implement it._) 

## Step 3: Implement your algorithm

Now that you have an algorithm (that seems to work, because you've tested it), you're ready to implement it: create a file in the root of your Codespace called `lab_05.py` - this is where your application code must go.

Did I mention that there's been a little wrinkle? Your boss just walked in and has given you a few restrictions - they want things to look "just right".

What does "just right" mean?

Well, the program should look like the following examples when run, with **bold text** representing user input:

#### example 1

<pre>
Enter the number of gems: <b>17</b>
Enter the number of players: <b>3</b>

Gems:            17
Players:          3
Gems per player:  5
Gems left over:   2
</pre>

#### example 2

<pre>
Enter the number of gems: <b>3</b>
Enter the number of players: <b>4</b>

Gems:             3
Players:          4
Gems per player:  0
Gems left over:   3
</pre>

#### warning 1

Your output is expected to be formatted *exactly* as shown: 2 spaces for the numbers column and 17 for the text column - and use the same text ("Gems:", "Players:", etc.)

[f-strings](https://docs.python.org/3/tutorial/inputoutput.html#formatted-string-literals) will be necessary, as they allow you to display text and numbers with a minimum character width. You can assume the number of gems will be either 1 or 2 digits.

#### warning 2

Remember, the `input` function always returns a **string** - you must cast the result to the appropriate data type.

## Step 4: Run some automated tests

This lab has 3 automated tests (as we did in Lab-03): one for the number of gems per player, one for the gems left over, and one for formatting.

The tests are located in `test_lab_05.py`, you can run the tests like you did in Lab-03.

**DON'T ALTER THE CODE IN THE TESTS, OR THINGS WILL BUST HARD!**

Try your best to get all 3 tests passing - but beware: tests that check formatting in general can be annoyingly picky!