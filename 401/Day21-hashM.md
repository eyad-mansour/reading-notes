# Hash Table

The Hash table data structure stores elements in key-value pairs where

- Key- unique integer that is used for indexing the values.

- Value - data that are associated with keys.

#### Hashing (Hash Function)

In a hash table, a new index is processed using the keys. And, the element corresponding to that key is stored in the index. This process is called hashing.

#### Hash Collision

When the hash function generates the same index for multiple keys, there will be a conflict (what value to be stored in that index). This is called a hash collision.
We can resolve the hash collision using one of the following techniques.

- Collision resolution by chaining
- Open Addressing: Linear/Quadratic Probing and Double Hashing

1. Collision resolution by chaining

In chaining, if a hash function produces the same index for multiple elements, these elements are stored in the same index by using a doubly-linked list.

If j is the slot for multiple elements, it contains a pointer to the head of the list of elements. If no element is present, j contains NIL.

2. Open Addressing

Unlike chaining, open addressing doesn't store multiple elements into the same slot. Here, each slot is either filled with a single key or left NIL.

### Good Hash Functions

1. Division Method

If k is a key and m is the size of the hash table, the hash function h() is calculated as:

h(k) = k mod m

2. Multiplication Method

h(k) = ⌊m(kA mod 1)⌋

where,

kA mod 1 gives the fractional part kA,
⌊ ⌋ gives the floor value
A is any constant. The value of A lies between 0 and 1. But, an optimal choice will be ≈ (√5-1)/2 suggested by Knuth.

3. Universal Hashing

In Universal hashing, the hash function is chosen at random independent of keys.
