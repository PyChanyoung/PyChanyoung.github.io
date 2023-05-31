---
layout: single
title: "InsertionSort"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Insertion Sort

The key strategy of the Insertion Sort algorithm is to traverse through the array and insert a current element at the exact position within the already sorted portion of the array.<br>
The algorithm starts from the second element of the array because it assumes that the first element is already sorted. The current element(the second element and onwards) is compared with the previous element(referred to as `arr[i]` and `arr[i-1]`).
<br>
If `arr[i] > arr[i-1]`, it means that the current element is already in its correct position, and it is considered sorted. The index is then moved to the right to proceed with the next element.
<br>
However, if `arr[i] < arr[i-1]`, it indicates that the current element is not yet sorted, so it needs to be placed before the previous element. This involves shifting the previous elements to the right to make room for the current element in its correct sorted position.
<br>
By moving to the next element in the array and repeating this logic so far, the algorithm continues to traverse through all elements, ensuring that each element is inserted at the appropriate position in the sorted portion. Eventually, the entire array becomes sorted.

## Core logic code

```
for (int i = 1; i < arr.length-1; i++) {
    for (int j = i-1; j >= 0; j--) {
        if (arr[j] > arr[j+1]) {
            int temp = arr[j + 1];
            arr[j + 1] = arr[j];
            arr[j] = temp;
        }
    }
}
```