---
title: Searching Techniques
author: Maged Helmy
date: 2018-10-01 14:00:00 +0100
categories: [Blogging, Computer Science]
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


A hash table allows the fast retrieval of data no matter how much data there is. Each index number can be calculated using the value itself. So, the values are placed in an array according to a calculation. For example, the name TIM. The ASCII key is 84, 105 and 109. We can sum up all the values (84 + 105 + 109) = 298. We can divide that by 11 (for example, if that was the length of the array), and the remainder is 1. This can be position of the ASCII key in the array list, at 1. This can be mathematically represented as

```
	Index number= sum (ASCII codes) Mod (size of array)
```
To retrieve an item, we use the value to do a fast retrieval look up using the hash function above.

To revisit, a hashing algorithm or a hash function, is the calculation applied to a key to transform it to an index number which corresponds to a position in the hash table.

To generatlize, for numeric keys, it is common to take the key and divide it by the number of available addresses, n, and take the remainder as the index. For alphanumeric keys, divide the sum of the ASCII codes in a key by the number of available addresses, n, and take the remainder as shown in the example above.

Another method to calculate the hash is the folding method (best for storing phone numbers), where we divide th key into equal parts then adds the part together. There are different types of hash table. Some are more appropriate than other depending on the size of data and length of available memory.

## Collisions

When generating an index for two items yields the same index value, this is called collisions as the index "collides".There are two ways to deal with this, open addressing and closed addresing.

One type of open addressing is linear probing. Linear probing is where you place an item with a colliding index in the next available slot. And when you want to retrieve this data you apply hashing function + linear probing method. In other words, open addressing is placing an item in the next open space.

Disadvantage of Linear Probing is that it might cause clustering of data if the index values are too close. At worse case, it may involve linear search if the data is the same size as the has table.

Other examples of open addressing are:
-	Plus 3 rehash: To deal with clustering issue of linear probing, instead of adding in the next available space, add in the 3rd available place.
-	Quadratic probing: square the number of failed attempts. The distance from the collision rapidly grows rapidly
-	Double hashing: applies a second hash function. The result of the second hashing is the distance to try next from the distance of collision

Another way, is to make the table storing the data bigger than needed. For example, to make only 70% of the hash table to be only occupied. This is called the load factor, where the total data occupied is less than the actual size of the array. A dynamic sizing can be applied, where if the database reaches the value of the loading factor the database will increase. If the load factor is low, then hashing with linear probing should work well.

Another way to deal with collision is to use chaining which is known as closed addressing. This is adding items on the colliding indexes by using a linked list. We can then search the item by traversing the linked list. The look up is better in comparison to the linear probing. If the load factor is slow, open addressing is better.

The best hash function should:

-	Minimize Collisions
-	Uniform distribution of hash values
-	The hash function should be easy to calculate
-	Resolve any collisions

## To summarize

-	The address of each key is calculated using the key itself
-	Collison’s resolved with open or closed addressing
-	Hashing is widely used in database indexing, compilers, cashing etc.
-	The insertion, deletion and retrieve occur in constant time in the best case scenario. Not when there is a collision.


## Depth First Traversal

This is O(n) since we have to visit all the nodes.

Depth first traversal traverses a graph in a depthward motion and uses a stack to remember to get to the next vertex to start a search, when a dead end occurs in any iteration. So a depth first travel, follows a path from a starting vertex until we reach the end of the vertex on that track. It then goes back an iteration and visits all the neighboring path in that vertex, and so on, until there are no longer any vertices to cover. We backtrack until all have been visited.
dfs.

It uses less memory than BFS since it does need memory to save child points/location.

![dfs1]({{"/assets/img/sample/dfs.PNG" | relative_url }})
![dfs2]({{"/assets/img/sample/dfs1.PNG" | relative_url }})
![dfs3]({{"/assets/img/sample/dfs2.PNG" | relative_url }})

The depth first traversal algorithm:

-	Push the first vertex onto the stack
-	Mark this vertex as visited
-	Repeat
o	Visit the next vertex adjacent to the one on top of the stack
o	Push this vertex onto the stack
o	Mark this vertex as visited
o	If there isn’t a vertex to bisit
o	Pop this vertex off the stack
-	End
-	Until the stack is empty

DFS uses stacking  whils BFS uses queuing.

## Breadth First Traversal

This is O(n) since we have to visit all the nodes.

Breath first research algorithm traverses a graph in a breadthward motion and uses a queue to remember to get the next vertex to start a search, when a dead end occurs in any iteration. The BFS starts by examining the nodes closer to the vertex and gradually starts examining those further away from the vertex.

![bfs1]({{"/assets/img/sample/bfs.PNG" | relative_url }})
![bfs2]({{"/assets/img/sample/bfs2.PNG" | relative_url }})
![bfs3]({{"/assets/img/sample/bfs3.PNG" | relative_url }})

Rule 1: visit the adjacent unvisited vertex. Mark it as visited. Display it. Insert it in a queue.

Rule 2: If no adjacent vertex is found, remove the first vertex from the queue

Rule 3: Repeat rule 1 and rule 2 until the queue is empty

You keep on going left to right until all nodes have been visited and dequeued. In other words, when there are no unmarked (unvisited) nodes. But as per the algorithm we keep on dequeuing in order to get all unvisited nodes. When the queue gets emptied, the program is over.

Both of these methods can be used in Graphs or Trees.

## Breadth First Traversal vs Depth First Traversal

BFS downside it requires more memory than DFS. All of the connected vertices must be stored in memory. So consumes more memory
The upside is, if you know the information required is closer up the node, then BFS will find it faster than DFS. Furthermore, it finds the shortest path between vertices

The DFS is better if solutions are frequent and located deep in the tree, or whether a path exists between two nodes, if the tree is wide (since BFS will require alot of memory). Moreover, DFS consumes less memory and finds the larger distant element(from source vertex) in less time.

THE BFS is better when you need to find the shortest path,  know the solution is closer to the root, if the solution is very deep but are rare.
