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


2. **Stacks** : It reminds me of stack of plates in my kitchen cabinet. The one you put on top is the very first one you can access. Its LIFO :Last in first out. If you want to access you favorite plate you have to move through each plate from top until you reach your plate. If its at the bottom then you will access all the n-1 plates until you reach your favorite plate i.e, it has O(n) search /access time. Inserts and deletes are O(1) as they are operated on top of the stack.
Utility operations on Stacks : push() : adds an item, pop() : removes and returns the top item, peek() : returns the item on the top of the stack, without removing it and is_empty() : returns True if the stack is empty, False otherwise.


   **Big O complexities** :
   Space complexity worst case:  O(n)
   
   |Average|Worst case |
   |----|----|
   |Access : O(n) |Access : O(n)|
   |Search : O(n) |Search : O(n)|
   |Insert : O(1) |Insert : O(1)|
   |Delete : O(1) |Delete : O(1)|
   

3. **Queue** : Remember the queue in Star bucks the customer standing first in the line gets served first. Its FIFO : first in first out. Enqueue is to add elements to the end of the queue and dequeue is to remove the elements from the start of the queue. Other utility methods are peek() :returns the item at the front of the queue, without removing it, is_empty() : returns True if the queue is empty, False otherwise.


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
   


6. **Hash tables/ Hash Maps** :Storing the key value pair such that each value is mapped to the key (hash of the value). Data is unordered. Hash map ensures constant time for insertion and lookups. But it comes with a cost if more than one value is hashed to  the same value. This is called Hash-collision.This is accommodated by having very large hash tables. Important applications of this is in database indexing.


   **Big O complexities** :
   Space complexity worst case:  O(n)
   
   |Average|Worst case |
   |----|----|
   |Search : O(1) |Search : O(n)|
   |Insert : O(1) |Insert : O(n)|
   |Delete : O(1) |Delete : O(n)|
   

