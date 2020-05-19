---
title: Intro to Algorithms
author: Maged Helmy
date: 2018-02-01 14:00:00 +0100
categories: [Blogging, Articles]
tags: [Tutorial]
---

## Algorithms

When starting with any problem to solve. Clearly have the input stated and the output stated. Also, right down any edge cases as part of the input. The algorithm bridges the input with the output. The algorithm is a step-by-step procedure which defines the instructions to be executed in an order to get a desired output.


--------------------------------------------------
Greedy Algorithms: It solves the problem by making a local optimal choice at each stage with the hope of finding a global optimum.
--------------------------------------------------

Divide and Conquer Algorithms: The problem is divided into smaller sub-problems and then each problem is solved independently. When we keep on dividing, it will reach into a stage where it cannot be divided anymore. It is recursive by nature. When you break the problem, it essentially remains the same. The solution of all sub-problems is merged in order to obtain the solution of an original problem. Examples include merge sort, quick sort, binary search, closest pair.
Dynamic Programming: Similar to divide and conquer in breaking down the problem into smaller problems. But unlike divide and conquer, these sub-problems are not solved independently, but rather it looks at will examine the results of the previously solved sub-problems. The solutions of sub-problems are combined in order to achieve the best solution. It makes it efficient by storing intermediate results. It uses memoization.  A good example is Fibonacci where it has several recursion calls. The idea of dynamic programming is to reduce function calls of same methods. By storing the result of the function, we do not call it again. Using dynamic programming on Fibonacci, greedy algorithm is O(2^n) while dynamic programming is O(n). This technique of storing the results of already solved subproblems is called Memoization.
There are two methods:

1)	Top-down with Memoization: This approach tries to solve the bigger problem by recursively finding the solution to smaller sub-problems. Whenever we solve a sub-problem, we cache its resuls so that we don’t end up solving it repeatedly if it is called multiple times later. Instead, we return the saved results. This technique of storing the results of already solved subproblems is called Memoization.

2)	Bottom-up with Tabulation: This method avoids recursion, and works by solving an n-dimensional table. Since we know Fibonacci number is the sum of the two preceding numbers, we can use fact to populate table.
