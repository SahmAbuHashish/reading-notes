# Hashtables

## What is a Hashtable?

- Terminology:

1. Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

2. Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

3. Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

## Why do we use them?

- Hold unique values
- Dictionary
- Library

## What Are they

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

## Bucket Sizes

Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.

The load factor tells us something about how full the hash table is. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.

## Methods

- set(): When adding a new key/value pair to a hashtable:
    1. send the key to the hash() method.
    2. Once you determine the index of where it should be placed, go to that index
    3. Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
    4. If something does exist, add the new key/value pair to the data structure within that bucket.

- get(): The get() method takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

- has(): The has() method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the hash() method and check the hashtable if the key exists in the table given the index returned.

- keys(): The keys() method returns a collection (array) of unique hash keys.

- hash(): The hash() method will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.