7. **Trees** : A tree is a widely used abstract data type (ADT) or data structure implementing this ADT that simulates a hierarchical tree structure, with a root value and subtrees of children with a parent node, represented as a set of linked nodes.

    * **Binary trees** : A binary tree is a tree where every node has two or fewer children. The children are usually called left and right.The number of nodes on the last level is equal to the sum of the number of nodes on all other levels (minus 1). In other words, half of our nodes are on the last level.If we have O(n) nodes, we have a height of O(log 2(n)).
        * **Binary search trees** : It is binary tree with following invariants: 
            * The data stored at each node has a distinguished key which is unique in the tree and belongs to a total order. (That is, for any two non-equal keys, x,y either x < y or y < x.)
            * The key of any node is greater than all keys occurring in its left subtree and less than all keys occurring in its right subtree.
            * Inserts are simple, insert the nodes to maintain the invariants.
            * But delete operations in BST are of two types : 
                * Simple delete : Deleting a leaf --- simply remove it.Deleting a node with one child --- remove it and move its child (the subtree rooted at its child) up.
                * Complex delete : Deleting a node with two children --- swap with the smallest keyed-child in its right subtree, then remove or swap with the largest keyed-child in its left subtree, then remove.

              **Big O complexities**: Space complexity worst case : O(n)
                  
              |Average|Worst case |
              |----|----|
              |Access : O(log(n)) |Access : O(n)|
              |Search : O(log(n)) |Search : O(n)|
              |Insert : O(log(n)) |Insert : O(n)|
              |Delete : O(log(n)) |Delete : O(n)|
                
        * **AVL** :AVL tree is a self-balancing Binary Search Tree (BST) with the invariant that the difference between heights of left and right subtrees cannot be more than one.The worst case complexity for skewed BST is O(n) to avoid this time complexity and to guarantee an upper bound of O(log n) for insert, search and delete operations. 
        
             **Big O complexities** :
            Space complexity worst case:  O(n)
            
            |Average|Worst case |
            |----|----|
            |Access : O(log(n)) |Access : O(log(n))|
            |Search : O(log(n)) |Search : O(log(n))|
            |Insert : O(log(n)) |Insert : O(log(n))|
            |Delete : O(log(n)) |Delete : O(log(n))|

        * **Red-black** : A red-black tree is a binary search tree which has the following red-black properties:
               * Every node is either red or black.
               * Every leaf (NULL) is black.
               * If a node is red, then both its children are black.
               * Every simple path from a node to a descendant leaf contains the same number of black nodes.
               
             **Big O complexities** :
            Space complexity worst case:  O(n)
            
            |Average|Worst case |
            |----|----|
            |Access : O(log(n)) |Access : O(log(n))|
            |Search : O(log(n)) |Search : O(log(n))|
            |Insert : O(log(n)) |Insert : O(log(n))|
            |Delete : O(log(n)) |Delete : O(log(n))|


    * **B-Trees**
         
         **Big O complexities** :
        Space complexity worst case:  O(n)
            
        |Average|Worst case |
        |----|----|
        |Access : O(log(n)) |Access : O(log(n))|
        |Search : O(log(n)) |Search : O(log(n))|
        |Insert : O(log(n)) |Insert : O(log(n))|
        |Delete : O(log(n)) |Delete : O(log(n))|

        * **B+Trees** :  A B+tree is a balanced tree in which every path from the root of the tree to a leaf is of the same length, and each nonleaf node of the tree has between [n/2] and [n] children, where n is fixed for a particular tree. It contains index pages and data pages. The capacity of a leaf has to be 50% or more. For example: if n = 4, then the key for each node is between 2 to 4. The index page will be 4 + 1 = 5.It is easy to maintain the tree balanced. Inserts in B+ trees:
         * do a search to determine what bucket the new record should go in if the bucket is not full, add the record.
         * otherwise, split the bucket.
         * allocate new leaf and move half the bucket's elements to the new bucket
         * insert the new leaf's smallest key and address into the parent.
         * if the parent is full, split it also
         * now add the middle key to the parent node
         * repeat until a parent is found that need not split
         * if the root splits, create a new root which has one key and two pointers.
         
        * **B\* Trees** :  A B-tree in which nodes are kept 2/3 full by redistributing keys to fill two child nodes, then splitting them into three nodes. 
        
        * **2-3 trees** :A tree which has every node with children (internal node) that either has two children (2-node) and one data element or three children (3-nodes) and two data elements.
        
        * **2-3-4 trees** :The 2, 3, and 4 in the name refer to how many links to child nodes can potentially be contained in a given node. 
          * For non-leaf nodes, three arrangements are possible:
            * A node with only one data item always has two children
            * A node with two data items always has three children
            * A node with three data items always has four children.
          * For non-leaf nodes with at least one data item ( a node will not exist with zero data items), the number of links may be 2, 3, or 4.
          
    * **Heaps** : 
        * **Binary heaps** : A binary heap is a complete binary tree which satisfies the heap ordering property. The ordering can be one of two types:
         * the min-heap property: the value of each node is greater than or equal to the value of its parent, with the minimum-value element at the root.
         * the max-heap property: the value of each node is less than or equal to the value of its parent, with the maximum-value element at the root.
         * In a heap the highest (or lowest) priority element is always stored at the root, hence the name "heap". A heap is not a sorted structure and can be regarded as partially ordered. As you see from the picture, there is no particular relationship among nodes on any given level, even among the siblings.
         * Since a heap is a complete binary tree, it has a smallest possible height - a heap with N nodes always has O(log N) height.
         * A heap is useful data structure when you need to remove the object with the highest (or lowest) priority. A common use of a heap is to implement a priority queue.


             **Big O complexities** :
                
            |Average |
            |----|
            |Heapify : O(n)|
            |FindMax : O(1) |
            |ExtractMax: O(log(n)) |
            |IncreaseKey: O(log(n))|
            |Insert : O(log(n))|
            |Delete : O(log(n))|
            |Merge : O(m+n)|

        * **Binomial heaps** :  A binomial tree of order k is defined recursively:
            * Order 0: single node.
            * Order k: one binomial tree of order k – 1 linked to another of order k – 1.
            * Given an order k binomial tree Bk,
               ・Its height is k.
               ・It has 2k nodes.
               ・It has nodes at depth i.
               ・The degree of its root is k.
               ・Deleting its root yields k binomial trees Bk–1, …, B0
            * A binomial heap is a sequence of binomial trees such that:
               ・Each tree is heap-ordered.
               ・There is either 0 or 1 binomial tree of order k.
            * Given a binomial heap with n nodes:
               ・The node containing the min element is a root of B0, B1, …, or Bk.
               ・It contains the binomial tree Bi iff bi = 1, where bk⋅ b2 b1 b0 is binary representation of n.
               ・It has ≤ ⎣log2 n⎦ + 1 binomial trees.
               ・Its height ≤ ⎣log2 n⎦.
               
               
             **Big O complexities** :
            
            |Average |
            |----|
            |Heapify : -|
            |FindMax : O(1) |
            |ExtractMax: O(log(n)) |
            |IncreaseKey: O(log(n))|
            |Insert : O(1)|
            |Delete : O(log(n))|
            |Merge : O(log(n))|
            
            
        * **Fibonacci heaps** :Like the binomial heap, a Fibonacci heap is a collection of heap-ordered trees. They do not need to be binomial trees however, this is where the relaxation of some of the binomial heap’s properties comes in.Each tree has an order just like the binomial heap that is based on the number of children. Nodes within a Fibonacci heap can be removed from their tree without restructuring them, so the order does not necessarily indicate the maximum height of the tree or number of nodes it contains.

             **Big O complexities** :
            
            |Average |
            |----|
            |Heapify : -|
            |FindMax : O(1) |
            |ExtractMax: O(log(n)) |
            |IncreaseKey: O(log(n))|
            |Insert : O(1)|
            |Delete : O(log(n))|
            |Merge : O(log(n))|
            

    * **Trees**
        * **Trie** : Trie is an efficient information retrieval data structure. Using trie, search complexities can be brought to optimal limit (key length). If we store keys in binary search tree, a well balanced BST will need time proportional to M * log N, where M is maximum string length and N is number of keys in tree. Using trie, we can search the key in O(M) time. However the penalty is on trie storage requirements.Every node of trie consists of multiple branches. Each branch represents a possible character of keys. We need to mark the last node of every key as leaf node. A trie node field value will be used to distinguish the node as leaf node (there are other uses of the value field). A simple structure to represent nodes of English alphabet can be as following,
  
  ``` java
  struct trie_node{
  int value; /* Used to mark leaf nodes */
  trie_node_t *children[ALPHABET_SIZE];
  };
  ```
  
    Inserting a key into trie is simple approach. Every character of input key is inserted as an individual trie node. Note that the children is an array of pointers to next level trie nodes. The key character acts as an index into the array children. If the input key is new or an extension of existing key, we need to construct non-existing nodes of the key, and mark leaf node. If the input key is prefix of existing key in trie, we simply mark the last node of key as leaf. The key length determines trie depth.
    
    Searching for a key is similar to insert operation, however we only compare the characters and move down. The search can terminate due to end of string or lack of key in trie. In the former case, if the value field of last node is non-zero then the key exists in trie. In the second case, the search terminates without examining all the characters of key, since the key is not present in trie.
    
    Insert and search costs O(key_length), however the memory requirements of trie is O(ALPHABET_SIZE * key_length * N) where N is number of keys in trie. There are efficient representation of trie nodes (e.g. compressed trie, ternary search tree, etc.) to minimize memory requirements of trie.


    * **Radix** : A radix tree is a compressed version of a trie. In a trie, on each edge you write a single letter, while in a PATRICIA tree (or radix tree) you store whole words.
        

