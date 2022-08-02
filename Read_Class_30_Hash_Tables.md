## what is hash table?

It is also known as hash map is a data structure used to implement an associative array.It is a structure that can map keys to values.



## Terminology:

Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.


Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.


Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.


## Why do we use them?

Hold unique values

Dictionary

Library

## What Are they

Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. 

A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.



## How it works?

A hash table uses a hash function to compute an index into an array of buckets or slots, from which the correct value can be found.

See the below diagram it clearly explains.

![hashTable](Screen/tiD5Z.png)

## Advantages:

In a well-dimensioned hash table, the average cost for each lookup is independent of the number of elements stored in the table.

Many hash table designs also allow arbitrary insertions and deletions of key-value pairs.

In many situations, hash tables turn out to be more efficient than search trees or any other table lookup structure.

## Disadvantages:

The hash tables are not effective when the number of entries is very small. (However, in some cases the high cost of computing the hash function can be mitigated by saving the hash value together with the key.)

## Uses:

They are widely used in many kinds of computer software, particularly for associative arrays, database indexing, caches and sets.
