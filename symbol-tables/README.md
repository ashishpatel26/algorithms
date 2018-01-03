
Definition: the [Symbol Table](https://en.wikipedia.org/wiki/Symbol_table) data structure associates a key to a value. They are also known as associative arrays, **maps**, or **dictionaries**.

Complexity: 

Duplicated-keys: it is not possible to have duplicated keys because when a new element associated with an existing key is added, the old key is kept and the associated value is overwritten.

Implementation
--------------

- Linked list (sequential search). The keys are stored in a sequence of linked nodes.
- Ordered array (binary search)
- [Binary search trees](https://en.wikipedia.org/wiki/Binary_search_tree) (binary search). The main problem is with the deletion operation (Hibbard deletion) that is the only method used today. The Hibbard deletion unbalance the three leading to sqrt(N) height.


Methods
--------


Applications
------------


Quiz
-----




Material
--------
- **Coursera Algorithms Part 1**: week 4
- **Algorithms**, Sedgewick and Wayne (2014): Chapter 2.3
