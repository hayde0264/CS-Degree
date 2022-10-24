# Hash Tables 

A hash table, or **hash map**, is an **abstract data type** that maps **keys to values**. Since each data value has its own unique index, **accessing data becomes very 
fast**.

![hashTable](https://user-images.githubusercontent.com/109105989/197427494-4790075a-b1f4-4332-81b9-3fac9df79c47.png)

# What is Hashing? 
Hashing refers to a function used to **convert a range of key values into a range of indexes of an array**. 

![hashFunction](https://user-images.githubusercontent.com/109105989/197427490-c517e574-3593-47ae-ace5-f869c266d087.png)

## Components of Hashing: 
1. In hashing, **large keys are converted into smaller keys by using** hash functions. 
2. Hash functions allocate such data to an array that places the values within **key-value** tables.


## Hashing allows operations such as: 
- **Searching** for element in a hash table 
- **Inserting** elements into a hash table 
- **Deleting** elements from a hash table 

# Collision 
Collisions occur when **two keys get mapped to the same index**.

![collision](https://user-images.githubusercontent.com/109105989/197427488-7563185b-51fe-4304-9a22-16fce5875512.png)

## Chaining 
**chaining** - solves collisions by **using linked lists that each have unique indexes**.               

![chaining](https://user-images.githubusercontent.com/109105989/197427477-d8e90a2a-0455-44ba-b26b-8133a1be4f88.png)

## Probing 
**probing** solves collisions by **creating methods**.

![probing](https://user-images.githubusercontent.com/109105989/197427498-ab0a0dc5-09a7-4ad2-a2e2-6049421a06a5.png)

These methods, such as linear probing, quadratic probing, and double hashing **, are algorithms with jobs to find available spots for hashes**.

# Advantages of Hash Tables: 
- high performance for reading, writing, and deleting values
- time complexities remain constant regardless of the number of items within a table
- they perform well among large datasets

# Disadvantages of Hash Tables: 
- you cannot use null values as keys
- collisions cannot be avoided when generating keys using hash functions



# References 
Basics of Hash Tables. (n.d.). *hacker earth*. <https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/> 

Data Structures and Algorithms - Hash Table. (n.d.). *tutorials point*. <https://www.tutorialspoint.com/data_structures_algorithms/hash_data_structure.htm> 

Hash Table. (2022, October 23). *Wikipedia*. <https://en.wikipedia.org/wiki/Hash_table> 

What is a hash table? (2022). *educative*. <https://www.educative.io/answers/what-is-a-hash-table> 
