## what is hash table?

It is also known as hash map is a data structure used to implement an associative array.It is a structure that can map keys to values.

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
