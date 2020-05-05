---
title: Understanding Time and Space Complexity for Algorithm Performance
author: Maged Helmy
date: 2020-03-20 11:00:00 +0100
categories: [Blogging, Articles]
tags: [algorithmic thinking]
---
## Introduction

There can be several ways to implement a for-loop of an if-statement when programming in python. There are also several ways in which these algorithms can be designed to interact with each other. But how do we measure the performance of these different implementations ? This is where we consider the time complexity and space complexity of the algorithms implemented. In case of time complexity, this will specifically measure the impact of more data vs the time it needs to execute the function. In case of space complexity, this will measure the impact of more data vs the amount of memory required to execute the function. We take a look at three examples, the linear search, the quicksort and the mergesort. The goal of any algorithmic design is to have the shortest time and take the least amount of space as possible.

## Time Complexity
Time complexity quantifies the amount of time it takes by the algorithm to run as a function of its input length, n. The order of growth is the correlation between time and length of the input. If the length increases by x amount, how much more time does it take ?

The time complexity of an algorithm can be expressed using the following asymptotic notations.

O-notation: (pronounced “big-oh of g of n”): Denotes the asymptotic upper bound (An asymptotic line is a line that gets closer and closer to a curve as the distance gets closer to infinity.) for a given function.

\Omega()-notation: (pronounced “big-omega of g of n”): Denote the asymptotic lower bound for a given function.

\Theta()-notation:(pronounced “big-theta of g of n”): Denotes the asymptotic tight bound for a given function.

When considering time complexity, we look at the O-notation since it gives as the upper limit of execution. Generally, Big O Notation is the language we use to describe the complexity of an algorithm. Big O notation talks about how quickly the runtime grows in relative to the input. For instance, "runtime grows on the order of the size of the input O(n)" or "on the order of the square of the size of the input (O(N^2))"


## Space Complexity
Space complexity quantifies the amount of memory the algorithm needs to execute as a function of its input length, n. Space complexity includes both auxiliary space and space used by the input. Space complexity is commonly expressed using the Big O notation.

The auxiliary space is the temporary space the algorithm needs while getting executed.

## For the linear search:

Imagine we have 10 items and a target value that take certain amount of memory when the algorithm is running. Worse case, if we double our items to 20 items, then it will take double the time to execute the function. This means that the time taken is proportional to the amount of data. This is known as "Linear Time Complexity" - O(n). The amount of memory required does not change since we still hold one target value in the memory. Therefore, the amount of memory required stays constant regardless of the amount of data. Therefore, the linear search has a constant space complexity O(1). Other examples that have constant space complexity are the bubble sort, insertion sort and the selection sort.

For the Quick Sort: Quick sort is a divide and conquer algorithm which creates two empty arrays to hold elements less than the pivot value and elements greater than the pivot value, and then recursively sort the sub arrays. There are two basic functions, swapping items in place and partitioning a section of the array.

In worse case scenario, if you want to sort a list of 8 items, you need (7 + 6 + 5 + 4 + 3 + 2 + 1) which is a total of 28 comparisons for 8 items. What if we double the list to 16 ? then it will (15+14+.....) which is a total of 120. The relation between the amount of data and the amount of processing required is not linear, since when we double the input data, the number of processes increase. The time complexity is quadratic. O(n^2) (O - n squared) since if we double the amount of input data, the processing roughly quadruples. For space complexity, if we double the amount of data, we need the double amount of stacks to hold the data. Therefore, Quicksort has a linear space complexity O(n) since quicksort relies on recursive calls.

## Merge Sort
The input array is divided several times, sorted and then they are combined and merged back together. That is O(nlog(n)) in time complexity which is known as linearithmic. It is the same with best, average or worse scenario since the amount of operations are still the same. For space complexity, the number of levels represents the recursion, if we double the data, we need one more level of recursion, therefore, the stack will increase logarithmically. So the stack has O(log n) space complexity but the auxiliary array has O(n) linear space complexity, since you need temporary stacks to hold the array. Since linear complexity is bigger, than the space complexity of merge sort is linear.

## Summarize:

- Big O time complexity: Describes the impact of increasing the input data on the time taken for a program to running
- Big O space complexity: Describes the impact of increasing the input data on the extra memory needed by the program.
- Recursive algorithms require additional stack space for their processes.

Common way to talk about Big O notation:
- The function runs in O(1) meaning it has constant time in relative to its input
- The function runs in O(n) means in linear time where n is the number of items in the arrays
- The function runs in O(n^2) means it runs in quadratic time. For eg, nested for loops.
- Big O usually talks about the worse case scenario. But it is import to imply it when talking about Big O notation.
- Usually when we talk about space complexity, we're talking about additional space, so we don't include space taken up by the inputs
