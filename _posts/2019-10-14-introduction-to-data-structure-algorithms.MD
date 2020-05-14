---
title: Introduction to Algorithms and Data Structure
author: Maged Helmy
date: 2019-10-14 14:00:00 +0100
categories: [Blogging, Articles]
tags: [data_structure]
---

Data Structure & Algorithms Introduction:
From the data structure point of view, following are some important categories of algorithms:
-	Search − Algorithm to search an item in a data structure.
-	Sort − Algorithm to sort items in a certain order.
-	Insert − Algorithm to insert item in a data structure.
-	Update − Algorithm to update an existing item in a data structure.
-	Delete − Algorithm to delete an existing item from a data structure.
Data structure is a systematic way to organize data to use efficiently.  The characteristic of data structure is three, correctness, time complexity and space complexity. Time Complexity − Running time or the execution time of operations of data structure must be as small as possible. Space Complexity − Memory usage of a data structure operation should be as little as possible.

Algorithms Introduction:
When starting with any problem to solve. Clearly have the input stated and the output stated. Also, right down any edge cases as part of the input. The algorithm bridges the input with the output. The algorithm is a step-by-step procedure which defines the instructions to be executed in an order to get a desired output.
Asymptotic analysis is defining the mathematical framing of an algorithm run-time performance. This helps us in concluding the best case (minimum time required to run execution), average case and worse case (maximum time required for program execution) scenario of an algorithm. For example, f(n) means it increases linearly, for g(n^2) it increases exponentially. Asymptotic Notations are O-notation, Omega-notation and Theta Notation. We have a whole article dedicated to this in this website but a quick recap o the asymptotic notations are:
-	Big O Notation: Formal way to express the upper bound of an algorithm’s running time. It measures the worse case time complexity of the longest amount of time an algorithm can possibly take to complete.
-	Omega Notation: is the formal way to measure the lower bound of an algorithm running time. It measures the best time to complete an algorithm
-	Theta Notation: It expresses the lower and upper bound of an algorithm running time.


|Common Asymptotic Notations |Term| Definition| Example
|:---|:---|:--|---:|
|Constant| O(1) | Program will run the same length regardless of input size| Stack push, pop and peek, Queue, enqueue and dequeue, insert a node into a linked list
|Logarithmic| O(log n) | The time taken is proportional to the logarithm of the amount of data. The impact of increasing data on time lessens as the data grows|Binary search a sorted list, search a binary tree, merge sort, heap sort, quick sort
|Linear| O(n) | Program will run proportionally to the size of the input| Linear Search, count items in a list, compare a pair of strings
|Linearithmic | O(n log n) | The time taken is proportional to the logarithm of the amount of data multiplied by the amount of data| Merge sort and Quick sort
|Quadratic| O(n^2) | Doubling the size of the input will quadruple the running time| Bubble sort, selection sort, insertion sort, traverse a 2D array
|Cubic| O(n^3) | Doubling the size of the input will have a cubic effect on the running time|-
|Polynomial| O(n^k) | Time taken is proportional to the amount of data raised to the power of a constant. If K is 2 then is quadratic, if k is 3 then it is cubic complexity. K can be any number| one can think of constant, linear, quadratic and cubic are examples of polynomial.
|Exponential| O(K^n) | Time taken is proportional to a constant raised to the power of the amount of data| n-Queen problem, Travelling salesman, password cracking that operates by brute force
|Factorial| O(n!) | Doubling the size of the input, will have a factorial effect on the time|



To summarize, the concept of asymptotic complexity is to draw an equivalence between functions as their input approaches infinity.
Greedy Algorithms: It solves the problem by making a local optimal choice at each stage with the hope of finding a global optimum.


Divide and Conquer Algorithms: The problem is divided into smaller sub-problems and then each problem is solved independently. When we keep on dividing, it will reach into a stage where it cannot be divided anymore. It is recursive by nature. When you break the problem, it essentially remains the same. The solution of all sub-problems is merged in order to obtain the solution of an original problem. Examples include merge sort, quick sort, binary search, closest pair.
Dynamic Programming: Similar to divide and conquer in breaking down the problem into smaller problems. But unlike divide and conquer, these sub-problems are not solved independently, but rather it looks at will examine the results of the previously solved sub-problems. The solutions of sub-problems are combined in order to achieve the best solution. It makes it efficient by storing intermediate results. It uses memoization.  A good example is Fibonacci where it has several recursion calls. The idea of dynamic programming is to reduce function calls of same methods. By storing the result of the function, we do not call it again. Using dynamic programming on Fibonacci, greedy algorithm is O(2^n) while dynamic programming is O(n). This technique of storing the results of already solved subproblems is called Memoization.
There are two methods:
1)	Top-down with Memoization: This approach tries to solve the bigger problem by recursively finding the solution to smaller sub-problems. Whenever we solve a sub-problem, we cache its resuls so that we don’t end up solving it repeatedly if it is called multiple times later. Instead, we return the saved results. This technique of storing the results of already solved subproblems is called Memoization.

2)	Bottom-up with Tabulation: This method avoids recursion, and works by solving an n-dimensional table. Since we know Fibonacci number is the sum of the two preceding numbers, we can use fact to populate table.

Data Structure Introduction:
Data Structure Basics: There are two types of data types, Built-in data type and Derived data types. The built-in data type is usually integers, Boolean, floating, character and strings. Whilst derived data types are list, array, stack and queue. The basic operations include traversing, searching, insertion, deletion sorting and merging.
Array Data Structure:  The two concepts of an array are an element and index. Each element stored in an array is called an element. Each location of an element in an array has a numerical index which identifies the element.
-	Traverse is printing all the array elements one by one
-	Insertion is adding an element at the given index
-	Deletion deletes an element at the given index
-	Searching is searching an element song the given index by the value
-	Update is updating an element given an index.
