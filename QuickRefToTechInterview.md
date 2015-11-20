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
Average|Worst case 
----|----
Access : O(1) |Access : O(1)
Search : O(n) |Search : O(n)
Insert : O(n) |Insert : O(n)
Delete : O(n) |Delete : O(n)

##### Abstract data types :
1. **Singly Linked lists** : Data is stored in a object called "node" and each data object also holds a reference to its next data object. In a linked list, the first node is called the head and the last node is called the tail.They have constant insertion and deletion time. They can continue to expand.

**Big O complexities** :
Space complexity worst case:  O(n)
Average|Worst case 
----|----
Access : O(n) |Access : O(n)
Search : O(n) |Search : O(n)
Insert : O(1) |Insert : O(1)
Delete : O(1) |Delete : O(1)

2. **Stacks**
3. **Queue**
4. **Doubly Linked lists** : Doubly linked list has pointers to the next and the previous nodes. Doubly linked lists allow backward traversal of the list as compared to singly linked list which fails if you just had a pointer to a node in the middle of a list, then there would be no way to know what its previous node was. 

**Big O complexities** :
Space complexity worst case:  O(n)
Average|Worst case 
----|----
Access : O(n) |Access : O(n)
Search : O(n) |Search : O(n)
Insert : O(1) |Insert : O(1)
Delete : O(1) |Delete : O(1)

5. **Skip lists**
6. **Hash tables/ Hash Maps** :Storing the key value pair such that each value is mapped to the key (hash of the value). Data is unordered. Hash map ensures constant time for insertion and lookups. But it comes with a cost if more than one value is hashed to  the same value. This is called Hash-collision.This is accomodated by having very large hash tables. Important applications of this is in database indexing.

**Big O complexities** :
Space complexity worst case:  O(n)
Average|Worst case 
----|----
Search : O(1) |Search : O(n)
Insert : O(1) |Insert : O(n)
Delete : O(1) |Delete : O(n)

7. **Trees**
    * **Binary trees** : Each node of this data structure has 2 nodes
        * **AVL**
        * **Red-black**
        * **Binary search trees**
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
