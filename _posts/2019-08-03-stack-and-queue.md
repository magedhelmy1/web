---
title: Stack and Queue
author: Maged Helmy
date: 2019-08-03 14:00:00 +0100
categories: [Blogging, Articles]
tags: [stack_queue]
---

Data Structure and Algorithms- Stack

Data structure is a way of organizing data so that it be efficiently accessed.

An abstract data structure is defined by a set of values and set of operations. The abstract is used to perform different operations that are abstracted from the user. In other words, an abstract data type is an abstraction of a data structure which provides only the interface to which a data structure must adhere to. For example, abstract data structures, are List, Queue, Map. The implement of a list is Dynamic array or linked list, the implement of a queue can be linked list-based queue, array based queue, or stack based queue. The map ADT can be implemented using tree map or hash table/hash map.

A stack is an abstract data type which allows operations at one end only. We can place or remove a card or plate from the top of the stack only. Also, all data operations occur at one end only, we can only access the top element of a stack.  This feature makes it a LIFO data structure, where LIFO stands for Last-in-first-out.  The element is inserted as a push operation and removed using a pop operation.

A stack operation may involve initializing the stack, using it and then do-initializing it. A stack is used for two reasons. Push() and pop(). When pushing, we can use peek() to get the top data element of the stack, isFull() to check if stack is fully, isEmpty() to check if stack is empty.
At all points, we maintain an index to the last pushed data on the stack. The top value is thus the last object.

The push operation is the process of adding a data element on the stack.
1)	Checks if the stack is full
2)	If stack is full, produces an error and exit
3)	If the stack is not full, increments top to the point next empty space
4)	Adds data element to the stack location where top is pointing
5)	Returns success

The pop operation, the data element is not actually move, instead top is decremented to a lower position in the stack. In a linked list, pop removes data element and deallocates memory space.

1)	Check if the stack is empty
2)	If empty, produce an error and exit
3)	If the stack is not empty, access the data element at the top
4)	Decrease the value of top by 1
5)	Return success


Data Structure and Algorithms – Queue

Similar to stacks, Queue is an abstract data structure, unlike stacks, a queue is open at both ends. One end is always used to inset data and the is used to remove data. This is First-in-first out methodology.

Queue representation: -> Data in-> Queue -> Data out. As in stacks, a queue can be also implemented using arrays, linked-lists, pointers and structures.

The basic operations of a queue are:
-	Enqueue()- add an item to the queue
-	Dequeue()- remove an item from the queue
-	Peek()- get the element at the front of the queue without removing it
-	Isfull()- check if the queue is full
-	Isempty()- check if the queue is empty
