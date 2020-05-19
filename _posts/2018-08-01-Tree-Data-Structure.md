---
title: Tree Data Structure
author: Maged Helmy
date: 2018-08-01 14:00:00 +0100
categories: [Blogging, Articles]
tags: [data_structure_and_algorithms]
---

Tree data Structure: A tree presents the nodes connected by edges. Binary tree is a special data structure used for data storage purposes. A binary tree has a special condition that each node can have a maximum of two children. A binary tree has the benefits of both an ordered array and a linked list as search is as quick as in a sorted array and insertion or deletion operation are as in linked list.
Important Terms:
-	Path refers to the sequence of nodes along the edges of a tree.
-	Root is the node at the op of the tree. There is only one root per tree and one path from the root node to any node
-	Parent: Any node except the root node has one edge upward to a node called parent
-	Child: The node below a given node connected by its edge downward is called its child node
-	Leaf: The node which does not have a any child node is called the leaf node
-	Subtree represents the descendants of a node
-	Visiting refers to checking the value of a node when control is on the node
-	Traversing means passing through nodes in a specific order
-	Levels: Level of a node represents the generation of a node.
-	Key represents a value of a node based on which a search operation is to be carried out for a node.
Binary Search Tree Representation:
A binary search tree is special. Its node’s left child must have a value lesst than its parents value and the nodel right child must have a value greater than its parent value.
The BST operations are:
-	Insert: Inserts an element in a tree/create a tree
-	Search: Searches an element in a tree
-	Preorder Traversal: Traverses a tree in a pre-order manner
-	Inorder Traversal: Traverses a tree in an in-order manner
-	Post order Traversal: Traverses a tree in a post-order manner
Insert operation:
The insert operation works as follows:
1)	The very first insertion creates the tree
2)	After that, whenever an element is to be inserted, first locate its proper location by searching from the root node
3)	If the data is less than the key value, search for the empty location in the left subtree and insert the data.
4)	Otherwise, search for the empty location in the right subtree and insert the data.
Search operation: Whenever an element is to be searched, start searching from the root node, then if the data is less than the key vaue, search for the element in the left subtree. Otherwise, search for the element in the right subtree.
Tree Traversal: Traversing is the process of searching the nodes on a tree. We traverse a tree to search or locate a given item or key in the tree or print all the values it contains.
Binary Search Tree:
-	In order traversal: the left subtree is visited first, then the root and later the right subtree. The output will produce sorted key values in an ascending order. D → B → E → A → F → C → G
-	Pre-order traversal: The root node is visited first, then the left subtree and finally the right subtree. A → B → D → E → C → F → G
-	Post-order traversal: The root node is visited last. First, we traverse the left subtree, then the right subtree and finally the root node. It visits all the leafs before going into the root. D → E → B → F → G → C → A

AVL (Adelson, Velski & Landis) Tree: The worst-case scenario of a BST is closest to linear search algorithms, that is O(n). AVL is a height balancing tree where it checks the height of the left and right sub-tress and assures that the difference is not more than 1. This difference is called the balance factor. If the difference in the height of left and right subtree is more than 1, the tree is balanced using some rotation techniques.
Right Rotation: AVL tree may become unbalanced, if a node is inserted in the left subtree of the left subtree. The tree needs a right rotation.
Left-right rotation: double rotations are slightly complex versions of rotations. To do them best, take notes “actions” while doing them. A left-right rotation is a combination of left rotation followed by right rotation.
Right-left rotation:

-	Use diagrams illustration from https://www.tutorialspoint.com/data_structures_algorithms/avl_tree_algorithm.htm
Spanning Tree: A spanning tree is a subset of graph G which has all the vertices covered with minimum possible number of edges. A spanning tree does not have cycles and cannot be disconnected. Every connected and undirected graph G has at least one spanning tree. A disconnected graph does not have any spanning tree, as it cannot be spanned to all its vertices. N^N-2  to get the number of spanning trees, where n is the number of nodes. Thus, we can conclude that the spanning trees are a subset of connected graph G and disconnected graphs do not have spanning tree. Also a single graph can have more than one spanning tree.
Properties of spanning tree:
-	A connected graph G can have more than one spanning tree
-	All possible spanning tree of graph G, have the same number of edges and vertices
-	The spanning tree does not have any cycle (loops)
-	Removing one edge from the spanning tree will make the graph disconnected. The spanning tree is minimally connected
-	Adding one edge to the spanning tree will create a circuit or loop. i.e. The spanning tree is maximally acyclic.
A spanning tree is used to find the minimum path to connect all nodes in a graph. Common applications are:
-	Civil Network Planning
-	Computer Network Routing Protocol
-	Cluster Analysis
Minimum Spanning Tree (MST): In a weighted graph, a minimum spanning tree is a spanning tree that has minimum weight than all other spanning trees of the same graph. Spanning tree examples are Kruskals algorithm and Prims algorithm which are examples of greedy algorithms.
Heap: is a special case of a balanced binary tree data structure where the root-node key is compared with its children and arranged accordingly. There are two types of heap, the min-heap and the max-heap. The min-heap is where the value of the root node is less than or equal to either of its children. The max-heap is where the value of the root node is greater than or equal to either of its children. Best demonstrated with a diagram

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
