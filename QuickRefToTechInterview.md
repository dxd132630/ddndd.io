# Quick reference to Tech interview:
======================================================

Generally the time complexities of the algorithms are expressed with following notations :

- Big Oh denotes "fewer than or the same as" <expression> iterations.
- Big Omega denotes "more than or the same as" <expression> iterations.
- Big Theta denotes "the same as" <expression> iterations.
- Little Oh denotes "fewer than" <expression> iterations.
- Little Omega denotes "more than" <expression> iterations.

### Asymptotic analysis :

In computational theory asymptote is used to represent the limiting behavior to describe the computational complexity of problems, generally in Big O notation. For rest of the discussion we will be using Big O notation to represent.

### Data structures :

<quote wiki> A data structure is a particular way to organize data in computer so  that it can be used efficiently.  < /quote wiki>
The data can be organized in various ways depending on the requirements like ease of access, optimized storage and efficient retrieval. Predominantly it can be categorized as follows :

##### Basic operations on data :
- **Insertion**:Insertion means addition of a new data element in a data structure.
- **Deletion**: Deletion means removal of a data element from a data structure if it is found.
- **Searching**:Searching involves searching for the specified data element in a data structure.
- **Traversal**:Traversal of a data structure means processing all the data elements present in it.
- **Sorting**:Arranging data elements of a data structure in a specified order is called sorting.
- **Merging**:Combining elements of two similar data structures to form a new data structure of the same type, is called merging.

##### Composite data structures: 
1. **Arrays** : 
An array is a low-level data structure that holds an ordered collection of elements. Each position in the array has an index, starting with 0. [ Wondering why indexing starts at 0 ?]. Optimal data representation for indexing. They are foundation of many other data structures, like dynamic arrays and dictionaries.
Dynamic arrays are one dimensional arrays which can grow dynamically in size. If the dynamic array is full they there is a mechanism to copy the contents to a large array.
Multi-dimensional arrays have more than one indices to collectively reference the data.

**Big O complexities** :
Space complexity worst case:  O(n)

|Average|Worst case |
|----|----|
|Access : O(1) |Access : O(1)|
|Search : O(n) |Search : O(n)|
|Insert : O(n) |Insert : O(n)|
|Delete : O(n) |Delete : O(n)|

##### Abstract data types :
1. **Singly Linked lists** : Data is stored in a object called "node" and each data object also holds a reference to its next data object. In a linked list, the first node is called the head and the last node is called the tail.They have constant insertion and deletion time. They can continue to expand.

**Big O complexities** :
Space complexity worst case:  O(n)

|Average|Worst case |
|----|----|
|Access : O(n) |Access : O(n)|
|Search : O(n) |Search : O(n)|
|Insert : O(1) |Insert : O(1)|
|Delete : O(1) |Delete : O(1)|

2. **Stacks** : It reminds me of stack of plates in my kitchen cabinet. The one you put on top is the very first one you can access. Its LIFO :Last in first out. If you want to access you favorite plate you have to move throught each plate from top until you reach your plate. If its at the bottom then you will access all the n-1 plates until you reach your favourite plate i.e, it has O(n) search /access time. Inserts and deletes are O(1) as they are operated on top of the stack.
Utility operations on Stacks : push() : adds an item, pop() : removes and returns the top item, peek() : returns the item on the top of the stack, without removing it and is_empty() : returns True if the stack is empty, False otherwise.


**Big O complexities** :
Space complexity worst case:  O(n)

|Average|Worst case |
|----|----|
|Access : O(n) |Access : O(n)|
|Search : O(n) |Search : O(n)|
|Insert : O(1) |Insert : O(1)|
|Delete : O(1) |Delete : O(1)|

3. **Queue** : Remember the queue in Starbucks the customer standing first in the line gets served first. Its FIFO : first in first out. Enqueue is to add elements to the end of the queue and dequeue is to remove the elements from the start of the queue. Other utility menthods are peek() :returns the item at the front of the queue, without removing it, is_empty() : returns True if the queue is empty, False otherwise.


**Big O complexities** :
Space complexity worst case:  O(n)

