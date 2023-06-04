---
layout: single
title: "Quick Sort"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Quick Sort

Quick Sort is a sorting algorithm that utilizes a pivot to partition the elements and performs recursive sorting. This is also **Divide and Conquer** strategies. Similar to Merge Sort, Quick Sort follows the Divide and Conquer approach, where the array is divided into smaller subarrays, each of which is recursively sorted.


### Process

1. Choosing a Pivot: Select a pivot element as a reference point for partitioning.

2. Partitioning: Divide the array into two subarrays based on the pivot. One subarray contains elements smaller than the pivot, and the other contains elements larger than the pivot.

3. Placing Pivot: Put the pivot in its correct sorted position. Swap it with the element at the starting position after partitioning, so that all elements to its left are smaller or equal, and all elements to its right are larger.

The choice of the pivot can affect the efficiency of Quick Sort. Aim for a balanced partition by randomly selecting a pivot or choosing the middle element.

Quick Sort is an efficient sorting algorithm with an average time complexity of **O(n log n)**. It performs well when the array is large or contains many duplicate elements.


### Code
```
public static void quickSort(int[] array, int start, int end) {
    if (end - start < 1) {
        return;
    }

    // Part 1 - Choosing pivot
    Random rand = new Random();
    int pivotIdx = rand.nextInt(end - start + 1) + start;
    int pivotVal = array[pivotIdx];

    int temp = array[start];
    array[start] = array[pivotIdx];
    array[pivotIdx] = temp;

    // Part 2 - Partitioning
    int i = start + 1;
    int j = end;
    while (i <= j) {
        while (i <= j && array[i] <= pivotVal) {
            i++;
        }
        while (i <= j && array[j] >= pivotVal) {
            j--;
        }
        if (i <= j) {
            temp = array[i];
            array[i] = array[j];
            array[j] = temp;
            i++;
            j--;
        }
    }

    // Part 3 - Placing pivot in its correct position
    temp = array[start];
    array[start] = array[j];
    array[j] = temp;

    quickSort(array, start, j - 1);
    quickSort(array, j + 1, end);
}
```