### Sorting Algorithms:

#### Objective :
The objective is to rearrange the items such that their keys are in ascending order.
The sorting algorithms we consider divide into two basic types: those that sort in place (no extra memory except perhaps for a small function-call stack or a constant number of instance variables), and those that need enough extra memory to hold another copy of the array to be sorted.
There are two kinds of sorting of numbers :
   * Comparison sorting : The most common and prevalent sorting mechanism
   * Integer sorting : Less known sorting approach for numbers

#### Comparison sorting :

The idea used for sorting the numbers here is by having a comparison of the order of these numbers in the sequence and reassigning the numbers to the correct order based on this comparison. This generally has a lower bound of Sigma(nlogn). Although some sorting algorithms have O(n) only when they are sorted. In worst case the lower bound is nLogn.


1. **Selection sort** :The algorithm works by selecting the smallest unsorted item and then swapping it with the item in the next position to be filled.
The selection sort works as follows: you look through the entire array for the smallest element, once you find it you swap it (the smallest element) with the first element of the array. Then you look for the smallest element in the remaining array (an array without the first element) and swap it with the second element. Then you look for the smallest element in the remaining array (an array without first and second elements) and swap it with the third element, and so on.

   **Big O complexities** :
   Space complexity worst case:  O(1)
   
   |Time complexity|
   |----|
   |Best : O(n^2) |
   |Average : O(n^2) |
   |Worst : O(n^2) |

