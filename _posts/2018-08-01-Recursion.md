---
title: Recursions 
author: Maged Helmy
date: 2018-08-01 14:00:00 +0100
categories: [Blogging, Articles]
tags: [data_structure_and_algorithms]
---


Recursion: A recursion is where a function calls itself directly, or calls a function to call it directly. A recursive function can go infinite like a loop, therefore there must be 2 conditions.
The base criteria: There must be at least one base criteria or condition, such that, when this condition is met the function stops calling itself recursively.
The Progression Approach: The recursive calls should progress in such a way that each time a recursive call is made it comes closer to the base criteria.
Implementation: Recursion is implemented by means of stacks. The call stack holds the activation record on local variables, formal parameters, return address and all information passed to the caller function. When a function call itself, it suspends the execution temporarily and resume later when the execution control returns. The information is stored in the call stack.

Analysis of Recursion: Recursion makes a programmable more readable and is more efficient that iterations.
Time complexity: The number of times a recursive call is made is counted as 1. Therefore, recursion is O(n)
Space Complexity: The space complexity of recursive function may go higher than that of a function with iteration since it has to store all the data in every iteration.
Tower of Hanoi: is a puzzle which consists of three towers and atleast 3 rings. The minimal amount of moves required is 2^n -1. (insert python example)
Fibonacci: Fibonacci series generates the subsequent number by adding two previous numbers. (insert python example with iterative algorithm and recursive algorithm.








Investigate:
The following computer problems can be solved using Data Structures −
•	Tower of Hanoi
•	Fibonacci number series
•	Knapsack problem
•	All pair shortest path by Floyd-Warshall
•	Project scheduling
