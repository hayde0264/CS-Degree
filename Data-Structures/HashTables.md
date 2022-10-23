# Hash Tables 

A hash table, or **hash map**, is an **abstract data type** that maps **keys to values**. Since each data value has its own unique index, **accessing data becomes very 
fast**.

# What is Hashing? 
Hashing is a method used to **convert a range of key values into a range of indexes of an array**. 

## Components of Hashing: 
1. In hashing, **large keys are converted into smaller keys by using** hash functions. 
2. Hash functions allocate such data to an array that places the values within **key-value** tables.


## Hashing allows operations such as: 
- **Searching** for element in a hash table 
- **Inserting** elements into a hash table 
- **Deleting** elements from a hash table 

# Collision 
Collisions occur when **two keys get mapped to the same index**.

## Chaining 
**chaining** - solves collisions by **using linked lists that each have unique indexes**.               

## Probing 
**probing** solves collisions by **creating methods**.

These methods, such as linear probing, quadratic probing, and double hashing **, are algorithms with jobs to find available spots for hashes**.

# Advantages of Hash Tables: 
- high performance for reading, writing, and deleting values
- time complexities remain constant regardless of the number of items within a table
- they perform well among large datasets

# Disadvantages of Hash Tables: 
- you cannot use null values as keys
- collisions cannot be avoided when generating keys using hash functions



During a lookup, **the key becomes "hashed"**, thus indicating where the index of the corresponding value. 

# References 
Basics of Hash Tables. (n.d.). *hacker earth*. <https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/> 

Data Structures and Algorithms - Hash Table. (n.d.). *tutorials point*. <https://www.tutorialspoint.com/data_structures_algorithms/hash_data_structure.htm> 

Hash Table. (2022, October 23). *Wikipedia*. <https://en.wikipedia.org/wiki/Hash_table> 

What is a hash table? (2022). *educative*. <https://www.educative.io/answers/what-is-a-hash-table> 
