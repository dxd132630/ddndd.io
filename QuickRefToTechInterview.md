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
1. **Singly Linked lists** : 
2. **Stacks**
3. **Queue**
4. **Doubly Linked lists**
5. **Skip lists**
6. **Hash tables**
7. **Trees**
    * **Binary trees**
        * **AVL**
        * **Red-black**
        * **Binary search trees**
    * **B-Trees**
        * **B+Trees**
        * **B\* Trees**
        * **2-3 trees**
        * **2-3-4 trees**
    * **Heaps**
        * **Binary heaps**
        * **Binomial heaps**
        * **Fibonacci heaps**
    * **Trees**
        * **Trie**
        * **Radix**
8. **Graphs**
