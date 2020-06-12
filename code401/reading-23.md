# Hash Tables

 Finding a particular element in a data structure like a linked list involes traversing every element in the list until you find one 
 that matches. This gives a a big O of (n) at best. If you have array and the index of the particular element though, then the the 
 element can be found in O(1). A hash table attempts to recreate the efficieny of navigating arrays. A hash table, unlike a linked list 
 node, has a value and key. The key is then transformed using a hash function to turn it into a index of an array.

 Hash function: a function that can be used to map a data set of an arbitrary size to a data set of a fixed size, which falls into the 
 hash table. The values returned by a hash function are called hash values, hash codes, hash sums, or simply hashes.
 
Steps for creating a hash:
- Add or multiply all the ASCII values together.
- Multiply it by a prime number such as 599.
- Use modulo to get the remainder of the result, when divided by the total size of the array.
- Insert into the array at that index.


