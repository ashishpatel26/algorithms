
The [binary search trees](https://en.wikipedia.org/wiki/Binary_search_tree) are a particular [symbol table](https://en.wikipedia.org/wiki/Symbol_table) data structure that combines the flexibility of insertion in a linked list with the efficiency of search in an ordered array. Specifically, using two links per node (instead of the one link per node found in linked lists) leads to a very efficient implementation. In a binary search tree, each node also has a key and a value, with an ordering restriction to support efficient search.

<p align="center">
<img src="./images/bst_example_tree.png" width="300">
</p>


Implementation
--------------

1.  (binary search). The main problem is with the deletion operation (Hibbard deletion) that is the only method used today. The Hibbard deletion unbalance the three leading to sqrt(N) height.


Methods
--------

`put(key, value)`: insert a new pair of key-value. It must not be allowed to associate a `None` (python) value.

`get(key)`: return the value associated with the key. If the key does not exist it is possible to return `None`.

`remove(key)`: remove the key and the associated value.

`rank(key, lo, hi)`: (ordered array) the method is used in ordered array to search for a specific key using binary search. If the key is in the array it returns the index.

Applications
------------

1. Dictionaries: which is the application that also gives the name to the data structure (key=word, value=definition)
2. Account management: it can be used to process transactions (key=account-id, value=transaction detail)
3. Web search: find relevant pages based on keywords (key=keyword, value=web-pages)

Quiz
-----




Material
--------
- **Coursera Algorithms Part 1**: week 4
- **Algorithms**, Sedgewick and Wayne (2014): Chapter 3.2 "Binary Search Trees"
