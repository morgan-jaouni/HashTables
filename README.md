# HashTables


## Concept
* What is a hash table?

#### A hash table is an unordered collection of key-value pairs, where each value is unique. The key is sent to a hash function (hashSimple()) that performs an arithmertic operation and gives the key a unique value that is not associated with any other keys.

![Screen Shot 2020-11-19 at 4 40 45 PM](https://user-images.githubusercontent.com/73499055/99732993-14ed1c80-2a86-11eb-8a71-6a4207c044f0.png)


* What operation does the hash function perform? 

#### The hash function takes a key and assigns each character(A-Z) an integer(1-26). Then, the value of each character within the key is summed % 11 = index value. 
* Why are hash tables beneficial? 

#### A hash table is an efficient way to sort a large amount of keys into unqiue key-value pairs. 

## Example A (Python)

### A school system could benefit from using hash tables by taking all of the registered students and using the hash function (hashSimple()) to give each student a unique school ID number. 

Class Person:
def __init__(self, name): <br/>
self.name = name <br/>
def __eq__(self, other):  <br/>
return self.name == other.name <br/>
def __hash__(self): <br/>
print(‘The hash is:’) <br/>
return hash((self.name)) <br/>
person = Person(‘Adam’) <br/>
print(hash(person)) <br/>
When run, the output of the above program will look like this, <br/>
The hash is: <br/>
5445254133660435902

### Example B

## Questions 

### What happens when the hash function assigns the same value to different keys? 

#### When the hash function assings an identical value to two different keys, it is defined as collision. When collisions occurs, the hash function will utilize linear probing which iterates through the values and assigns the key to the first available value in the index. This resulted in a new function being formed, linearHash() which will automatically verify that the value is unique before assigning it to a key.

### When would you want to use a hash table? 
A hash table organizes data so you can quickly look up values for a given key.

#### Strengths:
* Fast lookups - Lookups take O(1)O(1) time on average.
* Flexible keys - Most data types can be used for keys, as long as they're hashable.

#### Weaknesses:
* Slow worst-case lookups. Lookups take O(n)O(n) time in the worst case.
* Unordered. Keys aren't stored in a special order. If you're looking for the smallest key, the largest key, or all the keys in a range, you'll need to look through every key to find it.
* Single-directional lookups. While you can look up the value for a given key in O(1)O(1) time, looking up the keys for a given value requires looping through the whole dataset—O(n)O(n) time.
* Not cache-friendly. Many hash table implementations use linked lists, which don't put data next to each other in memory.
