---
title: Sorting Techniques
author: Maged Helmy
date: 2020-05-09 14:00:00 +0100
categories: [Blogging, Articles]
tags: [data_structure_and_algorithms]
---

Sorting Techniques:
What is the sorting problem: Sorting is arranging data in a particular format. Sorting algorithms specifies the way to arrange data order. Most are in numerical or lexicographical order. A type of Sorting is said to happen “in-place sorting” when the algorithm does not require any extra space, for example bubble-sort. Other sorting algorithms require space equal or more than the algorithm elements, this is called not-in-place sorting. For example, merge sort.
Moreover, there is stable and not stable sorting. Stable sorting does not change the sequence of duplicate value in which they appear, while unstable sorting changes the sequence of duplicate content.
Furthermore, there are adaptive and non-adaptive sorting algorithms. An adaptive sorting algorithm takes into account that some elements might be already sorted in the list. A non-adaptive sorting algorithm does not take into account that some lists are already sorted, and re-enforces sorting to confirm the sort. Example: 1, 3, 4, 6, 8, 9
An increasing order is if the successive element is great than the previous one.
A non-decreasing order is if the successive element is greater than or equal to the previous element in the sequence. Example: 1, 3, 3, 6, 8, 9
A decreasing order is when successive element is less than the current one.
A non-increasing order if the successive element is less than or equal to its previous element in the sequence
Types of Sorting Algorithms:

-	Bubble Sort:
o	It is a simple algorithm which compares a pair of adjacent elements and swaps them if they are not equal. Bubble sort starts with the first two elements, compares them to check which is greater, then swaps them. It keeps on repeating this process until no swaps are required by the last pass.
o	This algorithm is not suitable for large scale data sets and the worst case complexity are O(n^2) where n is the number of items

-	Insertion Sort:
o	This is an in-place comparison-based sorting algorithm. A sorted sub-list is maintained which is always sorted. An element which is to be “insert”ed in this sorted sub-list, has to find its appropriate place and then it has to be inserted there. The array is search sequentially and unsorted items are moved and inserted into the sorted sub-list.
o	Not suitable for large data since the worse case complexity are O(n^2) where n is the number of items.
o	Insertion sorts, scans number by number and inserts it in the appropriate place on the sorted array
o	Good reference: https://stackoverflow.com/questions/15799034/insertion-sort-vs-selection-sort
-	Selection Sort:
o	This sorting algorithm is an in-place comparison-based algorithm in which the list is divided into two parts, the sorted part at the left and the unsorted part at the right side. Initially, the sorted part is empty, and the unsorted part is the entire list.
o	Selection sort finds the lowest number on every iteration
o	The smallest element is selected from the unsorted array and swapped with the leftmost element, and that element becomes part of the sorted array. This process continues moving unsorted array by one element to the right. Not suitable for large datasets with a worse case complexity are of O(n^2), where n is the number of items.
-	Merge Sort:
o	Idea is based on divide and conquer technique with a worse-case time complexity being O(n log n).
o	Merge sort divides the whole array iteratively unless the atomic values are achieved. The elements for each list are compared and combined in a sorted manner. And recursively lists are merged, until the list is back again.
-	Shell Sort:
o	Based on the insertion sort algorithm but highly efficient. Shell sorts avoids large shifts as in case of insertion sort, if the smaller value is to the far right and has to be moved to the far left.
o	It uses spacing termed as interval which is calculated based on the Knuth’s formulae.
o	The worse case is O(n) since it depends on the gap sequence
o	The concept of gap is if it i.e. equals to 4, then we will consider the first element and the 5th element. The 2nd element with 6th element and so on. We compare these numbers and sort them. We then create a smaller gap for example 2 and again swap values according to the other.
o	In the last pass shell sort is like the insertion sort with gap 1. Where it compares element next to each other.
-	Quick sort:
o	Is a highly efficient sorting algorithm and is based on partitioning of array into smaller arrays. It is based on the divide-and-conquer algorithm.
o	The large array is partitioned into two arrays, one of which holds values smaller than the specified value, say pivot. Based on that partition values will hold greater or smaller values.
o	The pivot value divides the list into two parts and recursively, it finds the pivot for each sub-lists until all lists contain only one element
o	There are four ways the pivot can be picked, the first element as a pivot, the last element as a pivot, a random element as a pivot and a median element as a pivot.
o	The pivot should divide the list where all elements smaller than it should go to the left side, and all elements larger than it should go on the right side.
	Example:
	Choose the highest index to be the pivot
	Take two variables to point left and right of the list excluding pivot
	Left points to the low index
	Right points to the high index
	While value at left is less than pivot move right
	While value at right is greater than pivot move left
	If both steps 5 and steps 6 does not match swap left and right
	If left is bigger than right, the point where they met is the new pivot

How to calculate the asymptotic time complexity of the above algorithms?
Generally, by calculating how many times a statement will execute when the data doubles.  WE calculate the rate of growth of time in respect to the input size.

## Merge Sort
The input array is divided several times, sorted and then they are combined and merged back together. That is O(nlog(n)) in time complexity which is known as linearithmic. It is the same with best, average or worse scenario since the amount of operations are still the same. For space complexity, the number of levels represents the recursion, if we double the data, we need one more level of recursion, therefore, the stack will increase logarithmically. So the stack has O(log n) space complexity but the auxiliary array has O(n) linear space complexity, since you need temporary stacks to hold the array. Since linear complexity is bigger, than the space complexity of merge sort is linear.
