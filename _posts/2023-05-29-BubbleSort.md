---
layout: single
title: "BubbleSort"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Bubble Sort

The core logic of Bubble Sort is "Moving the largest element in the array to the very end."<br>

There are several ideas for this process:<br>

Firstly, before traversing the array, the final index position is declared.<br>

Secondly, the declared final index of the array decreases with each iteration. This is due to the main logic of Bubble Sort, which places the largest elements towards the end of the array. Once the largest element is in the correct position, it becomes a 'sorted' element and does not need to be checked again.<br>

Thirdly, while traversing, adjacent element are compared and the larger element is placed behind. It's because of this third idea that Bubble Sort allows the largest element to be positioned at the end during traversal.

## Core logic code
```
int lastIdx = arr.length-1;
while (lastIdx > 0) {
    for (int i=0; i<lastIdx; i++) {
        int comparison = arr[i].compareTo(arr[i+1]);
        if (comparison > 0) {
            int Temp = arr[i];
            arr[i] = arr[i+1];
            arr[i+1] = temp;
         }
    }
    lastIdx--;
}
```

## Last Swap Optimization

The "Last Swap Optimization" is a strategy used to improve the efficiency of the bubble sort algorithm.<br>
This strategy is most effective when the array is **partially sorted**.<br>
As the array is traversed, it tracks the point at which the last swap occurs and sets this point as the ending point for the next traversal, reducing the number of element comparisons.<br>

## Core logic code (with Last Swap Optimization)

```
boolean swapsMade = true
int endIdx = arr.length-1;
while (swapsMade) {
    swapsMade = false;
    for (int i = 0; i < endIdx; i++) {
        if (arr[i] > arr[i+1]) {
            int temp = arr[i];
            arr[i] = arr[i+1];
            arr[i+1] = temp;
            swapsMade = true;
            endIdx = i;
        }
    }
}
```

