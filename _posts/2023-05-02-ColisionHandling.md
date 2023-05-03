---
layout: single
title: "HashMaps - Collision Handling"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Collision?

`Collision` in a HashMap refers to situation where two different keys have the same hash value.

HashMaps normally use the array data structure to store kv pairs and compute a unique hash value for each key. This enables fast data retrieval and access.

However, hash function can return same hash value for different input values, collision may occur. If a collision occurs, two or more keys with the same hash value will crash when searched for in the hashmaps.

## Collision Handling

Collision handling refers to the techniques used to resolve collisions.

There are several techniques to handle collisions in HashMaps.

- `Close addressing`

  - `Chaining`: In this method, each bucket in the HashMap stores a linked list of key-value pairs. When a collision occurs, the key-value pair is added to a linked list in the corresponding bucket (index) of the HashMap as a new node, along with any previously stored key-value pairs in the list.

- `Open addressing`

  - `Probing`

    - `Linear probing`: `Linear probing` is a collision resolution method that uses an array structure. When a key is hashed and its bucket is already occupied, this method searches for the next available slot in the array by probing linearly from the occupied slot. Typically, the index of the slot is calculated using the modulo operation on the hash value.

    - `Quadratic probing`: `Quadratic probing` is one of the methods to handle collisions in a HashMap. When a hash collision occurs, Quadratic probing searches for a different empty slot in the hash table by calculating the distance to move to the next slot using a `square value`.

    For example, if a collision occurs from hash value `h`, the first attempt checks the slot at `h+1(=h+1^2)`. If this slot is already occupied, the next attempt checks the slot at `h+4(=h+2^2)`, and then the slot at `h+9(=h+3^2)` is checked. This is how quadratic probing moves slots by calculating the distance using a square value.
