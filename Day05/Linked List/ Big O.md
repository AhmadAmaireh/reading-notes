## ## Big O: Analysis of Algorithm Efficiency

Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

Running Time (also known as time efficiency / complexity)
The amount of time a function needs to complete.

Memory Space (also known as space efficiency / complexity)
The amount of memory resources a function uses to store data and instructions.

## Overview
Big O’s role in algorithm efficiency is to describe the Worst Case of efficiency an algorithm can have in performing it’s job. It specifically looks at the factors mentioned above, which we often refer to as Space and Time. In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:

## Input Size
Units of Measurement
Orders of Growth
Best Case, Worst Case, and Average Case
Input Size
Input Size refers to the size of the parameter values that are read by the algorithm. This does not simply refer to the number of parameters an algorithm reads, but takes into account the size of each parameter value as well.


## Units of Measurement
To evaluate a function for Time and Space complexity, we need a way to measure each of these factors.

In order to quantify the Running Time in our analysis, we will consider Three Measurements of time:
The time in milliseconds from the start of a function execution until it ends.
For the purposes of Big O, we won’t be considering this measurement since different machines will have different individual run times depending on how powerful they are. Regardless, this will always be a measurement of run-time.

The number of operations that are executed.
Think of this as the number of lines of code that are executed from start to finish of a function.

The number of “Basic Operations” that are executed.
“Basic Operation” refers to the operation that is contributing the most to the total running time. This is usually the most time consuming operation within the inner most loop.

In order to quantify Memory Space, we can consider Four Sources of Memory Usage during function run-time:
The amount of space needed to hold the code for the algorithm.
Think of this as the number of bytes required to store the characters for the instructions specified in your function.

The amount of space needed to hold the input data.
If direct input data is not considered, we may just refer to this as Additional Memory Space since not all functions have direct input values.



## Orders of Growth
We can describe overall efficiency by using the input size n and measuring the overall Units of Space and Time required for the given input size n. As the value of n grows, the Order of Growth represents the increase in Running Time or Memory Space.

![Orders of Growth](./OrdersOfGrowth.png)

## Worst Case, Best Case, Average Case

- Worst Case: The efficiency for the worst possible input of size `n`

- Best Case: The efficiency for the best possible input of size `n`

- Average Case: The efficiency for a “typical” or “random” input of size `n`.

![Basic asymptotic efficiency of code](./Basic%20asymptotic%20efficiency%20of%20code.png)