2. **Insertion sort** : The algorithm that people often use to sort bridge hands is to consider the cards one at a time, inserting each into its proper place among those already considered (keeping them sorted). In a computer implementation, we need to make space for the current item by moving larger items one position to the right, before inserting the current item into the vacated position.
Following are some of the important characteristics of Insertion Sort.

      * It has one of the simplest implementation
      * It is efficient for smaller data sets, but very inefficient for larger lists.
      * Insertion Sort is adaptive, that means it reduces its total number of steps if given a partially sorted list, hence it increases its efficiency.
      * It is better than Selection Sort and Bubble Sort algorithms.
      * Its space complexity is less, like Bubble Sorting, insertion sort also requires a single additional memory space.
      * It is Stable, as it does not change the relative order of elements with equal keys


   **Big O complexities** :
   Space complexity worst case:  O(1)
   
   |Time complexity|
   |----|
   |Best : O(n) |
   |Average : O(n^2) |
   |Worst : O(n^2) |

3. **Shell sort** : Shellsort is a simple extension of insertion sort that gains speed by allowing exchanges of entries that are far apart, to produce partially sorted arrays that can be efficiently sorted, eventually by insertion sort. The idea is to rearrange the array to give it the property that taking every hth entry (starting anywhere) yields a sorted sequence. Such an array is said to be h-sorted.By h-sorting for some large values of h, we can move entries in the array long distances and thus make it easier to h-sort for smaller values of h. Using such a procedure for any increment sequence of values of h that ends in 1 will produce a sorted array: that is shellsort. Shell.java is an implementation of this method. The number of compares used by shellsort with the increments 1, 4, 13, 40, 121, 364, ... is bounded by a small multiple of N times the number of increments used, in this case it is is O(N^(3/2)).

   **Big O complexities** :
   Space complexity worst case:  O(n) total, O(1) auxilary
   
   |Time complexity|
   |----|
   |Best : O(nlog(n)) |
   |Average : depends on gap sequence |
   |Worst : O(n^2) |

4. **Bubble sort** : The algorithm works by comparing each item in the list with the item next to it, and swapping them if required. In other words, the largest element has bubbled to the top of the array. The algorithm repeats this process until it makes a pass all the way through the list without swapping any items.It is called Bubble sort, because with each iteration the smaller element in the list bubbles up towards the first place, just like a water bubble rises up to the water surface.

  **Big O complexities** :
   Space complexity worst case:  O(1)
   
   |Time complexity|
   |----|
   |Best : O(n) |
   |Average : O(n^2) |
   |Worst : O(n^2) |

5. **Merge sort** :Merge-sort is based on the divide-and-conquer paradigm. It involves the following three steps:
   * Divide the array into two (or more) subarrays
   * Sort each subarray (Conquer)
   * Merge them into one (in a smart way!)
   Its prime disadvantage is that it uses extra space proportional to N.The method merge(a, lo, mid, hi) and puts the results of merging the subarrays auxilary_array[lo..mid] with auxilary_array[mid+1..hi] into a single ordered array, leaving the result in a[lo..hi]. While it would be desirable to implement this method without using a significant amount of extra space, such solutions are remarkably complicated. Instead, merge() copies everything to an auxiliary array and then merges back to the original.
      * It requires equal amount of additional space as the unsorted list. Hence its not at all recommended for searching large unsorted lists.
      * It is the best Sorting technique for sorting Linked Lists.


   **Big O complexities** :
   Space complexity worst case:  O(n)
   
   |Time complexity|
   |----|
   |Best : O(nlog(n)) |
   |Average : O(nlog(n)) |
   |Worst : O(nlog(n)) |


6. **Quick sort** : Quicksort is popular because it is not difficult to implement, works well for a variety of different kinds of input data, and is substantially faster than any other sorting method in typical applications. It is in-place (uses only a small auxiliary stack), requires time proportional to N log N on the average to sort N items, and has an extremely short inner loop. Quicksort is a divide-and-conquer method for sorting. It works by partitioning an array into two parts, then sorting the parts independently.
The crux of the method is the partitioning process, which rearranges the array to make the following three conditions hold:
   * The entry a[j] is in its final place in the array, for some j.
   * No entry in a[lo] through a[j-1] is greater than a[j].
   * No entry in a[j+1] through a[hi] is less than a[j].
