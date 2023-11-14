# Lab-22: More File IO

**That's a wrap, folks!**

## Overview

Computers are really good at reading a bunch of data and summarizing it. For this lab, you'll be reading in a list of directions for a hike and calculating the total distance and the net distance ("as the crow flies"), then writing the results to a new file.

## Instructions

Open up `lab_22.py` and you'll see a few function definitions to complete. As usual, you may define additional functions as appropriate, but your main program entry point must be `main`. 

Your goal is to write a program that:
- Reads the text file `directions.txt` into a `list` of strings, one per line
- Calls `total_distance` to calculate the total distance of the hike
- Calls `net_distance` to calculate the net distance of the hike
- Writes the two distances to a file named `activity_log.txt`

Although you're only being asked to build 3 specific functions here, you would benefit by writing a number of additional helper functions as well!

### Input file format
The file `directions.txt` contains the data you will be reading. Each line has a **heading** (compass direction) and a **distance** in metres. The heading will be one of N (north), W (west), E (east), S (south). An example is as follows:

```plaintext
N    300
W    250
N    200
E    400
```

### Output file format
The output file `activity_log.txt` should contain the following text:

```plaintext
Total distance: xxxx
Net distance: xxx.x
```

where `xxxx` is a placeholder for the actual calculated numbers. If you choose not to implement one of the distance calculations, you may add a placeholder number such as 0, but make sure to include the text "Total distance" and "Net distance" on two separate lines.

### `total_distance` function
This function should:
- Take a list of directions as a parameter (one string per line)
- Calculate the sum of all the distances in the list, **ignoring heading**
- `return` the total distance 

> Hint: you will have to `split` the lines and cast the distances to a numeric data type before you can add them together

### `net_distance` function:
This one is considerably trickier! It should:
- Take a list of directions as a parameter (one string per line)
- Add up all the distances along the North-South axis, and all the distances along the East-West axis
- `return` the hypotenuse of the two distances

For example, for the list of distances given above:
- The North-South net distance is 500 metres
- The East-West net distance is 150 metres
- The hypotenuse of 500 and 150 is 522.0 metres

## Testing
Try to test your code first **before** running the automated tests - these should just confirm what you already know, not be used as a tool to exclusively check your work.