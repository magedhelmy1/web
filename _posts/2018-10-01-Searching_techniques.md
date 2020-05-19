---
title: Searching Techniques
author: Maged Helmy
date: 2018-10-01 14:00:00 +0100
categories: [Blogging, Articles]
tags: [data_structure_and_algorithms]
---

## Linear Search

A sequential search is made over all items one by one. Every item is checked and if a match is found then the item is returned.  Otherwise, the search continues to the end. with O(n) complexity since in worse case it has to search all the data in array.

## Binary Search

Is a fast algorithm with a run-time complexity of O(log n). This search algorithm works on the principle of divide and conquer. The items should be already sorted. The binary target looks for the item in the middle most item of the collection. If the match occurs, the index is returned otherwise, the middle item is great than the item it will search the sub-array to the left or right. In the sub-array, the mid index again checked if it contains the value. If not, it is subdivided and if smaller than mid value, the left side is checked, otherwise the right side will be checked. The search is continued until the subarray is reduced to zero.

## Interpolation Search

An improved variant of binary search. The search algorithm works on the probing position of the required value. For this algorithm to work properly, the data collection should be in a sorted form and equally distributed.  

Binary search goes to the middle element to check the algorithm. It does not take advantage to probe the position of the desired data. On the other hand, interpolation search searches in different locations according to the value of the key being searched. If the value of the key is close to the last element, interpolation search will start at the end. The interpolation search uses this equation instead to start looking for the index instead of jumping straight to the middle.

```
	mid = Lo + ((Hi - Lo) / (A[Hi] - A[Lo])) * (X - A[Lo])
	Step 1 − Start searching data from middle of the list.
	Step 2 − If it is a match, return the index of the item, and exit.
	Step 3 − If it is not a match, probe position.
	Step 4 − Divide the list using probing formula and find the new midle.
	Step 5 − If data is greater than middle, search in higher sub-list.
	Step 6 − If data is smaller than middle, search in lower sub-list.
	Step 7 − Repeat until match.

```

## Hash Table

Hash table is a data structure which stores data in an associative manner. In a hash table, data is stored in an array format, where each data value has its own unique index value. Thus, it becomes a data structure in which insertion and search operations are very fast irrespective of the size of the data. Hash tables are known as dictonaries in python.

Moreover, hashing is a technique that converts a range of key values into a range of indexes of an array. This stores the items in the (key,value) format. This can also be referred to as a hash function. A hash function generates the key/index where the value will be stored.

## Basic operations

Basic operations: the basic operations of a hash table are

-	Search: Searches an element in a hash table
-	Insert: Inserts an element in a hash table
-	Delete: Deletes an element from the hash table


A hash table allows the fast retrieval of data no matter how much data there is. Each index number can be calculated using the value itself. So, the values are placed in an array according to a calculation. For example, the name TIM. The ASCII key is 84, 105 and 109. We can sum up all the values (84 + 105 + 109) = 298. We can divide that by 11 (length of the array), and the remainder is 1. This can be position of the ASCII key in the array list. This can be mathematically represented as

	Index number= sum ASCII codes Mod size of array

To retrieve an item, we use the value to do a fast retrieval look up.

To revisit, a hashing algorithm or a hash function, is the calculation applied to a key to transform it to an index number which corresponds to a position in the hash table. For numeric keys, it is common to take the key by the number of available addresses, n, and take the remainder

-	Address = key Mod n

N is the number of available addresses.

For alphanumeric keys, divide the sum of the ASCII codes in a key by the number of available addresses, n, and take the remainder.

Another method is the folding method, divides key into equal parts then adds the part together. There are different types of hash table. Some are more appropriate than other.

## Linear probing

As we can see, it may happen that the hashing technique is used to create an already used index of the array. In such a case, we can search the next empty location in the array by looking into the next cell until we find an empty cell. This technique is called linear probing.

## Collisions

When generating an index for two items yields the same index value, this is called collisions as the index "collides".There are two ways to deal with this, open addressing and closed addresing.

One type of open addressing is linear probing, where you place an item with a classing index in the next available slot. And when you want to retrieve this data you apply hashing function + linear probing method.

Another way, is to make the table bigger than necessity. This is called the load factor, where the total data occupied is less than the actual size of the array. A dynamic sizing can be applied, where if the database reaches the value of the loading factor the database will increase. If the load factor is low, then hashing with linear probing should work well.

Another way to deal with collision is to use chaining which is known as closed addressing. This is adding items on the colliding indexes by using a linked list. We can then search the item by traversing the linked list. The look up is better in comparison to the linear probing. If the load factor is slow, open addressing is better.

## Open addressing:

-	Linear Probing: This might cause clustering of data if the index values are too close
-	Plus 3 rehash: To deal with clustering, instead of adding in the next available space, add in the 3rd available place.
-	Quadratic probing: square the number of failed attempts. The distance from the collision rapidly grows rapidly
-	Double hashing: applies a second hash function. The result of the second hashing is the distance to try next from the distance of collision

## Closed Addressing

-	Chaining:




## To summarize

Otherwise, if you know the values in advance, you can create the perfect hash function to sort them.

The objective of hash function
-	Minimize Collisions
-	Uniform distribution of hash values
-	The hash function should be easy to calculate
-	Resolve any collisions

-	The address of each key is calculated using the key itself
-	Collison’s resolved with open or closed addressing
-	Hashing is widely used in database indexing, compilers, cashing etc.
-	The insertion, deletion and retrieve occur in constant time in the best case scenario. Not when there is a collision.
