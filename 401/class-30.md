# Hash Tables

## Terminology

- Hash: ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value
- Buckets: what is contained in each index of teh array of the hashtable, each index is a bucket (index could contain multiple key-value pairs if a collision occurs)
- Collisions: what happens when more than one key gets hashed to the same location of the hashtable

## About Hashtables

- Data structure that utilizes key value pairs, every node or bucket has both a key, and a value
- Basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value
- Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity
- Hash function takes a key and returns an integer, use the integer to determine where the key/value pair should be placed in the array (hash code)
- The hash code is used again to read something from the hash map
- Take the key, run it through the hash code to get a number, use that number to index the array

## Creating a Hash

- Hashtable traditionally is created from an array
- After you've created your array, do some sort of logic to turn that "key" into a numeric number value (example: Add or multiply all the ASCII values together, Multiply it by a prime number such as 599, Use modulo to get the remainder of the result, when divided by the total size of the array, Insert into the array at that index)
- Each index of the array can hold many types of values
- Each index of the array contain “buckets”, and each of these “buckets” holds one key/value pair combination
- When there is no entry in a specific bucket, the buckets (each index of the array) all start null
- The hash table starts each bucket empty and overwrites their value once a key generates a hash code that corresponds with an index

## Collisions

- Collision occurs when more than one key hashes to the same index in an array
- Collisions are solved by changing the initial state of the buckets
- Instead of starting them all as null we can initialize a LinkedList in each one
- Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list
- Since different keys can lead to the same bucket it’s important to store the entire key/value pair in the bucket, not just the value

## To Store Values

- Hash maps to this to store values:
  - accept a key
  - calculate the hash of the key
  - use modulus to convert the hash into an array index
  - store the key with the value by appending both to the end of a linked list

## To Read Values

- Hash maps do this to read value:
  - accept a key
  - calculate the hash of the key
  - use modulus to convert the hash into an array index
  - use the array index to access the short LinkedList representing a bucket
  - search through the bucket looking for a node with a key/value pair that matches the key you were given