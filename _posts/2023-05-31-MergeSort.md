---
layout: single
title: "MergeSort"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Merge Sort

Merge Sort is one of **Divide and Conquer** strategies.<br><br>


### Process

1. **Divde**: Tear down the array until its length(arr.length) becomes 1.
2. **Conquer**: Merge the divided arrays back together while sorting.


### Merging Process

1. Given two arrays, compare the first element of each.
2. Remove the smaller element between the two from its original array and add  it to a new array.
3. Repeat this process until one of the two arrays is empty.
4. Append all elements of the remaining array to the new array.
5. The new array is now sorted.

<br><br>
This is how Merge Sort uses division and merging to sort the entire array. The time complexity of this algorithm is **O(n log n)**, which is efficient for all input sizes.


### Code
```
Part 1
public static void mergeSort(int[] array) {
    if (array.length < 2)
        return;

    int midIdx = array.length / 2;

    int[] left = new int[midIdx];
    int[] right = new int[array.length - midIdx];

    for (int i = 0; i < midIdx; i++) {
        left[i] = array[i];
    }

    for (int i = midIdx; i < array.length; i++) {
        right[i - midIdx] = array[i];
    }

    mergeSort(left);
    mergeSort(right);
}

```
