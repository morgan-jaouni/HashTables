# HashTables


## Concept
* What is a hash table?

#### A hash table is an unordered collection of key-value pairs, where each value is unique. The key is sent to a hash function (hashSimple()) that performs an arithmertic operation and gives the key a unique value that is not associated with any other keys.

* What operation does the hash function perform? 

#### The hash function takes a key and assigns each character(A-Z) an integer(1-26). Then, the value of each character within the key is summed % 11 = index value. 
* Why are hash tables beneficial? 

#### A hash table is an efficient way to sort a large amount of keys into unqiue key-value pairs. 

## Examples

### A school system could benefit from using hash tables by taking all of the registered students and using the hash function (hashSimple()) to give each student a unique school ID number. 

### 

## Questions 

### What happens when the hash function assigns the same value to different keys? 

#### When the hash function assings an identical value to two different keys, it is defined as collision. When collisions occurs, the hash function will utilize linear probing which iterates through the values and assigns the key to the first available value in the index. This resulted in a new function being formed, linearHash() which will automatically verify that the value is unique before assigning it to a key.