This j point is called pivot point at which the partition takes place. We achieve a complete sort by partitioning, then recursively applying the method to the subarrays. It is a randomized algorithm, because it randomly shuffles the array before sorting it.


   **Big O complexities** :
   Space complexity worst case:  O(nlog(n))
   
   |Time complexity|
   |----|
   |Best : O(nlog(n)) |
   |Average : O(nlog(n)) |
   |Worst : O(n^2) |


7. **Heap sort** :The heap sort combines the best of both merge sort and insertion sort. Like merge sort, the worst case time of heap sort is O(n log n) and like insertion sort, heap sort sorts in-place. The heap sort algorithm starts by using procedure BUILD-HEAP to build a heap on the input array A[1 . . n]. Since the maximum element of the array stored at the root A[1], it can be put into its correct final position by exchanging it with A[n] (the last element in A). If we now discard node n from the heap than the remaining elements can be made into heap. Note that the new element at the root may violate the heap property. All that is needed to restore the heap property.The HEAPSORT procedure takes time O(n lg n), since the call to BUILD_HEAP takes time O(n) and each of the n -1 calls to Heapify takes time O(lg n).

      * Heap sort is not a Stable sort, and requires a constant space for sorting a list.
      * Heap Sort is very fast and is widely used for sorting.


   **Big O complexities** :
   Space complexity worst case:  O(1)
   
   |Time complexity|
   |----|
   |Best : O(nlog(n)) |
   |Average : O(nlog(n)) |
   |Worst : O(nlog(n)) |


#### Integer sorting :  

It is the algorithmic problem of sorting a collection of data values by numeric keys, each of which is an integer. Algorithms designed for integer sorting may also often be applied to sorting problems in which the keys are floating point numbers or text strings.

1. **Bucket sort** :Bucket sort, or bin sort, is a sorting algorithm that works by distributing the elements of an array into a number of buckets. Each bucket is then sorted individually, either using a different sorting algorithm, or by recursively applying the bucket sorting algorithm.
   Bucket sort works as follows:

      * Set up an array of initially empty "buckets".
      * Scatter: Go over the original array, putting each object in its bucket.
      * Sort each non-empty bucket.
      * Gather: Visit the buckets in order and put all elements back into the original array
      

    **Big O complexities** :
   Space complexity worst case:  O(n)
   
   |Time complexity|
   |----|
   |Best : O(n+k) |
   |Average : O(n+k) |
   |Worst : O(n^2) |
  

2. **Count sort** : It works by counting the number of objects that have each distinct key value, and using arithmetic on those counts to determine the positions of each key value in the output sequence. Its running time is linear in the number of items and the difference between the maximum and minimum key values, so it is only suitable for direct use in situations where the variation in keys is not significantly greater than the number of items. However, it is often used as a subroutine in another sorting algorithm, radix sort, that can handle larger keys more efficiently
    When elements are in range from 1 to k.


   **Big O complexities** :
   Space complexity worst case:  O(n+k)
   
   |Time complexity|
   |----|
   |Best : O(n+k) |
   |Average : O(n+k) |
   |Worst : O(n^2) |


3. **Radix sort** :The idea of Radix Sort is to do digit by digit sort starting from least significant digit to most significant digit. Radix sort uses counting sort as a subroutine to sort.
   Do following for each digit i where i varies from least significant digit to the most significant digit.
      Repeat : Sort input array using counting sort (or any stable sort) according to the i’th digit.


   **Big O complexities** :
   Space complexity worst case:  O(n+k)
   
   |Time complexity|
   |----|
   |Best : O(nk) |
   |Average : O(nk) |
   |Worst : O(nk) |

### Searching Algorithms:

#### Objective : 
The objective is to seek the required element in the given data set.

1. **Sequential search** :Sequential search involves looking at each value in turn (i.e., start with the value in array[0], then array[1], etc). The algorithm quits and returns true if the current value is v; it quits and returns false if it has looked at all of the values in the array without finding v.If the values are in sorted order, then the algorithm can sometimes quit and return false without having to look at all of the values in the array: v is not in the array if the current value is greater than v.


      **Big O complexities** :
   Space complexity worst case:  O(1)
   
   Time complexity of Unordered list
  
   |Item present|Item not present|
   |----|----|
   |Best : O(1) |Best : O(n) |
   |Average : O(n/2) |Average : O(n) |
   |Worst : O(n) |Worst : O(n) |

   Time complexity of Ordered list
  
   |Item present|Item not present|
   |----|----|
   |Best : O(1) |Best : O(1) |
   |Average : O(n/2) |Average : O(n/2) |
   |Worst : O(n) |Worst : O(n) |