|Average|Worst case |
|----|----|
|Access : O(n) |Access : O(n)|
|Search : O(n) |Search : O(n)|
|Insert : O(1) |Insert : O(1)|
|Delete : O(1) |Delete : O(1)|

4. **Doubly Linked lists** : Doubly linked list has pointers to the next and the previous nodes. Doubly linked lists allow backward traversal of the list as compared to singly linked list which fails if you just had a pointer to a node in the middle of a list, then there would be no way to know what its previous node was. 


**Big O complexities** :
Space complexity worst case:  O(n)

|Average|Worst case |
|----|----|
|Access : O(n) |Access : O(n)|
|Search : O(n) |Search : O(n)|
|Insert : O(1) |Insert : O(1)|
|Delete : O(1) |Delete : O(1)|

5. **Skip lists** : A skip list is a data structure that allows fast search within an ordered sequence of elements. Fast search is made possible by maintaining a linked hierarchy of subsequences, each skipping over fewer elements. The idea is simple, we create multiple layers so that we can skip some nodes for faster access.The upper layer works as an “express lane” which connects only main outer stations, and the lower layer works as a “normal lane” which connects every station. 

**Big O complexities** :
Space complexity worst case:  O(n log(n))

|Average|Worst case |
|----|----|
|Access : O(log(n)) |Access : O(n)|
|Search : O(log(n)) |Search : O(n)|
|Insert : O(log(n)) |Insert : O(n)|
|Delete : O(log(n)) |Delete : O(n)|


6. **Hash tables/ Hash Maps** :Storing the key value pair such that each value is mapped to the key (hash of the value). Data is unordered. Hash map ensures constant time for insertion and lookups. But it comes with a cost if more than one value is hashed to  the same value. This is called Hash-collision.This is accomodated by having very large hash tables. Important applications of this is in database indexing.

**Big O complexities** :
Space complexity worst case:  O(n)

|Average|Worst case |
|----|----|
|Search : O(1) |Search : O(n)|
|Insert : O(1) |Insert : O(n)|
|Delete : O(1) |Delete : O(n)|

7. **Trees** : A tree is a widely used abstract data type (ADT) or data structure implementing this ADT that simulates a hierarchical tree structure, with a root value and subtrees of children with a parent node, represented as a set of linked nodes.
    * **Binary trees** : A binary tree is a tree where every node has two or fewer children. The children are usually called left and right.The number of nodes on the last level is equal to the sum of the number of nodes on all other levels (minus 1). In other words, half of our nodes are on the last level.If we have O(n) nodes, we have a height of O(log{2}(n)).

**Big O complexities** :
Space complexity worst case:  O(n)

|Average|Worst case |
|----|----|
|Access : O(log(n)) |Access : O(n)|
|Search : O(log(n)) |Search : O(n)|
|Insert : O(log(n)) |Insert : O(n)|
|Delete : O(log(n)) |Delete : O(n)|

        * **Binary search trees** : It is binary tree with following invariants: 
         * The data stored at each node has a distinguished key which is unique in the tree and belongs to a total order. (That is, for any two non-equal keys, x,y either x < y or y < x.)
         * The key of any node is greater than all keys occurring in its left subtree and less than all keys occurring in its right subtree.
         * Inserts are simple, insert the nodes to maintain the invariants.
         * But delete operations in BST are of two types : Simple delete and complex delete.
         * Simple delete :
            * Deleting a leaf --- simply remove it
            * Deleting a node with one child --- remove it and move its child (the subtree rooted at its child) up
            * Deleting a node with two children --- swap with the smallest keyed-child in its right subtree, then remove or swap with the largest keyed-child in its left subtree, then remove
        * **AVL** : 
        * **Red-black**
    * **B-Trees**
        * **B+Trees**
        * **B\* Trees**
        * **2-3 trees**
        * **2-3-4 trees**
    * **Heaps** : 
        * **Binary heaps**
        * **Binomial heaps**
        * **Fibonacci heaps**
    * **Trees**
        * **Trie**
        * **Radix**
8. **Graphs**
