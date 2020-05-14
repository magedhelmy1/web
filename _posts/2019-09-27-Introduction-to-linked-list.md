---
title: Introduction to Linked List
author: Maged Helmy
date: 2019-09-27 14:00:00 +0100
categories: [Blogging, Articles]
tags: [linked_lists]
---
Linked list representation:

Linked List Basics:
A linked list is a sequence of data structure which are connected via links. Linked list is a sequence of links which contains items. Each link contains a connection to another link. A link consists of:
Linked list can be visualized as a chain of nodes, where very node points to the next node. A linked list contains a link element called first. Each link carries a data field and a link field called next. Each link is linked with its next link using its next link. Last link carries a link as null to mark the end of the list.
Simply Linked List: Item navigation is forward only.
-	Link: Each link of a linked list can store a data called an element
-	Next: Each link of a linked list contains a link to the next link called Next
-	LinkedList- A linked list contains the connection link to the first link called first
Following are the basic operations supported by a list.
•	Insertion − Adds an element at the beginning of the list.
•	Deletion − Deletes an element at the beginning of the list.
•	Display − Displays the complete list.
•	Search − Searches an element using the given key.
•	Delete − Deletes an element using the given key.

Double Linked List: Items can be navigated forward and backward.
-	Prev: Each link of a linked list contains a link to the previous link called Prev.
-	LinkedList- A linked list contains the connection link to the first link called first, and to the last link called last.
A double linked list contains a link element called first and last. Each link carries a data field and two link fields called next and prev. Each link is linked with its next link using its next link. Each link is linked with its previous link using its previous link. The last link carries al ink as null to mark the end of the list.

Following are the basic operations supported by a list.
•	Insertion − Adds an element at the beginning of the list.
•	Deletion − Deletes an element at the beginning of the list.
•	Insert Last − Adds an element at the end of the list.
•	Delete Last − Deletes an element from the end of the list.
•	Insert After − Adds an element after an item of the list.
•	Delete − Deletes an element from the list using the key.
•	Display forward − Displays the complete list in a forward manner.
•	Display backward − Displays the complete list in a backward manner.

Circular Linked List: Last item contains link of the element as next and the first element has link to the last element as previous. Both single and double linked can be made into circular linked list. In a single linked list, the next pointer of the last node points to the first node. In a doubly linked as circular, the next pointer of the last node points to the first node and the previous pointer of the first node points to the last node making the circular both directions.
As shown above, the last link points to the first link of the list in both cases of singly as well as double linked list. The first link previous points to the last of the list in case of double linked list.

The following are operations supported:
-	Insert: Inserts an element of the start of the list
-	Delete: Deletes an element from the start of the list
-	Display: Displays the list
