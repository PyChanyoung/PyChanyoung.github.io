---
layout: single
title: "SelectionSort"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Selection Sort

Selection Sort is a relatively intuitive sorting algorithm. It involves finding the smallest number within the array and moving it to the corret position. By performing this algorithm, the array gradually becomes sorted as larger numbers are sequentially placed from the beginning.

## Core logic code

```
for (int i = 0; i < arr.length - 1; i++) {
    int minIdx = i;
    for (int j = i + 1; j < arr.length; j++) {
        if (arr[minIdx] > arr[j]) {
            minIdx = j;
        }
    }
    int temp = arr[minIdx];
    arr[minIdx] = arr[i];
    arr[i] = temp;
}
```