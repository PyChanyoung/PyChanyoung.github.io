---
layout: single
title: "LSD(Least Significant Digit) Radix Sort"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## LSD(Least Significant Digit) Radix Sort
LSD Radix Sort repeatedly sorts integers digit by digit, moving from the *least significant digit* to the most significant. It has the advantage of not relying on comparisons, but it can only sort integer-like data types.

### Process

1. First, create a LinkedList array with a size of 19.
2. Set the iteration variable from 0 to k. K is longest number in the given array.
3. Iterate over all elements in the array.
4. Calculate the current digit of the current number. The digit is determined based on the iteration value.
5. Add the current number to the bucket corresponding nto the calculated digit. Store the current number in buckets[digit+9]. The addition of 9 is done to handle negative numbers since the bucket indexes range from -9 to 9.
6. Initialize the idx variable to 0. This variable represents the index of the array.
7. Traverse the buckets array.
8. Repeat until the current bucket is not empty.
9. Remove a value from the bucket and store it in the array at the position of idx. Increment idx.

### Code
```
Algorithm radix(array)
1.  buckets <- LinkedList[19]
2.  for iteration <- 0, k (number of digits in longest nubmer)
3.      for i <- 0, array.length
4.          calculate the current digit of array[i]
5.          add array[i] to buckets[digit + 9]
6.      idx <- 0
7.      for bucket in buckets
8.          while bucket is not empty
9.              array[idx++] <- value removed from bucket
```

