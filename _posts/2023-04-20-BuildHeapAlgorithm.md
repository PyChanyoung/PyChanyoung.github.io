---
layout: single
title: "The BuildHeap Algorithm"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Definition
The BuildHeap algorithm is a procedure for building a binary heap from an unsorted array. A binary heap is a data structure that satisfies the heap property: the key of each node is greater than or equal to the keys of its children. In a binary heap, the root node contains the largest key (in a max-heap) or the smallest key (in a min-heap).

## Build Heap Example (MinHeap)
```

Given array: [1, 71, 14, 32, 33, 4, 7 ,17, 5]
                1
              /   \
            71     14
           /  \   /  \
          32  33 4    7
         /  \
        17   5

Comparison Step 1.
    1. Compare 17 and 5 (=5 is small)
    2. Compare 32 and 17(=17 is small)
    3. Compare 32 and 5 (=5 is small)

    5 is smallest. So swap 32 and 5.
          32            5
         /  \    =>    / \
        17   5        17 32

Comparison Step 2.
    1. Compare 4 and 7  (=4 is small)
    2. Compare 14 and 4 (=4 is small)
    3. Compare 14 and 7 (=7 is small)

    4 is smallest. So swap 14 and 4.
          14            4
         /  \    =>    / \
        4    7        14  7

Comparison Step 3.
    1. Compare 5 and 33 (=5 is small)
    2. Compare 71 and 5 (=5 is small)
    3. Compare 71 and 33(=33 is small)

    5 is smallest. So swap 71 and 5.
          71            5
         /  \    =>    / \
        5   33        71 33

Comparison Step 4.
    1. Compare 5 and 14 (=5 is small)
    2. Compare 1 and 5  (=1 is small)
    3. Compare 1 and 14 (=1 is small)

    1 is smallest. So no swap occurs.
          1            1
         / \    =>    / \
        5   4        5   4

Comparison Step 5.
    1. Compare 71 and 33 (=33 is small)
    2. Compare 5 and 71  (=5 is small)
    3. Compare 5 and 33  (=5 is small)

    5 is smallest. So no swap occurs.
          5            5
         / \    =>    / \
        71 33        71 33

Comparison Step 6.
    1. Compare 14 and 7 (=7 is small)
    2. Compare 4 and 14 (=4 is small)
    3. Compare 4 and 7  (=4 is small)

    4 is smallest. So no swap occurs.
          4            4
         / \    =>    / \
        14  7        14  7

Comparison Step 7.
    1. Compare 17 and 32 (=17 is small)
    2. Compare 71 and 17 (=17 is small)
    3. Compare 71 and 32  (=32 is small)

    17 is smallest. So swap 71 and 17.
          71            17
         /  \    =>    /  \
        17  32        71  32

Final heapified tree:
                1
              /   \
             5     4
           /  \   /  \
          17  33 14   7
         /  \
        71  32

Swap occurs 4 times.
Comparison occurs 21 times.

```