2. **Binary search** :Can we do better than sequential search? The answer is yes.The idea is based on an algorithm which is a great example of a divide and conquer strategy.Binary search will start by examining the middle item. If that item is the one we are searching for, we are done. If it is not the correct item, we can use the ordered nature of the list to eliminate half of the remaining items. If the item we are searching for is greater than the middle item, we know that the entire lower half of the list as well as the middle item can be eliminated from further consideration. The item, if it is in the list, must be in the upper half.We can then repeat the process with the upper half. Start at the middle item and compare it against what we are looking for. Again, we either find it or split the list in half, therefore eliminating another large part of our possible search space. 

  **Big O complexities** :
  
  |Average|Worst case |
  |----|----|
  |Search : O(log(n))|Search : O(log(n) +1)|
   
   
3. **Hashing** :Search algorithms that use hashing consist of two separate parts. The first step is to compute a hash function that transforms the search key into an array index. Ideally, different keys would map to different indices. This ideal is generally beyond our reach, so we have to face the possibility that two or more different keys may hash to the same array index. Thus, the second part of a hashing search is a collision-resolution process that deals with this situation.A hash table is a collection of items which are stored in such a way as to make it easy to find them later. Each position of the hash table, often called a slot.The mapping between an item and the slot where that item belongs in the hash table is called the hash function. The hash function will take any item in the collection and return an integer in the range of slot names, between 0 and m-1. The occupancy of values in slots is defined by load factor, and is commonly denoted by λ=number of items /tablesize. Now when we want to search for an item, we simply use the hash function to compute the slot name for the item and then check the hash table to see if it is present. According to the hash function, two or more items would need to be in the same slot. This is referred to as a collision (it may also be called a “clash”).Unfortunately, given an arbitrary collection of items, there is no systematic way to construct a perfect hash function. 

  Something interesting : Cuckoo hashing. Maximum load with uniform hashing is log n / log log n. Improve to log log n by choosing least loaded of two. (Only improves to log log n / log d if choose least loaded of d.) cuckoo hashing achieves constant average time insertion and constant worst-case search: each item has two possible slots. Put in either of two available slots if empty; if not, eject another item in one of the two slots and move to its other slot (and recur). "The name derives from the behavior of some species of cuckoo, where the mother bird pushes eggs out of another bird's nest to lay her own." Rehash everything if you get into a relocation cycle.


  **Big O complexities** :
  
  |Average|Worst case |
  |----|----|
  |Search : O(1) |Search : O(n)|



4. **Breadth first search** : An algorithm that searches a tree(or graph) by searching levels of the tree first, starting from the root. 
   * If there are more than one node at the same level then it recursively searches from left to right.
   * While doing this it tracks the children nodes of the nodes on the current level.
   * When finished examining a level it moves to the left most node on the next level.
   * The bottom-right most node is evaluated last( the node that is deepest and is farthest right of its level)

   This kind of searching is optimal for a tree that is deep. The algorithm uses queue to store information about the tree while it traverses. Queues are more memory intensive, so depth first search is also memory intensive. 

   Time complexity : O(|E| +|V|)


5. **Depth first search** : An algorithm that searches a tree by searching depth of the tree first, starting at the root.
   * It traverses left down a tree until it cannot go further.
   * Once it reaches the end of a branch it traverses back up by trying the right child of nodes on that branch, and if possible left from the right children.
   * When finished examining a branch it moves to the node right of the root then tries to go left on all it's children until it reaches the bottom.
   * The right most node is evaluated last(the node that is ight of all it's ancestors).

   This kind of searching is optimal for tree that are shallow and wide. Uses stacks to push nodes onto and as Stacks are LIFO it does not need to keep track if the node pointers and is therefore less memory intensive than BFS. Once it cannot go further left it begins to evaluate the stack.

Time complexity : O(|E| +|V|)

Note :

1. For wide, shallow trees use BFS
2. For deep, narrow trees use DFS
3. BFS tends to be looping algorithm
4. DFS tends to be recursive algorithm
